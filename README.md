<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>TECLADO | Tech Fest Registration</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box;margin:0;padding:0}

#particles-js{
    position:fixed;
    inset:0;
    z-index:-1;
}

body{
    font-family:'Orbitron',sans-serif;
    background:radial-gradient(circle at top,#00f7ff22,#0f0c29,#000);
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    color:#fff;
}

.container{
    background:rgba(0,0,0,0.75);
    padding:30px;
    width:100%;
    max-width:430px;
    border-radius:18px;
    box-shadow:0 0 40px #00f7ff;
    animation:fadeIn 1s ease;
}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(30px)}
    to{opacity:1;transform:translateY(0)}
}

h1{
    text-align:center;
    color:#00f7ff;
    letter-spacing:3px;
    text-shadow:0 0 15px #00f7ff;
}

p{
    text-align:center;
    font-size:14px;
    color:#aaa;
    margin:10px 0 25px;
}

.input-group{margin-bottom:18px}

label{font-size:13px;margin-bottom:6px;display:block}

input{
    width:100%;
    padding:12px;
    border-radius:10px;
    border:none;
    outline:none;
    background:#0f0f1a;
    color:#00f7ff;
}

input:focus{box-shadow:0 0 12px #00f7ff}

button{
    width:100%;
    padding:14px;
    border:none;
    border-radius:12px;
    background:linear-gradient(90deg,#00f7ff,#00c9d1);
    font-size:16px;
    cursor:pointer;
}

button:hover{
    box-shadow:0 0 20px #00f7ff;
    transform:scale(1.03);
}

.footer{
    text-align:center;
    font-size:12px;
    margin-top:15px;
    color:#777;
}

/* POPUP */
.popup{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.8);
    display:none;
    justify-content:center;
    align-items:center;
}

.popup-box{
    background:#050512;
    padding:30px;
    border-radius:18px;
    text-align:center;
    box-shadow:0 0 30px #00f7ff;
}

/* FLOATING BUTTONS */
.fab{
    position:fixed;
    bottom:25px;
    width:55px;
    height:55px;
    border-radius:50%;
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:24px;
    cursor:pointer;
    box-shadow:0 0 20px #00f7ff;
}

.call-btn{left:25px;background:#00f7ff;color:#000}
.insta-btn{right:25px;background:#e1306c;color:#fff}

/* CALL POPUP */
.call-popup{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.85);
    display:none;
    justify-content:center;
    align-items:center;
}
.call-box{
    background:#050512;
    padding:25px;
    border-radius:16px;
    text-align:center;
}
.call-box a{
    display:block;
    margin:10px 0;
    color:#00f7ff;
    text-decoration:none;
}
</style>
</head>

<body>

<div id="particles-js"></div>

<div class="container">

<div style="text-align:center;margin-bottom:15px;">
  <img src="https://ccsit.uoc.ac.in/images/logouc.png" width="70">
  <div style="font-size:13px;color:#00f7ff;">University of Calicut</div>
</div>

<div style="display:flex;justify-content:center;gap:10px;">
  <img src="https://ccsit.uoc.ac.in/images/ccsit_pkd/TECLADO.png" width="80">
  <h1>TECLADO</h1>
</div>

<p>CCSIT PALAKKAD</p>

<form id="regForm">

<div class="input-group">
<label>Full Name</label>
<input type="text" name="name" required>
</div>

<div class="input-group">
<label>Email</label>
<input type="email" name="email" required>
</div>

<div class="input-group">
<label>College</label>
<input type="text" name="college" required>
</div>

<div class="input-group">
<label>Phone</label>
<input type="tel" name="phone" pattern="[0-9]{10}" required>
</div>

<div class="input-group">
<label>Select Events</label>
<label><input type="checkbox" name="event[]" value="Hackathon"> Hackathon</label>
<label><input type="checkbox" name="event[]" value="Web Designing"> Web Designing</label>
<label><input type="checkbox" name="event[]" value="Gaming"> Gaming</label>
<label><input type="checkbox" name="event[]" value="Debugging"> Debugging</label>
</div>

<div class="input-group">
<label>UPI Transaction ID</label>
<input type="text" name="txn" minlength="10" required>
</div>

<img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=UPI_PAYMENT" style="display:block;margin:auto">

<p style="font-size:12px;">Pay ₹100 to register</p>

<button type="submit">Register Now</button>
</form>

<div id="qrcode" style="margin-top:15px;text-align:center;"></div>
<div class="footer">© 2026 TECLADO</div>
</div>

<!-- SUCCESS POPUP -->
<div class="popup" id="popup">
<div class="popup-box">
<h2>🎉 Registration Successful</h2>
<button onclick="closePopup()">OK</button>
</div>
</div>

<div class="fab call-btn" onclick="openCall()">📞</div>
<div class="fab insta-btn" onclick="openInsta()">📸</div>

<div class="call-popup" id="callPopup">
<div class="call-box">

    <a href="tel:+918089859411">+91 80898 59411</a>
    <a href="tel:+918075619012">+91 80756 19012</a>
    <a href="tel:+918714923412">+91 87149 23412</a>
    <a href="tel:+918089483773">+91 80894 83773</a>
<button onclick="closeCall()">Close</button>
</div>
</div>

<script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/qrcodejs/qrcode.min.js"></script>

<script>
particlesJS("particles-js",{particles:{number:{value:60},color:{value:"#00f7ff"},size:{value:3},move:{speed:1}}});

document.getElementById("regForm").addEventListener("submit",e=>{
e.preventDefault();
const f=e.target;

if(f.txn.value.length<10) return alert("Invalid UPI ID");

if(!f.querySelector('input[name="event[]"]:checked'))
  return alert("Select at least one event");

document.getElementById("popup").style.display="flex";

new QRCode(document.getElementById("qrcode"),{
text:`TECLADO | ${f.name.value} | ${f.phone.value}`,
width:160,height:160
});

window.open(`https://wa.me/91${f.phone.value}?text=Registration%20Successful!`,"_blank");
f.reset();
});

function closePopup(){popup.style.display="none";}
function openCall(){callPopup.style.display="flex";}
function closeCall(){callPopup.style.display="none";}
function openInsta(){window.open("https://instagram.com/ccsit.palakkad_official","_blank");}
</script>

</body>
</html>
