# anvikshi.github.io
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Тестовый сайт</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
        header { background-color: #222; color: #fff; padding: 20px; }
        nav { background: #eee; padding: 10px 20px; }
        nav a { margin-right: 15px; color: #333; text-decoration: none; }
        nav a:hover { text-decoration: underline; }
        main { padding: 20px; }
        section { display: none; }
        section.active { display: block; }
    </style>
</head>
<body>
    <header>
        <h1>Добро пожаловать на эту скучную страницу!</h1>
    </header>
    <nav>
        <a href="#home" id="link-home">Главная</a>
        <a href="#about" id="link-about">О проекте</a>
    </nav>
    <main>
        <section id="home" class="active">
            <h2>Главная</h2>
            <p>Это стартовая страница для тестирования всякого.</p>
        </section>
        <section id="about">
            <h2>О проекте</h2>
            <p>Этот сайт создан для экспериментов и проверки всякого разного.</p>
        </section>
    </main>
    <script>
        // Простая навигация между разделами без перезагрузки страницы
        const sections = document.querySelectorAll('section');
        function showSection(id) {
            sections.forEach(sec => sec.classList.remove('active'));
            document.getElementById(id).classList.add('active');
        }
        window.addEventListener('hashchange', () => {
            const id = location.hash.substr(1) || 'home';
            if(document.getElementById(id)) showSection(id);
        });
        // Показать правильный раздел при загрузке
        window.addEventListener('DOMContentLoaded', () => {
            const id = location.hash.substr(1) || 'home';
            if(document.getElementById(id)) showSection(id);
        });
    </script>
    <!-- Yandex.Metrika counter -->
    <script type="text/javascript">
        (function(m,e,t,r,i,k,a){
            m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
            m[i].l=1*new Date();
            for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
            k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)
        })(window, document,'script','https://mc.yandex.ru/metrika/tag.js?id=103664696', 'ym');

        ym(103664696, 'init', {ssr:true, webvisor:true, clickmap:true, ecommerce:"dataLayer",         accurateTrackBounce:true, trackLinks:true});
    </script>
    <noscript><div><img src="https://mc.yandex.ru/watch/103664696" style="position:absolute; left:-9999px;" alt="" />    </div></noscript>
    <!-- /Yandex.Metrika counter -->
</body>
</html>
