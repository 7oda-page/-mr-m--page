<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ömrüm</title>
  <style>
    body {
      font-family: system-ui, -apple-system, sans-serif;
      margin: 0;
      padding: 20px;
      background: url('Pg.jpg') no-repeat center center fixed;
      background-size: cover;
      color: #ffffff;
      text-align: center;
    }

‎    /* شاشة الباسورد */
    #lock-screen {
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.85);
      backdrop-filter: blur(8px);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 999;
    }

    .pass-box {
      background: rgba(255, 255, 255, 0.1);
      padding: 30px;
      border-radius: 16px;
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    input[type="23122024"] {
      padding: 12px;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      text-align: center;
      outline: none;
    }

    button {
      padding: 12px 24px;
      font-size: 16px;
      margin-top: 10px;
      border-radius: 8px;
      border: none;
      background-color: #007aff;
      color: white;
      cursor: pointer;
    }

‎    /* محتوى الصفحة */
    #content {
      display: none;
      max-width: 600px;
      margin: 0 auto;
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 20px;
    }

    .card {
      margin-bottom: 25px;
      background: rgba(255, 255, 255, 0.1);
      padding: 15px;
      border-radius: 12px;
    }

    img, video {
      width: 100%;
      border-radius: 10px;
    }

    .caption {
      margin-top: 10px;
      font-size: 15px;
      color: #e0e0e0;
    }

    .note-box {
      background: rgba(255, 255, 255, 0.15);
      padding: 15px;
      border-radius: 10px;
      margin: 20px 0;
      font-weight: bold;
    }

    audio {
      width: 100%;
      margin-top: 10px;
    }
  </style>
</head>
<body>

‎  <!-- شاشة القفل -->
  <div id="lock-screen">
    <div class="pass-box">
      <h3>Enter your password</h3>
      <input type="23122024" id="passInput" placeholder="password">
      <br>
      <button onclick="checkPassword()">Enter</button>
      <p id="error-msg" style="color: #ff4d4d; display: none; margin-top: 10px;"> The password is wrong!</p>
    </div>
  </div>

‎  <!-- محتوى الصفحة الرئيسي -->
  <div id="content">
    
‎    <!-- صورة 1 مع ملاحظة -->
    <div class="card">
      <img src="F1.jpg" alt="صورة">
      <div class="caption">بحبك</div>
    </div>

‎    <!-- فيديو مع ملاحظة -->
    <div class="card">
      <video controls>
        <source src="V1.mp4" type="video/mp4">
      </video>
      <div class="caption">بحبك</div>
    </div>

‎    <!-- النوت/الملاحظة العامة -->
    <div class="note-box">
‎     بحبك </div>

‎    <!-- تشغيل الأغنية -->
    <div class="card">
      <h4>🎵 المشغل الصوتي</h4>
      <audio controls>
        <source src="S1.mp3" type="audio/mpeg">
      </audio>
    </div>

  </div>

  <script>
    function checkPassword() {
‎      // استبدل 1234 بكلمة السر التي تريدها
      const correctPassword = "23122024"; 
      const input = document.getElementById("passInput").value;

      if (input === correctPassword) {
        document.getElementById("lock-screen").style.display = "none";
        document.getElementById("content").style.display = "block";
      } else {
        document.getElementById("error-msg").style.display = "block";
      }
    }
  </script>

</body>
</html>
