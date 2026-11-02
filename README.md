<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Distribuidora San Judas Tadeo</title>
    <style>
        
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        header {
            background-color: #1b365d;
            color: white;
            text-align: center;
            padding: 20px;
        }

        nav {
            background-color: #2c5282;
            padding: 10px;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            font-weight: bold;
        }

        nav a:hover {
            background-color: #1b365d;
            border-radius: 4px;
        }

        .container {
            width: 80%;
            margin: 20px auto;
            background: white;
            padding: 20px;
            box-shadow: 0px 0px 10px #ccc;
        }

        h2 {
            color: #1b365d;
            border-bottom: 2px solid #2c5282;
            padding-bottom: 5px;
        }

        .buscador {
            margin-bottom: 20px;
            text-align: center;
        }

        .buscador input {
            padding: 8px;
            width: 60%;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        .grid-catalogo {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-around;
        }

        .card {
            border: 1px solid #ddd;
            border-radius: 5px;
            width: 250px;
            padding: 15px;
            background: #fafafa;
            text-align: center;
        }

        .card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 4px;
            background-color: #e2e8f0;
        }

        .card h3 {
            font-size: 18px;
            color: #2d3748;
            margin: 10px 0 5px 0;
        }

        .precio {
            color: #2b6cb0;
            font-weight: bold;
            font-size: 1.1em;
            margin: 10px 0;
        }

        footer {
            text-align: center;
            background-color: #1b365d;
            color: white;
            padding: 15px;
            margin-top: 30px;
            font-size: 14px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Distribuidora San Judas Tadeo</h1>
        <p>Catálogo Digital de Repuestos y Accesorios para Motocicletas</p>
    </header>

    <nav>
        <a href="#inicio">Inicio</a>
        <a href="#catalogo">Catálogo de Repuestos</a>
        <a href="#contacto">Contacto</a>
    </nav>

    <div class="container" id="inicio">
        <h2>Bienvenido</h2>
        <p>Ubicados en el sector Puente Unión, Capacho Viejo, Estado Táchira. Este sistema web optimiza la visualización de inventario, facilitando la búsqueda rápida de componentes mecánicos, sistemas eléctricos y accesorios para motocicletas en nuestro establecimiento.</p>
    </div>

    <div class="container" id="catalogo">
        <h2>Catálogo de Repuestos</h2>
        
        <div class="buscador">
            <input type="text" id="busqueda" placeholder="Buscar repuesto por nombre o categoría..." onkeyup="filtrarProductos()">
        </div>

        <div class="grid-catalogo" id="lista-productos">
            <!-- Producto 1 -->
            <div class="card">
                <img src="kitT.jpg" alt="Kit de Transmisión">
                <h3>Kit de Transmisión</h3>
                <p>Aplicación: Motos de Alta Rotación</p>
                <div class="precio">$25.00</div>
            </div>

            <!-- Producto 2 -->
            <div class="card">
                <img src="Pastillas.jpg" alt="Pastillas de Freno">
                <h3>Pastillas de Freno</h3>
                <p>Aplicación: Sistema delantero</p>
                <div class="precio">$6.50</div>
            </div>

            <!-- Producto 3 -->
            <div class="card">
                <img src="bujias.jpg" alt="Bujía de Encendido">
                <h3>Bujía de Encendido</h3>
                <p>Aplicación: Motor 150cc / 200cc</p>
                <div class="precio">$3.00</div>
            </div>

            <!-- Producto 4 -->
            <div class="card">
                <img src="CableCloche.jpg" alt="Cable de Embrague">
                <h3>Cable de Embrague</h3>
                <p>Aplicación: Universal / Ajustable</p>
                <div class="precio">$4.50</div>
            </div>
        </div>
    </div>

    <div class="container" id="contacto">
        <h2>Información de Contacto</h2>
        <p><strong>Ubicación:</strong> Sector Puente Unión, Parroquia Cipriano Castro, Capacho Viejo, Estado Táchira.</p>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d494.0809509609936!2d-72.31729741277272!3d7.827070810550914!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e666b0069c0038b%3A0x4cdb6f8ec5761ac2!2sREPUESTOS%20DISTRIBUIDORA%20SAN%20JUDAS%20TADEO!5e0!3m2!1ses-419!2sve!4v1793108390820!5m2!1ses-419!2sve" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="strict-origin-when-cross-origin"></iframe>
        <p><strong>Horario de atención:</strong> Lunes a Sábado de 8:00 AM a 6:00 PM.</p>
        <p><strong>Desarrollado por:</strong> Estudiantes del PNF en Informática - UPTAIET (2026).</p>
    </div>

    <footer>
        <p>&copy; 2026 Distribuidora San Judas Tadeo. Todos los derechos reservados.</p>
    </footer>

    <script>
        // Script filtrado JS
        function filtrarProductos() {
            let input = document.getElementById('busqueda').value.toLowerCase();
            let tarjetas = document.getElementsByClassName('card');

            for (let i = 0; i < tarjetas.length; i++) {
                let titulo = tarjetas[i].getElementsByTagName('h3')[0].innerText.toLowerCase();
                let descripcion = tarjetas[i].getElementsByTagName('p')[0].innerText.toLowerCase();
                
                if (titulo.includes(input) || descripcion.includes(input)) {
                    tarjetas[i].style.display = "";
                } else {
                    tarjetas[i].style.display = "none";
                }
            }
        }
    </script>

</body>
</html>
