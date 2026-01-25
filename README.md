<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>TECLADO | CCSIT Palakkad</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- GOOGLE FONT -->
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap" rel="stylesheet">

    <style>
        * {
            box-sizing: border-box;
        }
        
        body {
            margin: 0;
            font-family: 'Orbitron', sans-serif;
            background: radial-gradient(circle at top, #0f0c29, #302b63, #24243e);
            color: #fff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        /* PARTICLES */
        
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        /* TOP LOGO */
        
        .top-logo {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 70px;
            filter: drop-shadow(0 0 12px rgba(255, 120, 0, 0.9));
        }
        /* CARD */
        
        .container {
            background: rgba(0, 0, 0, 0.55);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(0, 255, 204, 0.4);
            padding: 30px;
            width: 100%;
            max-width: 420px;
            border-radius: 18px;
            box-shadow: 0 0 35px rgba(0, 255, 204, 0.35);
            animation: slideUp 1s ease;
        }
        
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        h1 {
            text-align: center;
            font-size: 38px;
            color: #00ffcc;
            text-shadow: 0 0 20px #00ffcc;
        }
        
        h2 {
            text-align: center;
            font-size: 14px;
            letter-spacing: 3px;
            color: #aaa;
            margin-bottom: 25px;
        }
        
        input {
            width: 100%;
            padding: 12px;
            margin: 8px 0;
            border-radius: 8px;
            border: none;
            background: #111;
            color: #00ffcc;
        }
        
        input::placeholder {
            color: #555;
        }
        
        .fee {
            text-align: center;
            margin: 15px 0;
            font-size: 20px;
            color: #00ffcc;
            text-shadow: 0 0 10px #00ffcc;
        }
        /* QR */
        
        .qr-box {
            text-align: center;
            margin: 20px 0;
            padding: 15px;
            border: 1px dashed #00ffcc;
            border-radius: 12px;
        }
        
        .qr-box img {
            width: 180px;
            border-radius: 10px;
        }
        
        .upi-id {
            font-size: 14px;
            color: #aaa;
            margin: 10px 0;
        }
        /* BUTTON */
        
        button,
        .upi-btn {
            width: 100%;
            padding: 14px;
            font-size: 15px;
            font-family: 'Orbitron', sans-serif;
            background: linear-gradient(90deg, #00ffcc, #00ccff);
            border: none;
            border-radius: 30px;
            cursor: pointer;
            color: #000;
            box-shadow: 0 0 20px rgba(0, 255, 204, 0.6);
            transition: 0.2s;
            margin-top: 10px;
        }
        
        button:hover,
        .upi-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 0 35px rgba(0, 255, 204, 0.9);
        }
        
        .upi-btn {
            text-decoration: none;
            display: block;
        }
        
        .hidden {
            display: none;
        }
        /* SUCCESS */
        
        .success {
            text-align: center;
            padding: 25px;
            border-radius: 12px;
            border: 1px solid #00ffcc;
            box-shadow: 0 0 30px rgba(0, 255, 204, 0.7);
            animation: glow 1.5s infinite alternate;
        }
        
        @keyframes glow {
            from {
                box-shadow: 0 0 15px rgba(0, 255, 204, 0.4);
            }
            to {
                box-shadow: 0 0 35px rgba(0, 255, 204, 1);
            }
        }
        
        .success a {
            color: #00ffcc;
            font-size: 18px;
            text-decoration: none;
        }
        /* FLOATING BUTTONS */
        
        .floating-btn {
            position: fixed;
            bottom: 20px;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            background: linear-gradient(135deg, #00ffcc, #00ccff);
            box-shadow: 0 0 20px rgba(0, 255, 204, 0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 22px;
            z-index: 999;
        }
        
        .call-btn {
            left: 20px;
        }
        
        .insta-btn {
            right: 20px;
        }
        
        .call-menu {
            position: fixed;
            bottom: 90px;
            left: 20px;
            background: rgba(0, 0, 0, 0.9);
            border: 1px solid #00ffcc;
            border-radius: 12px;
            padding: 12px;
            box-shadow: 0 0 25px rgba(0, 255, 204, 0.6);
        }
        
        .call-menu a {
            display: block;
            color: #00ffcc;
            text-decoration: none;
            margin: 8px 0;
        }
    </style>
</head>

<body>

    <div class="top-logo">
        <img src="https://ccsit.uoc.ac.in/images/ccsit_pkd/TECLADO.png" width="100%">
    </div>

    <div id="particles-js"></div>

    <div class="container">

        <h1>TECLADO</h1>
        <h2>CCSIT PALAKKAD</h2>

        <form id="regForm">
 <input type="text" name="fullname" placeholder="Full Name" required>
<input type="email" name="email" placeholder="Email" required>
<input type="text" name="college" placeholder="College Name" required>
<input type="tel" name="phone" pattern="[0-9]{10}" placeholder="Phone Number" required>
<input type="text" name="txn" placeholder="UPI Transaction ID" required>


            <div class="fee">₹1 Registration Fee</div>

            <div class="qr-box">
            <img src="c:\Users\HP\OneDrive\Desktop\NEW FOLDER SRM\PHOTO SHOP\qr.jfif">
                <div class="upi-id">UPI ID: <b>umasreeram333@oksbi</b></div>           
 <a class="upi-btn" id="upiPay"href="upi://pay?pa=umasreeram333@oksbi&pn=TECLADO&am=1&cu=INR">
   PAY USING UPI
</a>
            </div>

 <input type="text" placeholder="UPI Transaction ID" required>

            <button type="submit" id="submitBtn">I HAVE PAID</button>
        </form>

        <div class="success hidden" id="successBox">
            ✅ Payment Submitted!<br><br> You’ll be verified shortly 👀<br><br> Join WhatsApp Group 👇<br><br>
            <a href="https://chat.whatsapp.com/GbVDdVB3pSFKymxNxYkdv7" target="_blank">
        JOIN NOW
    </a>
        </div>

    </div>

    <!-- FLOATING -->
    <div class="floating-btn call-btn" id="callBtn">📞</div>
    <div class="call-menu hidden" id="callMenu">
        <a href="tel:8089859411">8089859411</a>
        <a href="tel:8714923412">8714923412</a>
        <a href="tel:8075619012">8075619012</a>
    </div>

    <a class="floating-btn insta-btn" href="https://www.instagram.com/ccsit.palakkad_official/" target="_blank">📸</a>

    <!-- PARTICLES -->
    <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
    <script>
        particlesJS("particles-js", {
            particles: {
                number: {
                    value: 90
                },
                color: {
                    value: "#00ffcc"
                },
                size: {
                    value: 3,
                    random: true
                },
                line_linked: {
                    enable: true,
                    color: "#00ffcc"
                },
                move: {
                    enable: true,
                    speed: 2
                }
            },
            interactivity: {
                events: {
                    onhover: {
                        enable: true,
                        mode: "repulse"
                    }
                }
            }
        });
    </script>

    <script>
        let paid = false;
        const upiBtn = document.getElementById("upiPay");
        const form = document.getElementById("regForm");
        const success = document.getElementById("successBox");
        const submitBtn = document.getElementById("submitBtn");

form.addEventListener("submit", e => {
    e.preventDefault();

    const txn = document.querySelector('[name="txn"]').value.trim();

    if (txn.length < 10) {
        alert("Enter a valid UPI Transaction ID");
        return;
    }

    if (!paid) {
        alert("Please complete UPI payment first!");
        return;
    }


        form.addEventListener("submit", e => {
            e.preventDefault();
            if (!paid) {
                alert("Please complete UPI payment first!");
                return;
            }
            submitBtn.innerText = "Verifying...";
            submitBtn.disabled = true;

            setTimeout(() => {
                form.classList.add("hidden");
                success.classList.remove("hidden");
            }, 1200);
        });
        document.getElementById("callBtn").onclick = () =>
            document.getElementById("callMenu").classList.toggle("hidden");
    </script>

</body>

</html>
