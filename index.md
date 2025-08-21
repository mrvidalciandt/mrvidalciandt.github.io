<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecting...</title>
    <script type="text/javascript">
        function redirectTo() {
            const userAgent = navigator.userAgent || navigator.vendor || window.opera;
            const isMobile = /iPhone|iPad|iPod|Android/i.test(userAgent);
            const isUserComingFromInstagram = document.referrer.includes("instagram");
            const isUserComingFromFacebook = document.referrer.includes("facebook");

            if (isMobile) {
                // Deep link for Instagram and Facebook
                if (isUserComingFromInstagram || isUserComingFromFacebook) {
                    const link = document.getElementById("deepLink");
                    link.click(); // Trigger the click event to follow the link
                    // Fallback to App Store or Play Store after a delay
                    setTimeout(function() {
                        // Check if user is on iOS or Android
                        if (/iPad|iPhone|iPod/.test(userAgent)) {
                            window.location = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795"; // Fallback for iOS
                        } else if (/android/i.test(userAgent)) {
                            window.location = "https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam"; // Fallback for Android
                        }
                    }, 5000); // 2-second delay
                } else {
                    const link = document.getElementById("deepLink");
                    link.click(); // Trigger the click event to follow the link
                    // Fallback to App Store or Play Store after a delay
                    setTimeout(function() {
                        // Check if user is on iOS or Android
                        if (/iPad|iPhone|iPod/.test(userAgent)) {
                            window.location = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795"; // Fallback for iOS
                        } else if (/android/i.test(userAgent)) {
                            window.location = "https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam"; // Fallback for Android
                        }
                    }, 5000); // 2-second delay
                }
            } else {
                // Optionally handle desktop users, for example:
                window.location = "https://your-desktop-website.com"; // Redirect for desktop users
            }
        }

        // Run the redirect function when the page loads
        window.onload = redirectTo;
    </script>
</head>
<body>
    <h1>Redirecting...</h1>
    <a id="deepLink" href="ethmobileapp://" style="display:none;">Open App</a>
    <p>If you are not redirected automatically, follow this <a href="https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795">link to the Apple Store</a>.</p>
    <p>or follow this <a href="https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam">link to the Google Play Store</a>.</p>
</body>
</html>
