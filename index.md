<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecting...</title>
    <script type="text/javascript">
        // Function to detect the device type and redirect
        function redirectToStore() {
            var userAgent = navigator.userAgent || navigator.vendor || window.opera;

            // Detect iOS
            if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
                window.location.href = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795";
            }
            // Detect Android
            else if (/android/i.test(userAgent)) {
                window.location.href = "https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam";
            } else {
                // Fallback in case we can't detect the device
                window.location.href = "https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795";
            }
        }

        // Redirect when the page loads
        window.onload = redirectToStore;
    </script>
</head>
<body>
    <h1>Redirecting to the App Store...</h1>
    <p>If you are not redirected automatically, follow this <a href="https://apps.apple.com/mx/app/en-tu-hogar-by-coca-cola/id6444010795">link to the apple store</a>.</p>
    <p>or follow this <a href="https://play.google.com/store/apps/details?id=com.coca_cola.android.d2c_latam">link to the google play store</a>.</p>
</body>
</html>
