<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Escudo contra la tormenta</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            overflow-x: hidden; /* Evita el scroll horizontal */
        }
        body {
            font-family: Arial, sans-serif !important;
            background: none !important;
            color: white !important;
            text-align: center;
            overflow-x: hidden; /* Asegura que el body no permita desplazamiento horizontal */
        }
        .slideshow-container {
            position: relative;
            width: 100%;
            height: 75vh; /* Reducir la altura manteniendo el ancho al 100% */
            overflow: hidden;
        }
        .slide {
            position: absolute;
            width: 100%;
            height: 100%;
            background-size: cover; /* Asegurar que la imagen cubra todo sin espacios */
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }
        .active {
            opacity: 1;
        }
        .overlay {
            background: rgba(0, 0, 0, 0.4);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .content {
            position: relative;
            z-index: 2;
            width: 80%;
            display: flex;
            flex-direction: column;
            align-items: center; /* Centrar el contenido horizontalmente */
            justify-content: center; /* Centrar el contenido verticalmente */
            text-align: center; /* Asegurar que el texto esté centrado */
        }
        h1 {
            font-size: clamp(2rem, 5vw, 4rem); /* Tamaño de fuente responsivo */
            font-weight: bold;
            margin-bottom: 2%; /* Margen en porcentaje */
        }
        p {
            font-size: clamp(1rem, 2vw, 1.5rem); /* Tamaño de fuente responsivo */
            margin-top: 1.5%; /* Margen en porcentaje */
            margin-bottom: 1.5%; /* Margen en porcentaje */
        }
        /* Estilos específicos para los botones dentro del slideshow */
        .slideshow-container .cta-button {
            display: inline-block;
            margin-top: 3%; /* Margen en porcentaje */
            padding: 1% 2%; /* Padding en porcentaje */
            font-size: clamp(1rem, 1.5vw, 1.5rem); /* Tamaño de fuente responsivo */
            font-weight: normal;
            background: transparent !important;
            color: white !important;
            border: 2px solid red !important;
            border-radius: 35px;
            cursor: pointer;
            text-decoration: none;
            transition: background 0.3s ease-in-out, border 0.3s ease-in-out;
            width: auto; /* Ancho automático para ajustarse al contenido */
        }
        .slideshow-container .cta-button:hover {
            background: #14427c !important; /* Azul cuando el cursor pasa */
            color: white !important;
            border-color: #14427c !important;
        }
        .dots {
            position: absolute;
            bottom: 5%; /* Posición en porcentaje */
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 4%; /* Espacio entre puntos en porcentaje */
        }
        .dot {
            width: 1vw; /* Tamaño en porcentaje del ancho de la pantalla */
            height: 1vw; /* Tamaño en porcentaje del ancho de la pantalla */
            background: white;
            border-radius: 50%;
            cursor: pointer;
            opacity: 0.5;
        }
        .dot.active {
            opacity: 1;
            background: #14427c; /* Cambiar el color de los puntos activos a azul */
        }
        @media (max-width: 767px) {
            .slideshow-container {
                height: 60vh; /* Ajustar altura en móvil */
            }
            .dots {
                bottom: 3%; /* Posición en porcentaje en móvil */
            }
            h1 {
                font-size: clamp(1.5rem, 6vw, 2.5rem); /* Tamaño de fuente más pequeño en móvil */
                margin-bottom: 5%; /* Más espacio entre el título y el texto */
            }
            p {
                font-size: clamp(0.9rem, 3vw, 1.2rem); /* Tamaño de fuente más pequeño en móvil */
                margin-top: 3%; /* Más espacio entre párrafos */
                margin-bottom: 3%; /* Más espacio entre párrafos */
            }
            .slideshow-container .cta-button {
                font-size: clamp(0.9rem, 3vw, 1.2rem); /* Tamaño de fuente más pequeño en móvil */
                padding: 2% 4%; /* Padding más pequeño en móvil */
                margin-top: 5%; /* Más espacio entre el texto y el botón */
            }
            .dot {
                width: 3vw; /* Tamaño más grande en móvil */
                height: 3vw; /* Tamaño más grande en móvil */
            }
        }
        .slide:nth-child(1) { background-image: url('https://cdn.shopify.com/s/files/1/0674/6357/7826/files/LANDING_PAGE_TRIASO_SHUTTERS_2.jpg?v=1739329064'); }
        .slide:nth-child(2) { background-image: url('https://cdn.shopify.com/s/files/1/0674/6357/7826/files/LANDING_PAGE_TRIASO_SHUTTERS_1.jpg?v=1739296200'); }
        .slide:nth-child(3) { background-image: url('https://cdn.shopify.com/s/files/1/0674/6357/7826/files/66.jpg?v=1739387381'); }
    </style>
</head>
<body>
    <div class="slideshow-container">
        <div class="slide active">
            <div class="overlay"></div>
            <div class="content">
                <h1>TU ESCUDO CONTRA LA TORMENTA</h1>
                <p><strong>La seguridad de tu hogar comienza con nuestras persianas</strong></p>
                <p>Además de brindar protección contra los huracanes, ofrecen seguridad todo el año</p>
                <a href="#" class="cta-button">Configura tu persiana ideal</a>
            </div>
        </div>
        <div class="slide">
            <div class="overlay"></div>
            <div class="content">
                <h1>Seguridad Primero</h1>
                <p>La intensidad de huracanes ha aumentado un 23% en la última década tanto en el océano Pacífico y Atlántico, sin embargo en México no hay ninguna norma que exija regulaciones en las protecciones anti-ciclónicas. La falta de regulación no limita nuestra calidad: diseñamos persianas que realmente protegen.</p>
                <a href="#" class="cta-button">Conoce más...</a>
            </div>
        </div>
        <div class="slide">
            <div class="overlay"></div>
            <div class="content">
                <h1>Asegura la disponibilidad de tu persiana</h1>
                <p>Asegura tu lugar para adquirir tu persiana y garantiza la protección que necesitas para tu tranquilidad y la de tu familia.</p>
                <a href="#" class="cta-button">Solicita más información</a>
            </div>
        </div>
        <div class="dots"></div>
    </div>
    <script>
        let slides = document.querySelectorAll(".slide");
        let dotsContainer = document.querySelector(".dots");
        let currentSlide = 0;

        slides.forEach((_, index) => {
            let dot = document.createElement("div");
            dot.classList.add("dot");
            if (index === 0) dot.classList.add("active");
            dot.addEventListener("click", () => showSlide(index));
            dotsContainer.appendChild(dot);
        });

        function showSlide(index) {
            slides[currentSlide].classList.remove("active");
            dotsContainer.children[currentSlide].classList.remove("active");
            currentSlide = index;
            slides[currentSlide].classList.add("active");
            dotsContainer.children[currentSlide].classList.add("active");
        }

        setInterval(() => {
            let nextSlide = (currentSlide + 1) % slides.length;
            showSlide(nextSlide);
        }, 7000);
    </script>
</body>
</html>

<section class="info-section">
    <div class="container">
        <div class="info-box">
            <div class="image-container">
                <img src="https://cdn.shopify.com/s/files/1/0674/6357/7826/files/Vision.jpg?v=1739393193" alt="Visión">
            </div>
            <h2 class="title">Visión</h2>
            <p>En Onso, lideramos con innovación y calidad en persianas anti-ciclónicas, ofreciendo tecnología avanzada para la seguridad del hogar. Nos comprometemos con la excelencia en cada detalle, trabajando para convertir nuestra visión en realidad.</p>
            <div class="button-container">
                <a href="#" class="cta-button">Saber más...</a>
            </div>
        </div>
        <div class="info-box middle-box">
            <div class="image-container middle-image">
                <img src="https://cdn.shopify.com/s/files/1/0674/6357/7826/files/onso_logo1.jpg?v=1739393193" alt="Nosotros">
            </div>
            <h2 class="title">Nosotros</h2>
            <p>Con más de 25 años de experiencia, somos líderes en fabricación de trabajos con metal de alta calidad. La cuál nos ha convertido en expertos reconocidos en proyectos de soluciones. Comprometidos con soluciones de vanguardia y calidad superior.</p>
            <div class="button-container">
                <a href="#" class="cta-button">Saber más...</a>
            </div>
        </div>
        <div class="info-box">
            <div class="image-container">
                <img src="https://cdn.shopify.com/s/files/1/0674/6357/7826/files/MOBILE_LANDING_PAGE_TRIASO_SHUTTERS_1.jpg?v=1739393244" alt="Misión">
            </div>
            <h2 class="title">Misión</h2>
            <p>En Onso, nos destacamos por ofrecer soluciones avanzadas en protección residencial con nuestras persianas anti-ciclónicas. Comprometidos con la calidad excepcional, garantizamos seguridad y estilo en cada hogar que protegemos.</p>
            <div class="button-container">
                <a href="#" class="cta-button">Saber más...</a>
            </div>
        </div>
    </div>
</section>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Arial:wght@400;700&display=swap');
    
    .info-section {
        background: #f4f5f6;
        padding: 3% 8%; /* Más padding lateral para separar las secciones */
        text-align: center;
        font-family: 'Arial', sans-serif;
    }
    .container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        max-width: 1800px; /* Ancho máximo más grande para desktop */
        margin: auto;
        align-items: stretch;
        gap: 8%; /* Más espacio entre las secciones (en porcentaje) */
    }
    .info-box {
        width: 28%; /* Ancho en porcentaje (reducido para más espacio) */
        text-align: center;
        margin-bottom: 1%; /* Margen en porcentaje */
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 2%; /* Padding interno para separar contenido (en porcentaje) */
    }
    .middle-box {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .image-container {
        height: 20vh; /* Altura en porcentaje del viewport */
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 5%; /* Margen inferior para separar la imagen del título (en porcentaje) */
    }
    .image-container img {
        max-height: 100%;
        width: auto;
        max-width: 100%; /* Evitar que las imágenes se estiren */
        object-fit: cover; /* Mantener la proporción de la imagen */
    }
    .middle-image img {
        width: 30vw !important; /* Aumentar el tamaño de la imagen de "Nosotros" en desktop */
    }
    .info-box:nth-child(3) .image-container img {
        width: 12vw; /* Reducir el tamaño de la imagen de "Misión" en desktop */
    }
    .title {
        font-size: clamp(1.5rem, 2.8vw, 2.8rem); /* Tamaño de fuente responsivo */
        color: #4d4d4d;
        margin-bottom: 5%; /* Margen en porcentaje */
        min-height: 6vh; /* Altura mínima en porcentaje del viewport */
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .info-box p {
        font-size: clamp(0.9rem, 1.4vw, 1.4rem); /* Tamaño de fuente responsivo */
        color: #4d4d4d;
        text-align: justify;
        margin: 10 auto;
        max-width: 100%; /* Ancho máximo del texto para evitar que sea demasiado estrecho */
        flex-grow: 1;
        margin-bottom: 8%; /* Margen inferior para separar el texto del botón (en porcentaje) */
    }
    .button-container {
        margin-top: 5%; /* Margen en porcentaje */
    }
    .cta-button {
        display: inline-block;
        padding: 1.5% 3%; /* Padding en porcentaje */
        font-size: clamp(0.9rem, 1.2vw, 1.2rem); /* Tamaño de fuente responsivo */
        background: transparent;
        color: #4d4d4d;
        border: 2px solid #4d4d4d; /* Restaurar el contorno del botón */
        border-radius: 25px;
        cursor: pointer;
        text-decoration: none;
        white-space: nowrap; /* Evitar que el texto se divida en varias líneas */
        width: auto; /* Ancho automático para ajustarse al contenido */
        min-width: 150px; /* Ancho mínimo para evitar que sean demasiado pequeños */
    }
    .cta-button:hover {
        background: #4d4d4d;
        color: white;
    }
    @media (max-width: 1024px) {
        .info-box p {
            max-width: 100%; /* Ancho máximo del texto al 100% en desktop chico */
        }
    }
    @media (max-width: 768px) {
        .container {
            flex-direction: column;
            align-items: center;
            gap: 5%; /* Espacio entre las cajas en móvil (en porcentaje) */
        }
        .info-box {
            width: 95%; /* Ancho casi completo en móvil */
            text-align: center;
            margin-bottom: 5%; /* Margen en porcentaje */
            padding: 5%; /* Padding interno para móvil (en porcentaje) */
        }
        .image-container {
            height: 20vh; /* Altura automática en móvil */
            margin-bottom: 5%; /* Margen inferior para móvil (en porcentaje) */
        }
        .middle-image img {
            width: 50vw !important; /* Aumentar el tamaño de la imagen de "Nosotros" en móvil */
        }
        .info-box:nth-child(3) .image-container img {
            width: 40vw; /* Aumentar el tamaño de la imagen de "Misión" en móvil */
        }
        .info-box:first-child .image-container img {
            width: 50vw; /* Aumentar el tamaño de la imagen de "Visión" en móvil */
        }
        .image-container img {
            max-width: 100%; /* Asegurar que las imágenes no se salgan del contenedor */
        }
        .title {
            min-height: unset; /* Eliminar altura mínima en móvil */
            margin-bottom: 8%; /* Margen inferior para móvil (en porcentaje) */
        }
        .info-box p {
            margin-bottom: 10%; /* Margen inferior para móvil (en porcentaje) */
        }
        .cta-button {
            font-size: 0.9rem; /* Tamaño de fuente más pequeño en móvil */
            padding: 1.5% 3%; /* Padding en porcentaje para móvil */
            white-space: nowrap; /* Evitar que el texto se divida en varias líneas */
            min-width: 120px; /* Ancho mínimo para móvil */
        }
    }
</style>


<section class="persianas-section">
    <div class="tabs">
        <button class="tab-link active" onclick="changeTab(event, 'acordeon')">Persianas Acordeón</button>
        <button class="tab-link" onclick="changeTab(event, 'enrollables')">Persianas Enrollables</button>
        <button class="tab-link" onclick="changeTab(event, 'lona')">Lonas anti-ciclónicas</button>
    </div>

    <div id="acordeon" class="tab-content active">
        <div class="content-container">
            <img src="https://cdn.shopify.com/s/files/1/0674/6357/7826/files/86.jpg?v=1739404793" alt="Persiana Acordeón">
            <div class="text-content">
                <p style="font-size: clamp(0.9rem, 1.2vw, 1.2rem);"><strong>Protección robusta y compacta que integra seguridad superior, diseño práctico y funcionalidad adaptable, perfecta para cualquier espacio con nuestras persianas de acordeón anti-ciclónica.</strong></p>
                <div class="highlight-box blue">
                    <h3><strong>Protección y Comodidad con Plegado Fácil</strong></h3>
                    <p><strong>Nuestras persianas anti-ciclónicas están diseñadas para ser fáciles de plegar, brindando comodidad y eficiencia sin sacrificar seguridad.</strong></p>
                    <ul>
                        <li><strong>• Diseño compacto y funcional</strong></li>
                        <li><strong>• Fácil de almacenar y manejar</strong></li>
                        <li><strong>• Rápido y sencillo plegado</strong></li>
                    </ul>
                </div>
                <a href="#" class="cta-button">Saber más...</a>
            </div>
        </div>
    </div>

    <div id="enrollables" class="tab-content">
        <div class="section-description">
            <p style="font-size: clamp(0.9rem, 1.2vw, 1.2rem);"><strong>Las persianas más resistentes del mercado, creadas para ofrecer la máxima seguridad y comodidad en cualquier espacio.</strong></p>
        </div>
        <div class="content-container">
            <img src="https://cdn.shopify.com/s/files/1/0674/6357/7826/files/55.jpg?v=1739404879" alt="Persiana Enrollable">
            <div class="text-content">
                <div class="highlight-box red">
                    <h3><strong>Totalmente adaptadas a tu espacio</strong></h3>
                    <p><strong>Nuestras persianas anti-ciclónicas son fabricadas a la medida para ajustarse perfectamente al área donde serán instaladas, garantizando máxima protección para tu hogar.</strong></p>
                    <ul>
                        <li><strong>• Integradas en cancelería existente</strong></li>
                        <li><strong>• Con caja protectora personalizada</strong></li>
                        <li><strong>• Diseñadas para una instalación rápida y estética</strong></li>
                    </ul>
                </div>
                <a href="#" class="cta-button">Saber más...</a>
            </div>
        </div>
    </div>

    <div id="lona" class="tab-content">
        <div class="content-container">
            <img src="https://cdn.shopify.com/s/files/1/0674/6357/7826/files/116.jpg?v=1739404941" alt="Lona anti-ciclónica">
            <div class="text-content">
                <p style="font-size: clamp(0.9rem, 1.2vw, 1.2rem);"><strong>Lonas resistentes a huracanes, diseñadas para brindar una protección sólida y duradera a tu hogar, asegurando su seguridad frente a tormentas y condiciones climáticas extremas, sin comprometer la funcionalidad ni el diseño.</strong></p>
                <div class="highlight-box white">
                    <h3><strong>Resistencia y Protección para tu Hogar</strong></h3>
                    <p><strong>Nuestras persianas anti-ciclónicas ofrecen soluciones innovadoras para mantener tu hogar seguro y cómodo en todo momento.</strong></p>
                    <ul>
                        <li><strong>• Resistencia avanzada contra huracanes y tormentas</strong></li>
                        <li><strong>• Estructura robusta para condiciones extremas</strong></li>
                        <li><strong>• Materiales de alta durabilidad para una protección duradera</strong></li>
                        <li><strong>• Protección efectiva durante todo el año, sin importar el clima</strong></li>
                    </ul>
                </div>
                <a href="#" class="cta-button">Saber más...</a>
            </div>
        </div>
    </div>
</section>

<style>
    .persianas-section {
        background: #f4f5f6;
        padding: 30px 10px; /* Padding fijo */
        text-align: center;
        font-family: Arial, sans-serif;
        overflow-x: hidden;
    }
    .tabs {
        display: flex;
        justify-content: center;
        gap: 20%; /* Espacio fijo entre los títulos */
        margin-bottom: 70px; /* Margen fijo */
        flex-wrap: wrap;
    }
    .tab-link {
        background: none;
        border: none;
        font-size: clamp(1rem, 1.5vw, 1.5rem); /* Fuente responsiva */
        cursor: pointer;
        padding-bottom: 5px;
        transition: none;
        color: #393939;
        font-weight: normal;
        white-space: nowrap;
    }
    .tab-link.active {
        color: #14427c;
        border-bottom: 2px solid #14427c;
        font-weight: normal;
    }
    .tab-content {
        display: none;
        width: 100%;
        margin: auto;
    }
    .tab-content.active {
        display: block;
    }
    .content-container {
        display: flex;
        align-items: center;
        gap: 80px; /* Aumentar el espacio entre imagen y texto en desktop */
        position: relative;
        width: 100%;
        max-width: 1400px; /* Aumentar el ancho máximo del contenedor */
        margin: 0 auto;
    }
    .content-container img {
        width: 50%;
        max-width: 600px; /* Aumentar el tamaño máximo de la imagen */
        border-radius: 10px;
        z-index: 2;
        margin: 0 auto;
    }
    .text-content {
        width: 50%;
        text-align: justify;
        color: #393939;
        z-index: 2;
        padding-left: 20px; /* Aumentar el padding izquierdo */
    }
    .highlight-box {
        padding: 10px; /* Padding fijo */
        border-radius: 10px;
        margin-top: 10px; /* Margen fijo */
        color: #dfdfdf;
        background: #14427c;
        text-align: left;
    }
    .highlight-box.blue {
        background: #14427c;
    }
    .highlight-box.white {
        background: #ffffff;
    }
    .highlight-box.red {
        background: #ca1c1c;
    }
    .highlight-box h3 {
        color: white;
        font-size: clamp(1.2rem, 1.8vw, 1.8rem); /* Fuente responsiva */
        margin-bottom: 8px; /* Margen fijo */
    }
    .highlight-box p {
        font-size: clamp(0.9rem, 1.2vw, 1.2rem); /* Fuente responsiva */
        line-height: 1.2;
    }
    .highlight-box ul {
        list-style-type: disc;
        padding-left: 15px; /* Padding fijo */
        font-size: clamp(0.9rem, 1.2vw, 1.2rem); /* Fuente responsiva */
    }
    .highlight-box ul li {
        margin-bottom: 6px; /* Margen fijo */
    }
    .cta-button {
        display: block;
        margin: 50px auto 0; /* Margen fijo */
        padding: 8px 16px; /* Padding fijo */
        font-size: clamp(0.9rem, 1.2vw, 1.2rem); /* Fuente responsiva */
        border: 2px solid #4d4d4d;
        color: #4d4d4d;
        border-radius: 20px;
        text-decoration: none;
        transition: background 10s;
        background: #fff;
        width: fit-content;
    }
    .cta-button:hover {
        background: #4d4d4d;
        color: white;
    }
    .section-description {
        text-align: justify;
        margin: 10px auto; /* Margen fijo */
        max-width: 800px;
        font-size: clamp(0.9rem, 1.2vw, 1.2rem); /* Fuente responsiva */
        color: #393939;
    }
    @media (max-width: 768px) {
        .persianas-section {
            padding: 20px 20px; /* Padding fijo en móvil */
        }
        .tabs {
            gap: 7%; /* Espacio fijo en móvil */
            flex-wrap: nowrap;
            overflow-x: auto;
            justify-content: center;
            padding: 0 0px; /* Padding fijo en móvil */
        }
        .tab-link {
            font-size: 0.6rem; /* Tamaño fijo en móvil */
            white-space: nowrap;
            padding: 0 1px; /* Padding fijo en móvil */
        }
        .content-container {
            flex-direction: column;
            gap: 20px; /* Espacio fijo en móvil */
        }
        .content-container img {
            width: 100%; /* Ocupa todo el ancho en móvil */
            order: 1;
        }
        .text-content {
            width: 100%;
            padding-left: 0;
            order: 2;
        }
        .highlight-box {
            padding: 15px; /* Padding fijo en móvil */
        }
        .highlight-box h3 {
            font-size: 1rem; /* Tamaño fijo en móvil */
        }
        .highlight-box p {
            font-size: 0.8rem; /* Tamaño fijo en móvil */
        }
        .highlight-box ul {
            font-size: 0.8rem; /* Tamaño fijo en móvil */
        }
        .section-description {
            padding: 0 20px; /* Padding fijo en móvil */
            font-size: 0.8rem; /* Tamaño fijo en móvil */
        }
    }

    /* Estilos específicos para el highlight-box de la sección "Lonas anti-ciclónicas" */
    #lona .highlight-box.white {
        background: #ffffff;
    }
    #lona .highlight-box.white h3 {
        color: #000000;
    }
    #lona .highlight-box.white p,
    #lona .highlight-box.white ul,
    #lona .highlight-box.white ul li {
        color: #393939;
    }
</style>

<script>
    function changeTab(event, tabId) {
        document.querySelectorAll('.tab-content').forEach(tab => {
            tab.classList.remove('active');
        });
        document.querySelectorAll('.tab-link').forEach(tab => {
            tab.classList.remove('active');
        });
        document.getElementById(tabId).classList.add('active');
        event.currentTarget.classList.add('active');
    }
</script>
