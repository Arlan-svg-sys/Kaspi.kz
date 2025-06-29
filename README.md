<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Kaspi - Удостоверение</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background-color: #f0f0f0;
    }

    .header {
      background-color: #e30613;
      color: white;
      padding: 15px;
      text-align: center;
      font-weight: bold;
      font-size: 18px;
    }

    .container {
      max-width: 400px;
      margin: 30px auto;
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
    }

    label {
      display: block;
      margin: 15px 0 5px;
      font-size: 14px;
      color: #444;
    }

    input[type="text"],
    input[type="date"] {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 14px;
    }

    input[type="file"] {
      display: none;
    }

    .file-label {
      display: block;
      background-color: #e30613;
      color: white;
      text-align: center;
      padding: 10px;
      border-radius: 6px;
      cursor: pointer;
      margin-bottom: 10px;
    }

    .preview-img {
      width: 100%;
      margin-top: 10px;
      border-radius: 8px;
      display: none;
    }

    button {
      width: 100%;
      background-color: #e30613;
      color: white;
      padding: 12px;
      border: none;
      border-radius: 6px;
      font-size: 15px;
      margin-top: 15px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="header">Kaspi.kz</div>

  <div class="container">
    <label>ФИО</label>
    <input type="text" placeholder="Иванов Иван Иванович" />

    <label>ИИН</label>
    <input type="text" placeholder="000000000000" />

    <label>Дата выдачи</label>
    <input type="date" />

    <label for="photo" class="file-label">Загрузить фото удостоверения</label>
    <input type="file" id="photo" accept="image/*" onchange="loadImage(event)" />
    <img id="preview" class="preview-img" />

    <button onclick="alert('Данные успешно отправлены')">Отправить</button>
  </div>

  <script>
    function loadImage(event) {
      const image = document.getElementById('preview');
      image.src = URL.createObjectURL(event.target.files[0]);
      image.style.display = 'block';
    }
  </script>
</body>
</html>
