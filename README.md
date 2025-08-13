<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coming Soon</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #fff;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            letter-spacing: 2px;
        }

        p {
            font-size: 1.2rem;
            margin-bottom: 20px;
            opacity: 0.8;
        }

        .countdown {
            font-size: 2rem;
            font-weight: bold;
            margin-top: 10px;
        }

        .socials {
            margin-top: 30px;
        }

        .socials a {
            color: #fff;
            margin: 0 10px;
            font-size: 1.5rem;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .socials a:hover {
            color: #1db954;
        }
    </style>
    <script>
        // Countdown Timer
        function startCountdown() {
            const launchDate = new Date("2025-12-31T00:00:00").getTime();
            const countdownElement = document.getElementById("countdown");

            setInterval(() => {
                const now = new Date().getTime();
                const distance = launchDate - now;

                if (distance < 0) {
                    countdownElement.innerHTML = "We're Live!";
                    return;
                }

                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);

                countdownElement.innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;
            }, 1000);
        }
    </script>
    <!-- Font Awesome CDN for icons -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body onload="startCountdown()">

    <h1>Coming Soon</h1>
    <p>website under construction. Stay tuned for something amazing!</p>
    <div id="countdown" class="countdown"></div>

    <div class="socials">
        <a href="#"><i class="fab fa-github"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
        <a href="#"><i class="fab fa-linkedin"></i></a>
    </div>

</body>
</html>
