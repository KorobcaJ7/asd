
# asd
ну тут сайт типа
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>STREET TICKETS — Афиша концертов</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <header class="header">
    <a class="logo" href="index.html">STREET<span>TICKETS</span></a>
    <nav class="nav">
      <a class="active" href="index.html">Главная</a>
      <a href="tickets.html">Билеты</a>
      <a href="lineup.html">Line-up</a>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div class="hero-noise"></div>
      <div class="hero-content">
        <p class="tag">главное событие сезона</p>
        <h1>Макс Корж<br><span>Большой street live</span></h1>
        <p class="hero-text">Концертная афиша с драйвом, городским ритмом и быстрым оформлением билетов.</p>
        <div class="hero-actions">
          <a class="btn primary" href="tickets.html?artist=korzh">Купить билет</a>
          <a class="btn ghost" href="#artists">Смотреть афишу</a>
        </div>
      </div>
      <div class="hero-card">
        <div class="poster poster-korzh">
          <span>MAX<br>KORZH</span>
        </div>
        <div class="concert-info">
          <p>Санкт-Петербург</p>
          <h3>СКА Арена</h3>
          <p>20 августа 2026 · 19:00</p>
        </div>
      </div>
    </section>

    <section class="section" id="artists">
      <div class="section-head">
        <p class="tag">афиша</p>
        <h2>Исполнители</h2>
      </div>
      <div class="artist-grid" id="artistGrid"></div>
    </section>

    <section class="banner-row">
      <div>
        <p class="tag">без лишнего</p>
        <h2>Выбери артиста, количество билетов и оформи заказ</h2>
      </div>
      <a class="btn primary" href="tickets.html">Перейти к покупке</a>
    </section>
  </main>

  <footer class="footer">
    <p>STREET TICKETS · городская афиша концертов</p>
  </footer>

  <script src="js/data.js"></script>
  <script src="js/main.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Line-up — STREET TICKETS</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <header class="header">
    <a class="logo" href="index.html">STREET<span>TICKETS</span></a>
    <nav class="nav">
      <a href="index.html">Главная</a>
      <a href="tickets.html">Билеты</a>
      <a class="active" href="lineup.html">Line-up</a>
    </nav>
  </header>

  <main>
    <section class="page-hero compact">
      <p class="tag">расписание</p>
      <h1>Line-up и города</h1>
      <p>Отфильтруй концерты по городу или найди исполнителя через поиск.</p>
    </section>

    <section class="tools">
      <input id="searchInput" type="search" placeholder="Поиск по исполнителю..." />
      <select id="cityFilter">
        <option value="all">Все города</option>
      </select>
    </section>

    <section class="lineup-list" id="lineupList"></section>
  </main>

  <footer class="footer">
    <p>STREET TICKETS · расписание событий</p>
  </footer>

  <script src="js/data.js"></script>
  <script src="js/lineup.js"></script>
</body>
</html>

# ФИНАЛ ОЧКА


<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Покупка билетов — STREET TICKETS</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <header class="header">
    <a class="logo" href="index.html">STREET<span>TICKETS</span></a>
    <nav class="nav">
      <a href="index.html">Главная</a>
      <a class="active" href="tickets.html">Билеты</a>
      <a href="lineup.html">Line-up</a>
    </nav>
  </header>

  <main>
    <section class="page-hero compact">
      <p class="tag">оформление</p>
      <h1>Покупка билета</h1>
      <p>Выбери концерт, сектор и количество билетов. Сумма считается автоматически.</p>
    </section>

    <section class="ticket-layout">
      <form class="ticket-form" id="ticketForm">
        <label>
          Исполнитель
          <select id="artistSelect"></select>
        </label>

        <label>
          Тип билета
          <select id="ticketType">
            <option value="fan">Фан-зона</option>
            <option value="dance">Танцпол</option>
            <option value="vip">VIP</option>
          </select>
        </label>

        <label>
          Количество
          <input id="ticketCount" type="number" min="1" max="10" value="1" />
        </label>

        <label>
          Имя покупателя
          <input id="buyerName" type="text" placeholder="Например: Даниил" required />
        </label>

        <label>
          Телефон
          <input id="buyerPhone" type="tel" placeholder="+7 999 000-00-00" required />
        </label>

        <button class="btn primary full" type="submit">Оформить заказ</button>
      </form>

      <aside class="order-card">
        <p class="tag">итог</p>
        <h2 id="orderArtist">Макс Корж</h2>
        <p id="orderDetails">Санкт-Петербург · СКА Арена</p>
        <div class="price-lines">
          <div><span>Цена за билет</span><strong id="singlePrice">4500 ₽</strong></div>
          <div><span>Количество</span><strong id="countText">1</strong></div>
          <div class="total"><span>Общая сумма</span><strong id="totalPrice">4500 ₽</strong></div>
        </div>
      </aside>
    </section>
  </main>

  <div class="popup" id="successPopup">
    <div class="popup-box">
      <button class="popup-close" id="closePopup">×</button>
      <p class="tag">готово</p>
      <h2>Покупка успешна!</h2>
      <p id="popupText">Ваш билет оформлен.</p>
      <a class="btn primary" href="lineup.html">Посмотреть line-up</a>
    </div>
  </div>

  <footer class="footer">
    <p>STREET TICKETS · оформление билетов</p>
  </footer>

  <script src="js/data.js"></script>
  <script src="js/tickets.js"></script>
</body>
</html>
