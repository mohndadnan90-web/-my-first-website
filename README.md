<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>بوابة مصرفية تجريبية</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Tahoma, Arial, sans-serif;
}

body {
  background: #f5f3f8;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.phone {
  width: 100%;
  max-width: 390px;
  min-height: 720px;
  background: white;
  border-radius: 25px;
  overflow: hidden;
  box-shadow: 0 10px 35px #33204a25;
}

.top {
  height: 65px;
  background: white;
  display: flex;
  align-items: center;
  justify-content: space-around;
  padding: 10px;
  border-bottom: 1px solid #eee;
}

.logo {
  background: #e9a000;
  color: white;
  border-radius: 12px;
  padding: 9px;
  font-weight: bold;
}

.bank-name {
  color: #58318c;
  font-size: 13px;
  font-weight: bold;
}

.hero {
  height: 285px;
  background: linear-gradient(120deg,#9862c3,#7134ad);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 20px;
}

.hero h2 {
  font-size: 21px;
  margin-bottom: 12px;
}

.symbol {
  font-size: 65px;
  margin-bottom: 15px;
}

.content {
  padding: 28px 25px;
}

.notice {
  background: #fff3dc;
  color: #754b00;
  text-align: center;
  font-size: 11px;
  padding: 9px;
  border-radius: 8px;
  margin-bottom: 22px;
}

label {
  display: block;
  color: #59358a;
  font-weight: bold;
  margin-bottom: 9px;
}

.input-box {
  width: 100%;
  background: #e9e5ef;
  border: 1px solid transparent;
  border-radius: 35px;
  padding: 17px;
  margin-bottom: 22px;
  outline: none;
  font-size: 15px;
  text-align: right;
}

.input-box:focus {
  border-color: #8955ba;
}

.login {
  width: 100%;
  background: #ee9c00;
  color: #fff;
  border: none;
  border-radius: 35px;
  padding: 17px;
  font-size: 19px;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 4px 8px #0002;
}

.login:active {
  transform: scale(.98);
}

.options {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 22px;
  font-size: 13px;
  color: #59358a;
}

.footer {
  text-align: center;
  color: #76569b;
  padding: 30px;
  font-size: 13px;
}

</style>
</head>

<body>

<div class="phone">

  <header class="top">
    <div class="logo">A+</div>
    <div class="bank-name">
      المصرف التجريبي الإسلامي
      <br>
      DEMO ISLAMIC BANK
    </div>
    <div style="font-size:28px;color:#7540a8">✺</div>
  </header>

  <section class="hero">
    <div>
      <div class="symbol">✺</div>
      <h2>المصرف التجريبي الإسلامي</h2>
      <p>بوابتك المصرفية الرقمية</p>
    </div>
  </section>

  <main class="content">

    <div class="notice">
      نموذج عرض تجريبي — لا تدخل بيانات مصرفية حقيقية
    </div>

    <label>رقم المستخدم التجريبي</label>
    <input
      class="input-box"
      type="text"
      placeholder="أدخل رقم تجريبي"
      autocomplete="off"
    >

    <label>كلمة المرور التجريبية</label>
    <input
      class="input-box"
      type="password"
      id="password"
      placeholder="أدخل كلمة تجريبية"
      autocomplete="off"
    >

    <button class="login" onclick="demoLogin()">
      دخول تجريبي
    </button>

    <div class="options">
      <span>
        <input type="checkbox" id="show">
        إظهار كلمة المرور
      </span>
      <span>نسيت كلمة المرور؟</span>
    </div>

  </main>

  <footer class="footer">
    ✦ خدمات مصرفية تجريبية ✦
    <p style="margin-top:15px">الإصدار التجريبي 1.0</p>
  </footer>

</div>

<script>
document.getElementById("show").addEventListener("change", function() {
  document.getElementById("password").type =
    this.checked ? "text" : "password";
});

function demoLogin() {
  alert("هذه واجهة تجريبية فقط. لا يتم إرسال أو حفظ أي بيانات.");
}
</script>

</body>
</html><label>رسالة تجريبية</label>
<textarea
  id="message"
  class="input-box"
  placeholder="اكتب رسالتك هنا..."
  rows="3">
</textarea>

<button
  type="button"
  style="background:#159447;color:white;border:0;
  border-radius:10px;padding:12px 25px;
  font-size:16px;cursor:pointer;"
  onclick="sendMessage()">
  إرسال
</button>function sendMessage() {
  const message = document.getElementById("message").value.trim();

  if (!message) {
    alert("اكتب رسالتك أولاً");
    return;
  }

  const email = "mohndadnan90@gmail.com";
  const subject = "رسالة من الموقع التجريبي";

  const url = "mailto:" + email +
    "?subject=" + encodeURIComponent(subject) +
    "&body=" + encodeURIComponent(message);

  window.location.href = url;
}
