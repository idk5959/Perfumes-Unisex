
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Catálogo de Perfumes Unisex</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f5f5f5;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #9c8df0;
            color: white;
            padding: 25px 0;
            text-align: center;
        }
        nav {
            background-color: #d6d1ff;
            padding: 10px;
            text-align: center;
        }
        nav button {
            background-color: #9c8df0;
            border: none;
            color: white;
            padding: 10px 15px;
            margin: 4px;
            border-radius: 6px;
            cursor: pointer;
        }
        nav button:hover {
            background-color: #7c6df0;
        }
        section {
            display: none;
            padding: 25px;
        }
        .active {
            display: block;
        }
        .catalogo {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
            max-width: 1100px;
            margin: 20px auto;
        }
        .tarjeta {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 0 8px rgba(0,0,0,0.15);
            overflow: hidden;
            text-align: center;
            transition: transform 0.2s;
        }
        .tarjeta:hover {
            transform: scale(1.03);
        }
        .tarjeta img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }
        .tarjeta h3 {
            color: #4b3fa4;
            margin-top: 10px;
        }
        .tarjeta p {
            padding: 0 15px 20px;
            color: #333;
        }
        #sopaGrid {
            display: inline-grid;
            grid-template-columns: repeat(12, 30px);
            gap: 4px;
            margin-top: 20px;
        }
        .letra {
            width: 30px;
            height: 30px;
            background: white;
            border: 1px solid #ccc;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-weight: bold;
        }
        .letra.seleccionada {
            background: #c2b8ff;
        }
        .letra.encontrada {
            background: #9c8df0;
            color: white;
        }
        form {
            background: white;
            padding: 20px;
            border-radius: 10px;
            max-width: 650px;
            margin: auto;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
        }
        input, textarea, select {
            padding: 8px;
            margin: 6px;
            width: 260px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button.submit {
            background-color: #9c8df0;
            border: none;
            color: white;
            padding: 10px 18px;
            border-radius: 6px;
            cursor: pointer;
        }
        footer {
            text-align: center;
            background: #d6d1ff;
            padding: 15px;
            font-weight: bold;
            margin-top: 30px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Catálogo de Perfumes Unisex</h1>
        <p>Aromas modernos, equilibrados y pensados para todos</p>
    </header>

    <nav>
        <button onclick="mostrar('inicio')">Inicio</button>
        <button onclick="mostrar('sopa')">Sopa de Letras</button>
        <button onclick="mostrar('registro')">Registro</button>
    </nav>

    <!-- SECCIÓN INICIO -->
    <section id="inicio" class="active">
        <h2 style="text-align:center;">Descubre tu fragancia ideal</h2>
        <p style="max-width:900px; margin:auto; text-align:justify;">
            Los perfumes unisex han redefinido el mundo de las fragancias. Estos aromas combinan lo mejor de las notas frescas, florales, cítricas y amaderadas, adaptándose a cualquier estilo y personalidad. Cada perfume busca transmitir emociones, recuerdos y sensaciones únicas, sin importar género o edad. 
            En este catálogo encontrarás opciones cuidadosamente seleccionadas para acompañarte en cada momento del día, reflejando autenticidad, elegancia y libertad.
        </p>

        <div class="catalogo">
            <div class="tarjeta">
                <img src="https://www.primor.eu/blog/wp-content/uploads/2023/09/PERF-OLOR-ROSA.jpg">
                <h3>Citrus Harmony</h3>
                <p>Una fragancia llena de vitalidad, con notas de naranja, limón y bergamota, acompañadas de un toque de jazmín. Ideal para días soleados y personas que irradian energía positiva. Perfecta para el uso diario.</p>
            </div>
            <div class="tarjeta">
                <img src="https://hips.hearstapps.com/hmg-prod/images/cosmetic-products-on-table-beauty-concept-a-place-royalty-free-image-1721738273.jpg" alt="Perfume Velvet Woods">
                <h3>Velvet Woods</h3>
                <p>Inspirada en la elegancia natural, mezcla cedro, vainilla y almizcle blanco. Su aroma cálido y sofisticado deja una impresión duradera. Recomendado para ocasiones especiales o ambientes tranquilos.</p>
            </div>
            <div class="tarjeta">
                <img src="https://cl-dam-resizer.ecomm.cencosud.com/unsafe/adaptive-fit-in/792x1068/cl/paris/240653999/variant/688767c4558ec0ebd77cf4b2/images/ad7b93f8-b1b0-4f3c-9ef8-91501edcbf84/240653999-0000-003.jpg" alt="Perfume Ocean Mist">
                <h3>Ocean Mist</h3>
                <p>Frescura marina en una botella: notas de menta, lavanda y sal marina crean un aroma limpio y relajante. Ideal para quienes buscan una sensación de libertad y aire puro durante todo el día.</p>
            </div>
            <div class="tarjeta">
                <img src="https://s.alicdn.com/@sc01/kf/H2ed24ed4474f4297928c44af42a3a406B.jpg_720x720q50.jpg" alt="Perfume Amber Essence">
                <h3>Amber Essence</h3>
                <p>Perfume intenso con toques de ámbar, sándalo y especias suaves. Perfecto para la noche, transmite confianza y sofisticación. Una fragancia ideal para quienes desean destacar sin exagerar.</p>
            </div>
            <div class="tarjeta">
                <img src="https://aromasfenpal.com/wp-content/uploads/2024/10/perfume-otono-scaled.jpg" alt="Perfume Pure Blossom">
                <h3>Pure Blossom</h3>
                <p>Delicado y equilibrado aroma floral con notas de rosa, peonía y lirio, suavizado por un fondo amaderado. Su fragancia transmite calma, serenidad y elegancia atemporal.</p>
            </div>
        </div>
        <footer>Created by: Isabella Castaño y Angelo Vergara - 10°1</footer>
    </section>

    <!-- SECCIÓN SOPA DE LETRAS -->
    <section id="sopa">
        <h2>Sopa de Letras: Encuentra las palabras</h2>
        <p><strong>Palabras a encontrar:</strong> AROMA, FLORAL, FRESCO, AMADERADO, UNISEX</p>
        <div id="sopaGrid"></div>
        <p id="mensaje"></p>
    </section>

    <!-- SECCIÓN REGISTRO -->
    <section id="registro">
        <h2>Registro de Clientes</h2>
        <p>Completa el formulario para recibir noticias, descuentos y recomendaciones personalizadas.</p>
        <form onsubmit="enviarFormulario(event)">
            <input type="text" id="nombre" placeholder="Nombre completo" required><br>
            <input type="email" id="correo" placeholder="Correo electrónico" required><br>
            <input type="number" id="edad" placeholder="Edad" required><br>
            <select id="genero" required>
                <option value="">Selecciona tu género</option>
                <option>Masculino</option>
                <option>Femenino</option>
                <option>Prefiero no decirlo</option>
                <option>Otro</option>
            </select><br>
            <input type="text" id="pais" placeholder="País" required><br>
            <input type="text" id="ciudad" placeholder="Ciudad" required><br>
            <input type="text" id="direccion" placeholder="Dirección"><br>
            <input type="tel" id="telefono" placeholder="Número de teléfono"><br>
            <select id="preferencia">
                <option value="">Tipo de aroma favorito</option>
                <option>Floral</option>
                <option>Cítrico</option>
                <option>Amaderado</option>
                <option>Dulce</option>
                <option>Fresco</option>
            </select><br>
            <input type="text" id="marca" placeholder="Marca de perfume que más usas"><br>
            <textarea id="comentarios" placeholder="¿Qué esperas de un perfume unisex?"></textarea><br>
            <button class="submit" type="submit">Enviar registro</button>
        </form>
        <p id="resultado"></p>
    </section>

    <script>
        // Navegación entre secciones
        function mostrar(id) {
            document.querySelectorAll("section").forEach(s => s.classList.remove("active"));
            document.getElementById(id).classList.add("active");
        }

        // Formulario funcional
        function enviarFormulario(e) {
            e.preventDefault();
            const nombre = document.getElementById("nombre").value;
            const correo = document.getElementById("correo").value;
            const pais = document.getElementById("pais").value;
            document.getElementById("resultado").innerText =
                "Registro completado correctamente. Gracias " + nombre + " de " + pais + ". Te contactaremos en " + correo + ".";
        }

        // --- Sopa de letras funcional ---
        const palabras = ["AROMA", "FLORAL", "FRESCO", "AMADERADO", "UNISEX"];
        const tam = 12;
        const grid = Array(tam).fill().map(() => Array(tam).fill(''));
        const sopa = document.getElementById("sopaGrid");
        const letras = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
        const direcciones = [[1,0],[0,1],[1,1],[1,-1]];

        for (const palabra of palabras) {
            let colocada = false;
            while (!colocada) {
                const dir = direcciones[Math.floor(Math.random()*direcciones.length)];
                const x = Math.floor(Math.random()*(tam - palabra.length));
                const y = Math.floor(Math.random()*(tam - palabra.length));
                let puede = true;
                for (let i=0;i<palabra.length;i++){
                    const nx = x + dir[0]*i;
                    const ny = y + dir[1]*i;
                    if (grid[ny][nx] && grid[ny][nx] !== palabra[i]) { puede=false; break; }
                }
                if (puede){
                    for (let i=0;i<palabra.length;i++){
                        const nx = x + dir[0]*i;
                        const ny = y + dir[1]*i;
                        grid[ny][nx] = palabra[i];
                    }
                    colocada = true;
                }
            }
        }

        for (let y=0;y<tam;y++){
            for (let x=0;x<tam;x++){
                if (!grid[y][x]) grid[y][x] = letras[Math.floor(Math.random()*letras.length)];
            }
        }

        for (let y=0;y<tam;y++){
            for (let x=0;x<tam;x++){
                const div = document.createElement("div");
                div.classList.add("letra");
                div.textContent = grid[y][x];
                div.dataset.x = x;
                div.dataset.y = y;
                sopa.appendChild(div);
            }
        }

        let seleccionadas = [];
        const letrasDiv = document.querySelectorAll(".letra");
        letrasDiv.forEach(l => {
            l.addEventListener("click", () => {
                if (l.classList.contains("encontrada")) return;
                l.classList.toggle("seleccionada");
                const x = l.dataset.x, y = l.dataset.y;
                const pos = seleccionadas.findIndex(c => c.x==x && c.y==y);
                if (pos>=0) seleccionadas.splice(pos,1);
                else seleccionadas.push({x,y,letra:l.textContent});
                verificar();
            });
        });

        function verificar(){
            const texto = seleccionadas.map(c=>c.letra).join('');
            for (const palabra of palabras){
                if (texto === palabra){
                    seleccionadas.forEach(c=>{
                        const el = [...letrasDiv].find(d=>d.dataset.x==c.x && d.dataset.y==c.y);
                        el.classList.remove("seleccionada");
                        el.classList.add("encontrada");
                    });
                    seleccionadas = [];
                    document.getElementById("mensaje").textContent = "¡Encontraste la palabra " + palabra + "!";
                    return;
                }
            }
        }
    </script>
</body>
</html>
