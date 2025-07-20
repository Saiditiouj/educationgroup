# educationgroup

# <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to said community - Hacker Style</title>
    <link href="https://fonts.googleapis.com/css2?family=VT323&family=Share+Tech+Mono&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --dark-background: #1a1a1a; /* Very dark background */
            --primary-red: #FF0000;    /* Original red for main accents */
            --neon-green: #00FF00;     /* Bright green for hover/focus */
            --text-color: #E0E0E0;     /* Light grey for general text */
            --input-bg: #2a2a2a;       /* Darker background for inputs */
            --border-color: #444444;   /* Dark grey border */
            --heading-color: #FF0000;  /* Red for main heading */
        }

        body {
            background-color: var(--dark-background);
            font-family: 'Share Tech Mono', monospace; /* Techy monospace font */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            color: var(--text-color);
            text-align: center;
            padding: 20px;
            box-sizing: border-box;
            /* Subtle background pattern (optional, can be an image too) */
            background-image:
                linear-gradient(0deg, transparent 24%, rgba(30, 30, 30, 0.8) 25%, rgba(30, 30, 30, 0.8) 26%, transparent 27%, transparent 74%, rgba(30, 30, 30, 0.8) 75%, rgba(30, 30, 30, 0.8) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(30, 30, 30, 0.8) 25%, rgba(30, 30, 30, 0.8) 26%, transparent 27%, transparent 74%, rgba(30, 30, 30, 0.8) 75%, rgba(30, 30, 30, 0.8) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
        }

        .container {
            background-color: rgba(0, 0, 0, 0.7); /* More opaque dark background */
            padding: 40px 60px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 255, 0, 0.3), 0 0 40px rgba(255, 0, 0, 0.2); /* Neon glow effect */
            max-width: 650px;
            width: 100%;
            border: 1px solid var(--border-color); /* Subtle border */
            position: relative;
            overflow: hidden; /* For potential future glitch effects */
        }

        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border-radius: 10px;
            background: repeating-linear-gradient(-45deg,
                rgba(0, 255, 0, 0.05),
                rgba(0, 255, 0, 0.05) 2px,
                transparent 2px,
                transparent 4px
            );
            pointer-events: none; /* Allows clicks to pass through */
        }


        h1 {
            font-family: 'VT323', monospace; /* Pixelated/Retro font for main heading */
            color: var(--heading-color); /* Main heading in red */
            margin-bottom: 25px;
            font-size: 3em; /* Larger, more impactful */
            text-shadow: 0 0 10px rgba(255, 0, 0, 0.7); /* Red glow for heading */
            letter-spacing: 2px; /* Spaced out letters */
        }

        h1 .icon {
            color: var(--neon-green); /* Icon in neon green */
            margin-right: 15px;
            font-size: 1em;
            text-shadow: 0 0 8px var(--neon-green); /* Green glow for icon */
        }

        p {
            font-size: 1.1em;
            line-height: 1.6;
            margin-bottom: 30px;
            color: var(--text-color);
        }

        .form-section {
            background-color: rgba(40, 40, 40, 0.8); /* Slightly lighter dark background for form */
            padding: 30px;
            border-radius: 8px;
            margin-top: 25px;
            text-align: left;
            border: 1px solid var(--border-color);
        }

        .form-group {
            margin-bottom: 20px;
            position: relative; /* For icon positioning */
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: var(--neon-green); /* Labels in neon green */
            font-family: 'VT323', monospace; /* Techy font for labels */
            font-size: 1.1em;
            letter-spacing: 1px;
            text-shadow: 0 0 5px rgba(0, 255, 0, 0.5);
        }

        .form-group i {
            position: absolute;
            left: 10px;
            top: 42px; /* Adjust based on input padding */
            color: var(--neon-green);
            font-size: 0.9em;
            pointer-events: none; /* Ensure clicks pass through icon to input */
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"] {
            width: calc(100% - 40px); /* Adjust width for padding and icon */
            padding: 12px 15px 12px 35px; /* Left padding for icon */
            border: 1px solid var(--border-color);
            border-radius: 5px;
            background-color: var(--input-bg);
            color: var(--neon-green); /* Input text in green */
            font-size: 1em;
            font-family: 'Share Tech Mono', monospace;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }

        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="tel"]:focus {
            border-color: var(--neon-green); /* Green border on focus */
            outline: none;
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.6); /* Green glow on focus */
            background-color: #3a3a3a; /* Slightly lighter dark on focus */
        }

        button {
            display: block;
            width: 100%;
            padding: 15px;
            background-color: var(--primary-red); /* Button base color is red */
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.3em;
            font-family: 'VT323', monospace; /* Techy font for button */
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
            margin-top: 30px;
            letter-spacing: 1px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.4); /* Red glow for button */
        }

        button:hover {
            background-color: var(--neon-green); /* Green on hover */
            color: black; /* Text becomes black on green background */
            transform: translateY(-2px); /* Slight lift effect */
            box-shadow: 0 0 15px rgba(0, 255, 0, 0.8); /* Stronger green glow on hover */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1><i class="fas fa-terminal icon"></i>Welcome to said community </h1>
        <p>
            <span style="color: var(--neon-green);">></span> Initializing connection...<br>
            <span style="color: var(--neon-green);">></span> Access granted.<br>
            <span style="color: var(--neon-green);">></span> Please authenticate by providing your credentials below.
        </p>

        <div class="form-section">
            <form action="#" method="POST">
                <div class="form-group">
                    <label for="fullName">Full Name:</label>
                    <i class="fas fa-user"></i>
                    <input type="text" id="fullName" name="fullName" placeholder="Enter your full alias" required>
                </div>

                <div class="form-group">
                    <label for="email">Email Address:</label>
                    <i class="fas fa-envelope"></i>
                    <input type="email" id="email" name="email" placeholder="e.g., ghost@domain.net" required>
                </div>

                <div class="form-group">
                    <label for="phone">Encrypted Contact:</label>
                    <i class="fas fa-phone-alt"></i>
                    <input type="tel" id="phone" name="phone" placeholder="e.g., +1.XXX.XXX.XXXX">
                </div>

                <div class="form-group">
                    <label for="address">Location Data (Optional):</label>
                    <i class="fas fa-map-marker-alt"></i>
                    <input type="text" id="address" name="address" placeholder="e.g., Undisclosed Location, Network">
                </div>

                <button type="submit">Transmit Data <i class="fas fa-arrow-circle-right"></i></button>
            </form>
        </div>
    </div>
</body>
</html>
