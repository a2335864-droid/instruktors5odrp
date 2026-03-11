<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Инструктора ОДРП №5</title>

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">

<!-- Иконки Font Awesome 6 -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Montserrat', sans-serif;
}

body{
background: radial-gradient(circle at top,#6b4cff,#1d103b 60%,#090012);
color:white;
min-height:100vh;
}

/* меню — навигация */
nav{
display:flex;
justify-content:center;
gap:20px;
padding:30px;
flex-wrap: wrap;
}

nav a{
text-decoration:none;
color:white;
padding:12px 24px;
border-radius:30px;
background:rgba(255,255,255,0.08);
border:1px solid rgba(255,255,255,0.2);
transition:0.3s ease;
display:flex;
align-items:center;
gap:8px;
}

/* Игровое свечение кнопок при наведении */
nav a:hover {
    background: #6be7ff;
    color: #001b22;
    box-shadow: 0 0 15px rgba(107, 231, 255, 0.8), 
                0 0 30px rgba(107, 231, 255, 0.6), 
                0 0 45px rgba(107, 231, 255, 0.4);
    transform: translateY(-3px);
}

/* заголовок */
header{
text-align:center;
margin-top:40px;
}

header h1{
font-size:48px;
font-weight:700;
}

/* контейнер */
.container{
max-width:900px;
margin:auto;
padding:20px;
}

/* блоки */
.block{
background:rgba(255,255,255,0.06);
border:1px solid rgba(255,255,255,0.15);
border-radius:18px;
padding:25px;
margin-top:20px;
backdrop-filter:blur(12px);
transition:0.3s ease;
}

.block.highlight{
border:1px solid #6be7ff;
background:rgba(107,231,255,0.12);
}

/* заголовок раздела */
.section-title{
text-align:center;
font-size:34px;
margin:70px 0 30px 0;
display:flex;
justify-content:center;
align-items:center;
gap:10px;
}

/* карточки тестов */
.cards{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:25px;
}

.card{
width:260px;
padding:28px;
border-radius:18px;
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.15);
transition:0.3s ease;
text-align:center;
}

.card i{
font-size:28px;
margin-bottom:10px;
color:#6be7ff;
}

.card:hover{
transform:translateY(-6px);
background:rgba(107,231,255,0.15);
border:1px solid #6be7ff;
box-shadow: 0 0 15px rgba(107, 231, 255, 0.8),
            0 0 30px rgba(107, 231, 255, 0.6),
            0 0 45px rgba(107, 231, 255, 0.4);
}

.card a{
display:inline-block;
margin-top:12px;
text-decoration:none;
color:#6be7ff;
font-weight:600;
transition:0.3s ease;
}

.card a:hover {
    color: #ffffff;
    transform: scale(1.1);
    text-shadow: 0 0 8px rgba(107, 231, 255, 0.7);
}

/* НОВЫЙ РАЗДЕЛ - Таблица наборщиков */
.section-title.large {
font-size: 42px;
margin: 90px 0 40px 0;
text-shadow: 0 0 10px rgba(107, 231, 255, 0.5);
}

.section-title.large i {
color: #6be7ff;
filter: drop-shadow(0 0 8px rgba(107, 231, 255, 0.7));
}

.table-block {
background: linear-gradient(145deg, rgba(107, 71, 255, 0.15), rgba(44, 24, 128, 0.25));
border: 2px solid rgba(107, 231, 255, 0.3);
border-radius: 30px;
padding: 40px;
margin: 30px 0 50px 0;
backdrop-filter: blur(15px);
transition: all 0.4s ease;
position: relative;
overflow: hidden;
}

.table-block::before {
content: '';
position: absolute;
top: -50%;
left: -50%;
width: 200%;
height: 200%;
background: radial-gradient(circle, rgba(107, 231, 255, 0.1) 0%, transparent 70%);
animation: rotate 20s linear infinite;
z-index: 0;
}

@keyframes rotate {
from { transform: rotate(0deg); }
to { transform: rotate(360deg); }
}

.table-block:hover {
border-color: #6be7ff;
box-shadow: 0 0 30px rgba(107, 231, 255, 0.4),
            0 0 60px rgba(107, 71, 255, 0.3);
transform: translateY(-5px);
}

.table-content {
position: relative;
z-index: 1;
display: flex;
align-items: center;
gap: 40px;
}

.table-icon {
font-size: 80px;
color: #6be7ff;
filter: drop-shadow(0 0 15px rgba(107, 231, 255, 0.8));
animation: pulse 3s ease-in-out infinite;
}

@keyframes pulse {
0% { transform: scale(1); filter: drop-shadow(0 0 15px rgba(107, 231, 255, 0.8)); }
50% { transform: scale(1.1); filter: drop-shadow(0 0 30px rgba(107, 231, 255, 1)); }
100% { transform: scale(1); filter: drop-shadow(0 0 15px rgba(107, 231, 255, 0.8)); }
}

.table-text {
flex: 1;
}

