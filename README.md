<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proyecto de Acuaponía</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f9;
        }

        header {
            background: #1E3A5F;
            color: white;
            padding: 2rem 0;
            text-align: center;
        }

        nav {
            display: flex;
            justify-content: center;
            background: #144272;
            padding: 1rem 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 0.75rem 1.5rem;
            margin: 0 1rem;
            transition: background 0.3s, transform 0.2s;
        }

        nav a:hover {
            background: #1E3A5F;
            transform: translateY(-3px);
        }

        .container {
            padding: 3rem 1.5rem;
            max-width: 1200px;
            margin: auto;
        }

        .content {
            text-align: center;
        }

        .info-section {
            margin-top: 2rem;
            text-align: left;
        }

        .info-section h3 {
            color: #144272;
        }

        .slider {
            position: relative;
            max-width: 800px;
            margin: 2rem auto;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .slides {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .slide {
            min-width: 100%;
            box-sizing: border-box;
        }

        .slide img {
            width: 100%;
            display: block;
        }

        .slider-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 1rem;
            cursor: pointer;
            z-index: 10;
        }

        .prev {
            left: 10px;
        }

        .next {
            right: 10px;
        }

        footer {
            text-align: center;
            padding: 1.5rem;
            background: #144272;
            color: white;
        }
    </style>
</head>

<body>
    <header>
        <h1>Proyecto de Acuaponía</h1>
    </header>

    <nav>
        <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería</a>
        <a href="preguntas%20frecuentes.html">Preguntas Frecuentes</a>
        <a href="contacto.html">Contacto</a>
        <a href="instalación.html">instalación</a>
        <a href="imformación2doy4to.html">imformación 2do y 4to</a>
        <a href="RECURSOS%20ADICIONALES.html">Recursos Adicionales</a>
    </nav>

    <div class="container">
        <div class="content" id="inicio">
            <h2>Bienvenido al Proyecto de Acuaponía</h2>
            <p>Descubre cómo la acuaponía fusiona la acuicultura y la hidroponía para crear un sistema de cultivo eficiente y sostenible.</p>
        </div>

        <!-- Información Crucial sobre la Acuaponía -->
        <div class="info-section">
            <h3>¿Qué es la Acuaponía?</h3>
            <p>La acuaponía es un sistema sostenible que combina la cría de peces (acuicultura) con el cultivo de plantas sin tierra (hidroponía). Los desechos de los peces proporcionan nutrientes esenciales para las plantas, mientras que las plantas filtran y purifican el agua que regresa a los peces.</p>

            <h3>Beneficios de la Acuaponía:</h3>
            <ul>
                <li>Ahorro significativo de agua en comparación con la agricultura tradicional.</li>
                <li>Producción simultánea de vegetales y proteínas (peces).</li>
                <li>Uso reducido de fertilizantes y productos químicos.</li>
                <li>Ideal para áreas urbanas o con recursos hídricos limitados.</li>
            </ul>

            <h3>¿Cómo Funciona?</h3>
            <p>El sistema de acuaponía sigue un ciclo cerrado:</p>
            <ol>
                <li>Los peces producen desechos ricos en amoníaco.</li>
                <li>Bacterias beneficiosas convierten el amoníaco en nitratos, un fertilizante natural para las plantas.</li>
                <li>Las plantas absorben los nutrientes y limpian el agua.</li>
                <li>El agua limpia regresa al tanque de los peces, completando el ciclo.</li>
            </ol>
        </div>

        <!-- Slider de Imágenes Locales -->
        <div class="slider">
            <div class="slides" id="slides">
                <div class="slide"><img src="imagen%201.jpg" alt="Imagen 1"></div>
                <div class="slide"><img src="imagen%204.jpg" alt="Imagen 2"></div>
                <div class="slide"><img src="imagen%203.jpg" alt="Imagen 3"></div> 
                <div class="slide"><img src="imagen%208.jpg" alt="Imagen 3"></div>
            </div>
            <button class="slider-btn prev" onclick="moverSlide(-1)">❮</button>
            <button class="slider-btn next" onclick="moverSlide(1)">❯</button>
        </div>

    </div>

    <footer>
        &copy; 2025 Proyecto de Acuaponía. Todos los derechos reservados.
    </footer>
 
    <script>
        function navigateTo(url) {
            let water = document.querySelector('.water-transition');
            gsap.to(water, { height: '100%', duration: 1, ease: 'power2.out', onComplete: () => window.location.href = url });
        }

        window.onload = function () {
            let water = document.querySelector('.water-transition');
            gsap.to(water, { height: '0%', duration: 1, ease: 'power2.in' });
            setInterval(() => moverSlide(1), 5000);
        }

        let index = 0;
        function moverSlide(n) {
            let slides = document.querySelectorAll('.slide');
            index = (index + n + slides.length) % slides.length;
            document.getElementById('slides').style.transform = `translateX(${-index * 100}%)`;
        }
    </script>
   
</body>
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galería - Proyecto de Acuaponía</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
        }

        header, footer {
            background: #1E3A5F;
            color: white;
            padding: 2rem 0;
        }

        nav {
            background: #144272;
            padding: 1rem 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 2rem;
        }

        .gallery img {
            width: 100%;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>

<body>
    <header>
        <h1>Galería del Proyecto de Acuaponía</h1>
    </header>

    <nav>
       <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería</a>
        <a href="preguntas%20frecuentes.html">Preguntas Frecuentes</a>
        <a href="contacto.html">Contacto</a>
        <a href="instalación.html">instalación</a>
        <a href="imformaci%C3%B3n2doy4to.html">imformación 2do y 4to</a>
         <a href="RECURSOS%20ADICIONALES.html">Recursos Adicionales</a>
    </nav>

    <div class="gallery">
        <img src="imagen%201.jpg" alt="Acuaponía 1">
        <img src="imagen%202.jpg" alt="Acuaponía 2">
        <img src="imagen%203.jpg" alt="Acuaponía 3">
        <img src="imagen%204.jpg" alt="Acuaponía 4">
        <img src="imagen%205.jpg" alt="Acuaponía 5">
        <img src="imagen%207.jpg" alt="Acuaponía 6">
        <img src="imagen%208.jpg" alt="Acuaponía 7">
    </div>

    <footer>&copy; 2025 Proyecto de Acuaponía. Todos los derechos reservados.</footer>
</body>
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preguntas Frecuentes - Proyecto de Acuaponía</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f9;
            color: #333;
        }

        header, footer {
            background: #1E3A5F;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        nav {
            background: #144272;
            text-align: center;
            padding: 1rem 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }

        .faq {
            max-width: 800px;
            margin: auto;
            padding: 2rem;
        }

        .faq h3 {
            color: #144272;
        }
    </style>
