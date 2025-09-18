<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Hisob-kitob</title>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f9f9f9;
      padding: 20px;
    }
    h2 { text-align: center; }
    label { display: block; margin-top: 10px; }
    input {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button {
      margin-top: 15px;
      width: 100%;
      padding: 10px;
      background: #2ea44f;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
    }
    button:hover { background: #22863a; }
  </style>
</head>
<body>
  <h2>🧾 Hisob-kitob</h2>

  <label>Mijoz ismi:</label>
  <input type="text" id="mijoz" placeholder="Ism">

  <label>Telefon:</label>
  <input type="text" id="telefon" placeholder="+998...">

  <label>Mahsulot:</label>
  <input type="text" id="mahsulot" placeholder="Mahsulot nomi">

  <label>Soni:</label>
  <input type="number" id="soni" placeholder="0">

  <label>Narx (so‘m):</label>
  <input type="number" id="narx" placeholder="0">

  <label>Qarz (so‘m):</label>
  <input type="number" id="qarz" value="0">

  <button onclick="sendData()">✅ Yakunla</button>

  <script>
    function sendData() {
      let data = {
        mijoz: document.getElementById("mijoz").value,
        telefon: document.getElementById("telefon").value,
        mahsulot: document.getElementById("mahsulot").value,
        soni: document.getElementById("soni").value,
        narx: document.getElementById("narx").value,
        qarz: document.getElementById("qarz").value
      };
      Telegram.WebApp.sendData(JSON.stringify(data));
    }
  </script>
</body>
</html>
