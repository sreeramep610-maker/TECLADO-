<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>TECLADO | Tech Fest Registration</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap" rel="stylesheet">

<!-- Particles JS -->
<script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }

body {
    font-family: 'Orbitron', sans-serif;
    background: #0f0c29;
    color: #fff;
    min-height: 100vh;
    overflow-x: hidden;
}

/* PARTICLES */
#particles-js {
    position: fixed;
    width: 100%;
    height: 100%;
    z-index: -1;
}

/* INTRO */
.intro {
    position: fixed;
    inset: 0;
    background: #000;
    display: flex;
    align-items: center;
    justify-content: center;
    animation: fadeOut 3s forwards;
    z-index: 10;
}

.intro h1 {
    font-size: 3rem;
    color: #00f5ff;
    animation: glow 1.5s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px #00f5ff; }
    to { text-shadow: 0 0 30px #6a00ff; }
}

@keyframes fadeOut {
    0% { opacity: 1; }
    80% { opacity: 1; }
    100% { opacity: 0; visibility: hidden; }
}
/* UNIVERSITY HEADER */
.uni-header {
    text-align: center;
    padding: 20px 10px 0;
}

.uni-logo {
    width: 260px;
    max-width: 85vw;
    margin-bottom: 6px;
    filter: drop-shadow(0 0 10px rgba(255,255,255,0.25));
}

.uni-text {
    font-size: 0.9rem;
    letter-spacing: 1px;
    color: #ddd;
    margin-bottom: 25px;
}

/* HEADER */
header {
    text-align: center;
    padding: 60px 20px;
}
.logo {
    width: 140px;
    max-width: 45vw;
    margin-bottom: 15px;
    filter: drop-shadow(0 0 15px rgba(255,120,0,0.6));
    animation: logoGlow 2s infinite alternate;
}

@keyframes logoGlow {
    from {
        filter: drop-shadow(0 0 10px rgba(255,120,0,0.4));
        transform: scale(1);
    }
    to {
        filter: drop-shadow(0 0 25px rgba(255,180,80,0.9));
        transform: scale(1.05);
    }
}

header h1 {
    font-size: 3rem;
    letter-spacing: 4px;
    color: #00f5ff;
}

header p {
    color: #ccc;
}

/* FORM CONTAINER */
.container {
    max-width: 700px;
    margin: auto;
    background: rgba(0,0,0,0.6);
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 0 25px rgba(0,245,255,0.3);
}

/* FORM */
form {
    display: flex;
    flex-direction: column;
    gap: 15px;
}
.events {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.events label {
    font-size: 0.9rem;
    color: #ccc;
    cursor: pointer;
}

.events input {
    margin-right: 8px;
    accent-color: #00f5ff;
}


input:focus, select:focus {
    outline: none;
    box-shadow: 0 0 10px #00f5ff;
}

button {
    margin-top: 20px;
    padding: 15px;
    background: linear-gradient(90deg,#00f5ff,#6a00ff);
    border: none;
    border-radius: 30px;
    color: #fff;
    font-size: 1.1rem;
    cursor: pointer;
}
.payment {
    margin-top: 15px;
    padding: 15px;
    border: 1px dashed #00f5ff;
    border-radius: 12px;
    text-align: center;
}

.fee {
    margin-bottom: 10px;
    color: #00f5ff;
}

.qr {
    width: 180px;
    margin: 10px auto;
    display: block;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(0,245,255,0.5);
}

.upi-id {
    font-size: 0.9rem;
    margin-bottom: 10px;
    color: #ccc;
}

.payment input {
    width: 100%;
    padding: 12px;
    border-radius: 8px;
    border: none;
    font-size: 1rem;
}

button:hover {
    transform: scale(1.05);
    box-shadow: 0 0 20px #00f5ff;
}

footer {
    text-align: center;
    padding: 20px;
    color: #aaa;
    font-size: 0.8rem;
}
/* FLOATING BUTTONS */
.floating-btn {
    position: fixed;
    bottom: 20px;
    width: 55px;
    height: 55px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 26px;
    color: #fff;
    cursor: pointer;
    z-index: 20;
    box-shadow: 0 0 20px rgba(0,245,255,0.7);
}

.call-btn {
    left: 20px;
    background: linear-gradient(135deg, #00f5ff, #0066ff);
}

.insta-btn {
    right: 20px;
    background: linear-gradient(135deg, #ff00cc, #ff6600);
}

/* CALL POPUP */
.call-popup {
    position: fixed;
    bottom: 90px;
    left: 20px;
    background: rgba(0,0,0,0.9);
    border-radius: 12px;
    padding: 15px;
    display: none;
    flex-direction: column;
    gap: 10px;
    z-index: 25;
    box-shadow: 0 0 25px rgba(0,245,255,0.4);
}

.call-popup a {
    color: #00f5ff;
    text-decoration: none;
    font-size: 0.9rem;
}

.call-popup a:hover {
    text-shadow: 0 0 10px #00f5ff;
}

</style>
</head>

<body>

<div id="particles-js"></div>

<!-- INTRO -->
<div class="intro">
    <h1>TECLADO</h1>
</div>

<header>
    <img src="https://ccsit.uoc.ac.in/images/ccsit_pkd/TECLADO.png" alt="TECLADO Logo" class="logo">
    <h1>TECLADO</h1>
    <p>CCSIT PALAKKAD</p>
</header>

<div class="container">
<form id="registrationForm">

<input type="text" name="name" placeholder="Full Name" required>
<input type="text" name="college" placeholder="College Name" required>
<input type="email" name="email" placeholder="Email" required>
<input type="tel" name="phone" placeholder="Phone Number" required>

<div class="events">
    <label>Select Events</label>

    <label><input type="checkbox" name="event[]" value="Coding Challenge"> Coding Challenge</label>
    <label><input type="checkbox" name="event[]" value="Hackathon"> Hackathon (+50 Rs)</label>
    <label><input type="checkbox" name="event[]" value="Tech Quiz"> Tech Quiz</label>
    <label><input type="checkbox" name="event[]" value="Web Design"> Web Design</label>
    <label><input type="checkbox" name="event[]" value="Gaming"> Gaming (+50 Rs)</label>
</div>
<div class="payment">
    <p class="fee">💸 Registration Fee: <strong>₹<span id="totalFee">100</span></strong></p>

    <img src="https://web.whatsapp.com/dcf2d375-d162-495d-9973-d793984f76bf" alt="UPI QR Code" class="qr">

    <p class="upi-id">UPI ID: <strong>umasreeram333@oksbi</strong></p>

    <input type="text" name="txn" placeholder="UPI Transaction ID" required>
    <input type="number" name="paidAmount" placeholder="Amount Paid (₹)" required>

    <input type="file" name="screenshot" accept="image/*" required>

<img id="preview" style="display:none; width:100%; margin-top:10px; border-radius:10px;">
</div>

<button type="submit" id="submitBtn" disabled style="opacity:0.5; cursor:not-allowed;">
    Register Now
</button>


</form>
</div>

<footer>
© 2026 TECLADO | CCSIT PALAKKAD
</footer>
<!-- CALL BUTTON -->
<div class="floating-btn call-btn" onclick="toggleCallPopup()">📞</div>

<!-- CALL POPUP -->
<div class="call-popup" id="callPopup">
    <a href="tel:+918089483773">+91 80894 83773</a>
    <a href="tel:+918089859411">+91 80898 59411</a>
    <a href="tel:+918714923412">+91 87149 23412</a>
    <a href="tel:+918075619012">+91 80756 19012</a>
</div>

<!-- INSTAGRAM BUTTON -->
<div class="floating-btn insta-btn" onclick="openInsta()">📸</div>
<!-- UNIVERSITY LOGO -->
<div class="uni-header">
    <img src="https://ccsit.uoc.ac.in/images/logouc.png" alt="University of Calicut" class="uni-logo">
    <div class="uni-text">University of Calicut</div>
</div>

<script>
    const PARTICIPANT_GROUP_LINK = "https://chat.whatsapp.com/GbVDdVB3pSFKymxNxYkdv7";

    const ADMIN_NUMBERS = [
    "+91 80756 19012"
];
function notifyAdmins(data) {
    const msg =
`🟢 NEW TECLADO REGISTRATION

👤 Name: ${data.name}
🏫 College: ${data.college}
📞 Phone: ${data.phone}
📧 Email: ${data.email}

🎯 Events: ${data.events}
💰 Amount: ₹${data.amount}
🧾 TXN ID: ${data.txn}

⏰ ${new Date().toLocaleString()}`;

    ADMIN_NUMBERS.forEach(num => {
        const url = `https://wa.me/${num}?text=${encodeURIComponent(msg)}`;
        window.open(url, "_blank");
    });
}

// PARTICLES CONFIG
particlesJS("particles-js", {
  particles: {
    number: { value: 80 },
    color: { value: "#00f5ff" },
    size: { value: 3 },
    move: { speed: 1 },
    line_linked: { enable: true, color: "#00f5ff" }
  }
});

// GOOGLE SHEET + WHATSAPP
const screenshotInput = document.querySelector('input[name="screenshot"]');
const preview = document.getElementById("preview");

screenshotInput.addEventListener("change", () => {
    const file = screenshotInput.files[0];
    if (file) {
        const reader = new FileReader();
        reader.onload = e => {
            preview.src = e.target.result;
            preview.style.display = "block";
        };
        reader.readAsDataURL(file);
    }
});
const baseFee = 100;
const extraEvents = {
    "Hackathon": 50,
    "Gaming": 50
};

const feeDisplay = document.getElementById("totalFee");
const eventCheckboxes = document.querySelectorAll('input[name="event[]"]');

function calculateFee() {
    let total = baseFee;

    eventCheckboxes.forEach(cb => {
        if (cb.checked && extraEvents[cb.value]) {
            total += extraEvents[cb.value];
        }
    });

    feeDisplay.textContent = total;
    return total;
}

eventCheckboxes.forEach(cb => {
    cb.addEventListener("change", calculateFee);
});

document.getElementById("registrationForm").addEventListener("submit", function(e){
    e.preventDefault();

    const form = e.target;
    const formData = new FormData(form);

    const events = [...document.querySelectorAll('input[name="event[]"]:checked')]
                   .map(e => e.value)
                   .join(", ");

    if (!events) {
        alert("Please select at least one event.");
        return;
    }

    formData.append("name", form.name.value);
    formData.append("college", form.college.value);
    formData.append("email", form.email.value);
    formData.append("phone", form.phone.value);
    formData.append("event", events);
    formData.append("txn", form.txn.value);
    const totalAmount = calculateFee();
    const paidInput = document.querySelector('input[name="paidAmount"]');
const submitBtn = document.getElementById("submitBtn");

function validatePayment() {
    const expected = calculateFee();
    const paid = Number(paidInput.value);

    if (paid === expected && expected > 0) {
        submitBtn.disabled = false;
        submitBtn.style.opacity = "1";
        submitBtn.style.cursor = "pointer";
    } else {
        submitBtn.disabled = true;
        submitBtn.style.opacity = "0.5";
        submitBtn.style.cursor = "not-allowed";
    }
}


function validatePayment() {
    const expected = calculateFee();
    const paid = Number(paidInput.value);

    if (paid === expected && expected > 0) {
        submitBtn.disabled = false;
        submitBtn.style.opacity = "1";
        submitBtn.style.cursor = "pointer";
    } else {
        submitBtn.disabled = true;
        submitBtn.style.opacity = "0.5";
        submitBtn.style.cursor = "not-allowed";
    }
}

paidInput.addEventListener("input", validatePayment);
eventCheckboxes.forEach(cb => cb.addEventListener("change", validatePayment));


formData.append("amount", totalAmount);

const paid = Number(form.paidAmount.value);

if (paid !== totalAmount) {
    alert(`❌ Payment mismatch!\nExpected: ₹${totalAmount}\nPaid: ₹${paid}`);
    return;
}

fetch("https://script.google.com/macros/s/AKfycbyXaDmOdRSdIbTueS6XZeZmYvaq2lTSA-GrSoCAHHzDTUprodwhjGS-YqwIu1YW05hxWQ/exec", {
    method: "POST",
    body: formData
})
.then(res => res.json())
.then(data => {

    const pid = data.participantId;
    const qr = data.qrUrl;

    // Admin alert
    notifyAdmins({
        name: form.name.value,
        college: form.college.value,
        phone: form.phone.value,
        email: form.email.value,
        events: events,
        amount: totalAmount,
        txn: form.txn.value
    });

    // WhatsApp message to participant
    const userMsg =
`🎉 TECLADO Registration Successful!

🆔 Participant ID: ${pid}
🎯 Events: ${events}
💰 Amount: ₹${totalAmount}

🎫 ENTRY QR:
${qr}

⚠️ Show this QR at the entry gate.
📢 Join participant group for updates 👇`;

    window.open(
        `https://wa.me/91${form.phone.value}?text=${encodeURIComponent(userMsg)}`,
        "_blank"
    );

    // Open WhatsApp group
    setTimeout(() => {
        window.open(PARTICIPANT_GROUP_LINK, "_blank");

    }, 1500);
});

});

function toggleCallPopup() {
    const popup = document.getElementById("callPopup");
    popup.style.display = popup.style.display === "flex" ? "none" : "flex";
}

function openInsta() {
    window.open("https://www.instagram.com/ccsit.palakkad_official", "_blank");
}

</script>

</body>
</html>


startScanner();
</script>

</body>
</html>