</head>

<body>
    <header>
        <h1>Preguntas Frecuentes</h1>
    </header>

    <nav>
        <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería</a>
        <a href="preguntas.html">Preguntas Frecuentes</a>
        <a href="contacto.html">Contacto</a>
        <a href="instalación.html">instalación</a>
        <a href="imformaci%C3%B3n2doy4to.html">imformación 2do y 4to</a>
        <a href="RECURSOS%20ADICIONALES.html">Recursos Adicionales</a>
    </nav>

    <div class="faq">
        <h3>¿Qué tipo de peces se pueden usar en la acuaponía?</h3>
        <p>Se pueden utilizar peces como tilapia, trucha y bagre debido a su resistencia y adaptabilidad.</p>

        <h3>¿Qué plantas crecen mejor en un sistema acuapónico?</h3>
        <p>Lechuga, albahaca, espinaca, fresas y tomates son opciones ideales por su demanda nutricional moderada.</p>

        <h3>¿Es difícil mantener un sistema de acuaponía?</h3>
        <p>No, una vez establecido, solo requiere monitorear el pH, la temperatura y la calidad del agua.</p>
    </div>

    <footer>&copy; 2025 Proyecto de Acuaponía. Todos los derechos reservados.</footer>
</body>
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preguntas Frecuentes - Proyecto de Acuaponía</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f9;
            color: #333;
        }

        header, footer {
            background: #1E3A5F;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        nav {
            background: #144272;
            text-align: center;
            padding: 1rem 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }

        .faq {
            max-width: 800px;
            margin: auto;
            padding: 2rem;
        }

        .faq h3 {
            color: #144272;
        }
    </style>
</head>

<body>
    <header>
        <h1>Instalación</h1>
    </header>

    <nav>
        <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería</a>
        <a href="preguntas%20frecuentes.html">Preguntas Frecuentes</a>
        <a href="contacto.html">Contacto</a>
        <a href="instalación.html">instalación</a>
        <a href="imformaci%C3%B3n2doy4to.html">imformación 2do y 4to</a>
         <a href="RECURSOS%20ADICIONALES.html">Recursos Adicionales</a>
    </nav>

    <div class="faq">
        <h3>1. PLANIFICACIÓN DEL SISTEMA</h3>
        <img src="imagen%208.jpg" alt="1">
        <p>-define el tipo de sistema 
           -Escoge los peces y plantas
           -Calcula el tamaño</p>

        <h3>2. RECOLECCIÓN DE MATERIALES</h3>
        <img src="imagen%204.jpg" alt="2">      
        <p>-tanque para peces(plástico grado alimenticio)
           -Bomba de agua(para recircular)
           -bomba de aire y difusores
           -Cama de cultivo
           -Biofiltro
           -Tuberias
           -Sustrato inerte</p>

        <h3>3. Instalación de sistema</h3>
        <img src="imagen%203.jpg" alt="3">
        <p>Ubicación: lugar con buena iluninación natural o artificial
           Tanque de peces: colocca en el punto mas bajo
           Cama de cultivo: sitúala mas alta que el tanque
           sistema de recirculación
           Aireación: coloca difusores de aire en el tanque y en el lecho si es DWC</p>
              
        <h3>4. Ciclo de nitrógeno</h3>
        <img src="imagen%201.jpg" alt="4">
        <p>-No pongas peces al principio
           -Añade una fuente de amoníaco
           -Espera 3-6 semanas hasta que se estabilicen bacterias nitrificantes
           -Usa kits para medir pH, amoníaco, nitritos y nitratos</p>
         
        <h3>5. Introducción de peces y plantas</h3>
        <img src="imagen%207.jpg" alt="5">
        <p>Una vez estabilizado: Introduce los peces gradualmente, planta hortalizas o plantas de rapído crecimiento</p>
        
        <h3>6. Instalación del sistema</h3>
        <img src="imagen%202.jpg" alt="6">
        <p>-Alimentar a los peces 1-2 veces al día
           -Monitorerar el agua: pH (6.8-7.2) temperatura, niveles de amoníaco y oxigeno.
           -Podar plantas, cosechar, limpiar filtros si los hay.
           -Reponer agua por evaporación </p>
        
    </div>
     
    
    <footer>&copy; 2025 Proyecto de Acuaponía. Todos los derechos reservados.</footer>
