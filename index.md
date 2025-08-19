<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecting...</title>
    <script type="text/javascript">
        window.onload = function () {
            const userAgent = navigator.userAgent || navigator.vendor || window.opera;
            const isMobile = /iPhone|iPad|iPod|Android/i.test(userAgent);
            const isUserComingFromInstagramReferral = document.referrer.includes("instagram");
            const isUserComingFromFacebookReferral = document.referrer.includes("facebook");

            if (isMobile) {
                // Handle deep linking for Instagram and Facebook
                if (isUserComingFromInstagramReferral || isUserComingFromFacebookReferral) {
                    const url = window.location.href.replace("https://mrvidalciandt.github.io", "ethmobileapp://");
                    window.location = url;

                     // Detect iOS
                    if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
                        window.location.href = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795";
                    } 
                    // Detect Android
                    else if (/android/i.test(userAgent)) {
                        window.location.href = "https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam";
                    } else {
                        // Fallback for unrecognized devices
                        window.location.href = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795";
                    }
                } else {
                    // Detect iOS
                    if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
                        window.location.href = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795";
                    } 
                    // Detect Android
                    else if (/android/i.test(userAgent)) {
                        window.location.href = "https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam";
                    } else {
                        // Fallback for unrecognized devices
                        window.location.href = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795";
                    }
                }
            }
        }
    </script>
</head>
<body>
    <h1>Redirecting to the App Store...</h1>
    <p>If you are not redirected automatically, follow this <a href="https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795">link to the Apple Store</a>.</p>
    <p>or follow this <a href="https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam">link to the Google Play Store</a>.</p>
</body>
</html>
