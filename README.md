# simatstransport

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SIMATS Transport Pass</title>

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: Arial, Helvetica, sans-serif;
}

{
    background:#ececec;
    overflow:hidden;body
}

/* ================= NAVBAR ================= */

.navbar{
    width:100%;
    height:58px;
    background:#4586de;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 18px;
    position:fixed;
    top:0;
    left:0;
    z-index:1000;
}

/* LEFT NAV */

.left-nav{
    display:flex;
    align-items:center;
}

/* LOGO */

.logo{
    width:42px;
    height:42px;
    object-fit:contain;
    margin-right:12px;
}

/* TITLE */

.title{
    color:white;
    font-size:16px;
    font-weight:700;
    letter-spacing:0.4px;
    font-family: "Trebuchet MS", Arial, sans-serif;
}

/* MENU */

.menu{
    display:flex;
    align-items:center;
    gap:30px;
}

.menu a{
    color:white;
    text-decoration:none;
    font-size:13px;
    font-weight:600;
    transition:0.2s;
}

.menu a:hover{
    color:#dcecff;
}

/* ================= MAIN ================= */

.main-container{
    height:100vh;
    overflow-y:auto;
    padding-top:78px;
    padding-bottom:90px;
}

/* SCROLLBAR */

.main-container::-webkit-scrollbar{
    width:8px;
}

.main-container::-webkit-scrollbar-thumb{
    background:#4586de;
    border-radius:10px;
}

.main-container::-webkit-scrollbar-track{
    background:#dadada;
}

/* ================= CARD ================= */

.card{
    width:360px;
    background:white;
    margin:auto;
    border:1px solid #cfcfcf;
}

/* STATUS */

.status{
    background:#19b700;
    color:white;
    text-align:center;
    padding:14px;
}

.time{
    font-size:18px;
    font-weight:700;
    margin-bottom:6px;
}

.valid{
    font-size:30px;
    font-weight:800;
    line-height:58px;
}

/* PROFILE */

.profile{
    text-align:center;
    padding-top:20px;
}

/* PROFILE IMAGE */

.profile-img{
    width:100%;
    max-width:360px;
    height:auto;
    display:block;
    margin:auto;
    opacity:0.45;
}

/* QR */

.qr{
    margin-top:-10px;
}

.qr img{
    width:95px;
}

/* NAME */

.name{
    margin-top:10px;
    font-size:20px;
    font-weight:700;
    color:black;
}

/* REG NO */

.reg{
    margin-top:8px;
    font-size:16px;
    font-weight:700;
    color:black;
}

/* STOP */

.stop{
    width:100%;
    background:#19b700;
    color:white;
    font-size:17px;
    font-weight:700;
    padding:8px;
    margin-top:15px;
}

/* FOOTER */

.footer{
    width:100%;
    height:54px;

    /* SIMPLE TRANSPARENCY */

    background:rgba(69, 134, 222, 0.88);

    color:white;

    display:flex;
    align-items:center;
    justify-content:center;

    position:fixed;
    bottom:0;
    left:0;

    font-size:15px;
    font-weight:bold;

    z-index:1000;
}


</style>
</head>

<body>

<!-- ================= NAVBAR ================= -->

<div class="navbar">

    <div class="left-nav">

        <!-- LOGO -->

        <img src="c:\Users\mukes\OneDrive\Pictures\Screenshots\Screenshot 2026-05-11 142400.png" class="logo">

        <!-- TITLE -->

        <div class="title">
            SIMATS TRANSPORTS
        </div>

    </div>

    <!-- MENU -->

    <div class="menu">

        <a href="#">Home</a>
        <a href="#">Pass Details</a>
        <a href="#">Notification</a>
        <a href="#">Raise Issue</a>
        <a href="#">Attendance</a>
        <a href="#">Contact</a>

        <a href="#">
            <i class="fa-solid fa-user"></i>
        </a>

        <a href="#">
            <i class="fa-solid fa-right-from-bracket"></i>
            Logout
        </a>

    </div>

</div>

<!-- ================= MAIN CONTENT ================= -->

<div class="main-container">

    <div class="card">

        <!-- STATUS -->

        <div class="status">

            <div class="time" id="datetime">
                11-MAY-2026 14:17:37
            </div>

            <div class="valid">
                VALID
            </div>

        </div>

        <!-- PROFILE -->

        <div class="profile">

            <!-- DEFAULT AVATAR -->

            <img src="https://cdn-icons-png.flaticon.com/512/149/149071.png"
            class="profile-img">

            <!-- QR CODE -->

            <div class="qr">

                <img src="https://api.qrserver.com/v1/create-qr-code/?size=120x120&data=212224230189">

            </div>

            <!-- NAME -->

            <div class="name">
                NITHEESH KUMAR B
            </div>

            <!-- REG NUMBER -->

            <div class="reg">
                212224230189
            </div>

            <!-- STOP -->

            <div class="stop">
                TIRUTTANI 10-D
            </div>

        </div>

    </div>

</div>

<!-- ================= FOOTER ================= -->

<div class="footer">
    © SIMATS - 2024
</div>

<!-- ================= JAVASCRIPT ================= -->

<script>

function updateDateTime(){

    const now = new Date();

    const options = {
        day:'2-digit',
        month:'short',
        year:'numeric'
    };

    let date = now.toLocaleDateString('en-GB', options)
    .replace(/ /g,'-')
    .toUpperCase();

    /* 24 HOUR FORMAT */

    let time = now.toLocaleTimeString('en-GB', {

        hour:'2-digit',
        minute:'2-digit',
        second:'2-digit',
        hour12:false

    });

    document.getElementById("datetime").innerHTML =
    `${date} ${time}`;
}

setInterval(updateDateTime,1000);

updateDateTime();

</script>

</body>
</html>

```