</body>
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preguntas Frecuentes - Proyecto de Acuaponía</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f9;
            color: #333;
        }

        header, footer {
            background: #1E3A5F;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        nav {
            background: #144272;
            text-align: center;
            padding: 1rem 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }

        .faq {
            max-width: 800px;
            margin: auto;
            padding: 2rem;
        }

        .faq h3 {
            color: #144272;
        }
    </style>
</head>

<body>
    <header>
        <h1>Imformación de 2do yb 4to</h1>
    </header>

    <nav>
       <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería</a>
        <a href="preguntas.html">Preguntas Frecuentes</a>
        <a href="contacto.html">Contacto</a>
        <a href="instalación.html">instalación</a>
        <a href="imformaci%C3%B3n2doy4to.html">imformación 2do y 4to</a>
        
    </nav>

    <div class="faq">
        <h3>1. PLANIFICACIÓN DEL SISTEMA</h3>
        <p>-define el tipo de sistema 
           -Escoge los peces y plantas
           -Calcula el tamaño</p>

        <h3>2. RECOLECCIÓN DE MATERIALES</h3>
        <p>-tanque para peces(plástico grado alimenticio)
           -Bomba de agua(para recircular)
           -bomba de aire y difusores
           -Cama de cultivo
           -Biofiltro
           -Tuberias
           -Sustrato inerte</p>

        <h3>3. Instalación de sistema</h3>
        <p>Ubicación: lugar con buena iluninación natural o artificial
           Tanque de peces: colocca en el punto mas bajo
           Cama de cultivo: sitúala mas alta que el tanque
           sistema de recirculación
           Aireación: coloca difusores de aire en el tanque y en el lecho si es DWC</p>
              
        <h3>4. Ciclo de nitrógeno</h3>
        <p>-No pongas peces al principio
           -Añade una fuente de amoníaco
           -Espera 3-6 semanas hasta que se estabilicen bacterias nitrificantes
           -Usa kits para medir pH, amoníaco, nitritos y nitratos</p>
         
        <h3>5. Introducción de peces y plantas</h3>
        <p>Una vez estabilizado: Introduce los peces gradualmente, planta hortalizas o plantas de rapído crecimiento</p>
        
        <h3>6. Instalación del sistema</h3>
        <p>-Alimentar a los peces 1-2 veces al día
           -Monitorerar el agua: pH (6.8-7.2) temperatura, niveles de amoníaco y oxigeno.
           -Podar plantas, cosechar, limpiar filtros si los hay.
           -Reponer agua por evaporación </p>
        
    </div>
     <div class="imagenes">
        <img src="1.jpg.jpg" alt="1">
        <img src="2.jpg" alt="2">
        <img src="3.jpg" alt="3">
         <img src="oip.jpg" alt="4">
        <img src="OIP 2.jpg" alt="5">
        <img src="OIP 3.jpg" alt="6">
    </div>

    <footer>&copy; 2025 Proyecto de Acuaponía. Todos los derechos reservados.</footer>
</body>
<!-- contactos.html -->
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contactos - Proyecto de Acuaponía</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
        }

        header, footer {
            background: #1E3A5F;
            color: white;
            padding: 2rem 0;
        }

        nav {
            background: #144272;
            padding: 1rem 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }

        .contact-list {
            max-width: 600px;
            margin: auto;
            padding: 2rem;
            text-align: left;
        }

        .contact-list h2 {
            color: #144272;
        }
    </style>
</head>

<body>
    <header>
        <h1>Contactos de los Encargados</h1>
    </header>

    <nav>
        <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería</a>
        <a href="preguntas%20frecuentes.html">Preguntas Frecuentes</a>
        <a href="contacto.html">Contacto</a>
        <a href="instalación.html">instalación</a>
        <a href="imformaci%C3%B3n2doy4to.html">imformación 2do y 4to</a>
    </nav>

    <div class="contact-list">
        <h2>Encargados del Proyecto</h2>
        <p><strong>Juan </strong> <br>📞 7295565887 </p>
        <p><strong>Blanca Estela</strong> <br>📞 4794793329</p>
        <p><strong>Roque</strong> <br>📞 4271860996 </p>
    </div>

    <footer>&copy; 2025 Proyecto de Acuaponía. Todos los derechos reservados.</footer>
</body>

</html>
