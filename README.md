<!DOCTYPE html><html lang="kk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>OKMPUCHEMLAB</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
    }
    .navbar {
      background-color: #1b1b1b;
      color: white;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      padding: 10px 20px;
    }
    .navbar a {
      color: white;
      margin: 5px 10px;
      text-decoration: none;
    }
    .navbar a:hover {
      text-decoration: underline;
    }
    section {
      display: none;
      padding: 20px;
      background: white;
      max-width: 1200px;
      margin: 20px auto;
      border-radius: 8px;
    }
    section.active {
      display: block;
    }
    iframe {
      width: 100%;
      border: none;
      aspect-ratio: 16 / 9;
    }
    form input, form textarea, form select, form button {
      display: block;
      margin: 10px 0;
      padding: 10px;
      width: 100%;
    }
    footer {
      text-align: center;
      padding: 20px;
      background: #1b1b1b;
      color: white;
    }
  </style>
</head>
<body>
  <div class="navbar">
    <strong>OKMPUCHEMLAB</strong>
    <div>
      <a href="#" onclick="showSection('home')">Басты бет</a>
      <a href="#" onclick="showSection('courses')">Курстар</a>
      <a href="#" onclick="showSection('lab')">3D Лаборатория</a>
      <a href="#" onclick="showSection('table')">Менделеев</a>
      <a href="#" onclick="showSection('calc')">Калькулятор</a>
      <a href="#" onclick="showSection('achievements')">Жетістіктер</a>
      <a href="https://platonus.okmpu.kz" target="_blank">Платонус</a>
      <a href="https://chat.openai.com" target="_blank">Чат GPT</a>
      <a href="#" onclick="showSection('contact')">Байланыс</a>
    </div>
  </div>  <section id="home" class="active">
    <h2>Қош келдіңіздер!</h2>
    <p>OKMPUCHEMLAB – оқушылар мен студенттерге арналған виртуалды химия зертханасы.</p>
    <button onclick="showSection('courses')">Курстарды қарау</button>
  </section>  <section id="courses">
    <h2>Онлайн Курстар</h2>
    <p>Курс бағалары:</p>
    <ul>
      <li>Базалық курс – 10 000 тг</li>
      <li>Кеңейтілген курс – 20 000 тг</li>
      <li>VIP курс – 35 000 тг</li>
      <li>Мамыр айына дейін -20% жеңілдік</li>
    </ul>
    <iframe src="https://www.youtube.com/embed/DV0dFH74-6A" allowfullscreen></iframe>
    <iframe src="https://www.youtube.com/embed/XzORKDexBUc" allowfullscreen></iframe>
    <iframe src="https://www.youtube.com/embed/jvzjh2_h14A" allowfullscreen></iframe>
  </section>  <section id="lab">
    <h2>3D Лаборатория</h2>
    <p>Виртуалды тәжірибе жүргізуге арналған Canva платформасы:</p>
    <iframe src="https://yjcxuvcfgg.my.canva.site/dagnwc4-iik"></iframe>
  </section>  <section id="table">
    <h2>Менделеев Кестесі</h2>
    <iframe src="https://ptable.com"></iframe>
  </section>  <section id="calc">
    <h2>Химиялық Калькулятор</h2>
    <iframe src="https://www.calculator.net/chemical-equation-balancer.html"></iframe>
  </section>  <section id="achievements">
    <h2>Жетістіктер</h2>
    <p><strong>Ғылыми жоба:</strong> Суды көміртегі және ионсымалы әдіспен тазалау</p>
    <p><strong>Жетістік:</strong> Республикалық 1 орын</p>
    <p><strong>Оқушы:</strong> Сдамбек Айбек (№46 мектеп-лицей, Шымкент)</p>
    <iframe src="https://www.youtube.com/embed/TBTHvyG3N5g" allowfullscreen></iframe>
  </section>  <section id="contact">
    <h2>Байланыс</h2>
    <p>Телефон: +77002472742</p>
    <p>WhatsApp: <a href="https://wa.me/qr/FMIJ6XIJF5YPC1" target="_blank">Жазу</a></p>
    <form>
      <input type="text" placeholder="Аты-жөніңіз" required>
      <input type="email" placeholder="Электрондық пошта" required>
      <select required>
        <option value="">Курсты таңдаңыз</option>
        <option value="basic">Базалық курс</option>
        <option value="extended">Кеңейтілген курс</option>
        <option value="vip">VIP курс</option>
      </select>
      <textarea placeholder="Қосымша хабарлама"></textarea>
      <button type="submit">Тіркелу</button>
    </form>
  </section>  <footer>
    Жоба авторлары: Дүйсенханов Ұлан, Орынбек Диас (1504-12 тобы)
  </footer>  <script>
    function showSection(id) {
      document.querySelectorAll('section').forEach(function(sec) {
        sec.classList.remove('active');
      });
      document.getElementById(id).classList.add('active');
      window.scrollTo(0, 0);
    }
  </script></body>
</html>
