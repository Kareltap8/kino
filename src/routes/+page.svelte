<script>
	import '$lib/images/1.jpg';

</script>

<svelte:head>
	<title>Кинотеатр</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<style>
    :root {
    --primary-color: rgb(155, 213, 252);
    --secodary-color: rgb(47, 241, 255);
}

* {
    box-sizing:  border-box;
}

main {
    display: flex;
    flex-wrap: wrap;
}

body{
    background-color:  var(--primary-color);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}

header {
    padding: 10px;
    display: flex;
    justify-content: flex-end;
    background-color: var(--secodary-color);
}

.search {
    background-color: transparent;
    border: 2px solid var(--primary-color);
    border-radius: 50px;
    font-family: inherit;
    font-size: 14px;
    padding: 20px 10px;
}

.search::placeholder {
    color: wheat;
}

.search.search:focus{
    outline: none;
    background-color: white;
}

.movie {
    width: 300px;
	height: 500px;
    margin: 10px;
    background-color: var(--secodary-color);
    box-shadow: 0 4px 5px rgba(0, 0, 0, 0.2);
    position: relative;
    overflow: hidden;
    border-radius: 3px;
}

.movie img{
    width: 100%;
}

.movie-info {
    color: black;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 30px 30px;
    letter-spacing: 0.5px;
}

.movie-info h3{
    margin-top: 0;
}

.movie-info span{
    background-color: var(--primary-color);
    padding: 25px 5px;
    border-radius: 3px;
    font-weight: bold;
}

.movie-info span.green{
    color: rgb(255, 255, 255);
}

.overview {
    background-color: white;
    padding: 20px;
    position: absolute;
    left: 0;
    bottom: 0;
    right: 0;
    max-width: 100%;
    transform: translateY(101%);
    transition: transform 0.3s ease-in;
}

.movie:hover .overview{
    transform: translateY(0)
}
</style>

<main id="main">
    <div class="movie" id="movie">
        <div class="movie-info" id="MovieInfoDiv">
            <h3 id="MovieTitle">Шерлок Холмс</h3>
            <span class="green">9.8</span>
        </div>
		<img src="https://www.timeout.ru/wp-content/uploads/kpposters/420923.jpg" alt="">
        <div class="overview">
            <h3 id="Description">Величайший в истории сыщик Шерлок Холмс вместе со своим верным соратником Ватсоном вступают в схватку, требующую нешуточной физической и умственной подготовки, ведь их враг представляет угрозу для всего Лондона.</h3>
        </div>
    </div>
	<div class="movie" id="movie">
        <div class="movie-info" id="MovieInfoDiv">
            <h3 id="MovieTitle">Шрек</h3>
            <span class="green">10.0</span>
        </div>
		<img src="https://i.pinimg.com/originals/7c/d7/9b/7cd79b2de286ef71bf61e43d6ed9eab2.jpg" alt="">
        <div class="overview">
            <h3 id="Description">Жил да был в сказочном государстве большой зеленый великан по имени Шрэк. Жил он в гордом одиночестве в лесу, на болоте, которое считал своим. Но однажды злобный коротышка лорд Фаркуад, безжалостно согнал на Шрэково болото всех сказочных обитателей. Но лорд Фаркуад пообещал вернуть Шрэку болото, если великан добудет ему прекрасную принцессу Фиону, которая томится в неприступной башне, охраняемой огнедышащим драконом.</h3>
        </div>
    </div>
    <div class="movie" id="movie">
        <div class="movie-info" id="MovieInfoDiv">
            <h3 id="MovieTitle">Убить Билла</h3>
            <span class="green">8.0</span>
        </div>
		<img src="https://images.justwatch.com/poster/14214599/s718/kill-bill-vol-1.%7Bformat%7D" alt="">
        <div class="overview">
            <h3 id="Description">В беременную наёмную убийцу по кличке Чёрная Мамба во время бракосочетания стреляет человек по имени Билл. Но голова у женщины оказалась крепкой — пролежав четыре года в коме, бывшая невеста приходит в себя. Она горит желанием найти предателей. Теперь только безжалостная месть успокоит сердце Чёрной Мамбы, и она начинает по очереди убивать членов банды Билла, решив оставить главаря напоследок. </h3>
        </div>
    </div>
	<div class="movie" id="movie">
        <div class="movie-info" id="MovieInfoDiv">
            <h3 id="MovieTitle">Сумерки</h3>
            <span class="green">7.8</span>
        </div>
		<img src="https://abrakadabra.fun/uploads/posts/2021-11/1636781874_1-abrakadabra-fun-p-sumerki-poster-1.jpg" alt="">
        <div class="overview">
            <h3 id="Description">Семнадцатилетняя девушка Белла переезжает к отцу в небольшой городок Форкс. Она влюбляется в загадочного одноклассника, который, как оказалось, происходит из семьи вампиров, отказавшихся от нападений на людей. Влюбиться в вампира. Это страшно? Это романтично, это прекрасно и мучительно, но это не может кончиться добром, особенно в вечном противостоянии вампирских кланов, где малейшее отличие от окружающих уже превращает вас во врага.</h3>
        </div>
    </div>
	<div class="movie" id="movie">
        <div class="movie-info" id="MovieInfoDiv">
            <h3 id="MovieTitle">Клаустрофобы</h3>
            <span class="green">9.0</span>
        </div>
		<img src="https://www.kinonews.ru/insimgs/2018/poster/poster83137_1.jpg" alt="">
        <div class="overview">
            <h3 id="Description">Получив приглашение сыграть в квест, победитель которого получит денежное вознаграждение, шестеро прежде незнакомых между собой людей решают испытать удачу. Но вскоре становится очевидно, что их выбрали для игры не случайно, задания не такие безобидные, а ставка в игре — их собственные жизни.</h3>
        </div>
    </div>
    <div class="movie" id="movie">
        <div class="movie-info" id="MovieInfoDiv">
            <h3 id="MovieTitle">Почему он?</h3>
            <span class="green">6.2</span>
        </div>
		<img src="https://media.filmz.ru/photos/full/filmz.ru_f_228954.jpg" alt="">
        <div class="overview">
            <h3 id="Description">Глава семейства вступает в противостояние с молодым и богатым парнем своей дочери.</h3>
        </div>
    </div>
</main>