.table-text h3 {
font-size: 36px;
margin-bottom: 15px;
background: linear-gradient(135deg, #ffffff, #6be7ff);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
font-weight: 700;
}

.table-text p {
font-size: 18px;
line-height: 1.6;
color: rgba(255, 255, 255, 0.9);
margin-bottom: 25px;
}

.table-btn {
display: inline-flex;
align-items: center;
gap: 12px;
background: linear-gradient(135deg, #6b4cff, #3a2b8f);
color: white;
text-decoration: none;
padding: 15px 35px;
border-radius: 50px;
font-weight: 600;
font-size: 18px;
border: 1px solid rgba(107, 231, 255, 0.5);
transition: all 0.3s ease;
box-shadow: 0 0 20px rgba(107, 231, 255, 0.3);
}

.table-btn:hover {
background: linear-gradient(135deg, #7b5cff, #4b3b9f);
transform: translateY(-3px) scale(1.05);
box-shadow: 0 0 30px rgba(107, 231, 255, 0.6),
            0 0 60px rgba(107, 71, 255, 0.4);
border-color: #6be7ff;
gap: 20px;
}

.table-btn i {
font-size: 20px;
transition: transform 0.3s ease;
}

.table-btn:hover i {
transform: translateX(5px) rotate(90deg);
}

/* Адаптация для мобильных */
@media (max-width: 768px) {
.table-content {
flex-direction: column;
text-align: center;
gap: 20px;
}

.table-icon {
font-size: 60px;
}

.table-text h3 {
font-size: 28px;
}

.table-btn {
padding: 12px 25px;
font-size: 16px;
}
}

/* футер */
footer{
margin-top:90px;
text-align:center;
padding:40px;
background:rgba(0,0,0,0.35);
}

footer h2{
color:#B197FC;
transition:0.4s ease;
}

footer p{
color:#B197FC;
transition:0.4s ease;
}

</style>
</head>

<body>

<nav>
    <a href="#"><i class="fa-solid fa-house"></i> Главная</a>

    <a href="https://docs.google.com/document/d/1GPLUaJWW2Ma8nIZwG6jXK4-g2AAGqrFYDQT25bCjM48/edit?tab=t.0#heading=h.twssduvwxag" target="_blank">
        <i class="fa-solid fa-book-open"></i> Методичка Инструкторов
    </a>

    <a href="https://docs.google.com/document/d/1GPLUaJWW2Ma8nIZwG6jXK4-g2AAGqrFYDQT25bCjM48/edit?tab=t.0#heading=h.9k9acbm4k0le" target="_blank">
        <i class="fa-solid fa-book"></i> Обучение кадетов
    </a>

    <!-- Новая кнопка "Таблица Инструкторов" с иконкой сетки/таблицы -->
    <a href="https://odrp5instructors.netlify.app/" target="_blank">
        <i class="fa-solid fa-table"></i> Таблица Инструкторов
    </a>
</nav>

<header>
<h1><i class="fa-solid fa-user-graduate"></i> Инструктора ОДРП №5</h1>
</header>

<div class="container">

<div class="block">
Инструктор - это Администратор, ответственный за проведение обучения Кадетам и помощи при необходимости.
</div>

<div class="block">
Цель Инструкторов - обучение новых кадров, проведение тестов для повышения и поддержка знаний у кадетов 5 сервера.
</div>

<div class="block highlight">
Помните! Инструктора - это ответственные за кадетов Администраторы. Вся ответственность насчёт знаний интернов - на вас! Старайтесь обучать кадетов не поверхостно, а углубленно.
</div>

<!-- НОВЫЙ РАЗДЕЛ: Таблица Инструкторов -->
<h2 class="section-title large">
    <i class="fa-solid fa-crown"></i> Таблица Инструкторов
    <i class="fa-solid fa-crown"></i>
</h2>

<div class="table-block">
    <div class="table-content">
        <div class="table-icon">
            <i class="fa-solid fa-table-cells-large"></i>
        </div>
        <div class="table-text">
            <h3>Таблица Инструкторов</h3>
            <p>с различными возможностями и информацией о Администраторах внутри отдела.</p>
            
            <a href="https://odrp5instructors.netlify.app/" class="table-btn" target="_blank">
                <i class="fa-solid fa-arrow-right-to-bracket"></i>
                ПЕРЕЙТИ К ТАБЛИЦЕ
                <i class="fa-solid fa-table"></i>
            </a>
        </div>
    </div>
</div>

<h2 class="section-title">
<i class="fa-solid fa-clipboard-check"></i> Тесты
</h2>

<div class="cards">

<div class="card">
<i class="fa-solid fa-file-circle-check"></i>
<h3>Тест №1</h3>
<a href="https://docs.google.com/forms/d/e/1FAIpQLSeEMZcwY5Y--6v4YsEn29P183xmQyZsiCueRZJRKWI2CjxIiA/viewform" target="_blank">Пройти</a>
</div>

<div class="card">
<i class="fa-solid fa-file-pen"></i>
<h3>Тест №2</h3>
<a href="https://docs.google.com/forms/d/e/1FAIpQLSfrAUqgZDG_API64myLkaIK9Doi_Jx_RXsfC2tTUMBOCXxDAg/viewform" target="_blank">Пройти</a>
</div>

<div class="card">
<i class="fa-solid fa-list-check"></i>
<h3>Тест №3</h3>
<a href="https://docs.google.com/forms/d/e/1FAIpQLScwhcdcYzW10jNkHrez3uUvZL481dZ5H1eQKeuzu_OxyZXu_A/viewform" target="_blank">Пройти</a>
</div>

</div>

</div>

<footer>
<h2>Инструктора 5 сервера</h2>
<p>by Алекс Уэйнрайт</p>
</footer>

</body>
</html>
