# Los-reyes
Está moda es el lujo 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>[Nombre de la Marca]</title>
  <style>
    /* Variables de color */
    :root {
      --negro: #0a0a0a;
      --blanco: #f9f9f9;
      --dorado: #c9a134;
      --gris: #222;
      --fuente-principal: 'Arial Black', sans-serif;
      --transicion: 0.3s ease;
    }

    /* Reset básico */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: var(--negro);
      color: var(--blanco);
      font-family: var(--fuente-principal);
      line-height: 1.5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: var(--gris);
      border-bottom: 2px solid var(--dorado);
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      z-index: 1000;
    }

    header h1 {
      color: var(--dorado);
      font-size: 2rem;
      cursor: pointer;
      user-select: none;
    }

    nav {
      display: flex;
      gap: 2rem;
    }

    nav a {
      color: var(--blanco);
      text-decoration: none;
      font-weight: bold;
      font-size: 1.1rem;
      transition: color var(--transicion);
    }

    nav a:hover {
      color: var(--dorado);
    }

    main {
      margin-top: 90px; /* espacio para header fijo */
      flex-grow: 1;
    }

    section {
      padding: 4rem 2rem;
      border-bottom: 1px solid var(--gris);
      max-width: 1200px;
      margin: auto;
    }

    /* Banner Inicio */
    #inicio {
      background: url('https://via.placeholder.com/1400x400') center/cover no-repeat;
      height: 400px;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
      color: var(--blanco);
      font-size: 2.5rem;
      font-weight: 900;
      text-shadow: 2px 2px 8px #000;
    }

    #inicio::before {
      content: '';
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    #inicio > * {
      position: relative;
      z-index: 1;
    }

    /* Catálogo */
    #catalogo h2 {
      color: var(--dorado);
      margin-bottom: 2rem;
      text-align: center;
    }

    .productos {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
      gap: 2rem;
    }

    .producto {
      background-color: var(--gris);
      border-radius: 10px;
      padding: 1rem;
      text-align: center;
      transition: transform 0.3s ease;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(201, 161, 52, 0.4);
    }

    .producto:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px rgba(201, 161, 52, 0.8);
    }

    .producto img {
      width: 100%;
      border-radius: 8px;
      margin-bottom: 1rem;
      object-fit: cover;
      height: 200px;
    }

    .producto h3 {
      margin-bottom: 0.5rem;
      color: var(--dorado);
    }

    .producto p {
      font-weight: bold;
      margin-bottom: 1rem;
      font-size: 1.2rem;
    }

    .boton-agregar {
      background-color: var(--dorado);
      border: none;
      padding: 0.6rem 1.2rem;
      border-radius: 20px;
      color: var(--negro);
      font-weight: bold;
      cursor: pointer;
      transition: background-color var(--transicion);
    }

    .boton-agregar:hover {
      background-color: #a87f23;
    }

    /* Galería */
    #galeria h2 {
      color: var(--dorado);
      margin-bottom: 2rem;
      text-align: center;
    }

    .galeria-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
      gap: 1rem;
    }

    .galeria-grid img, .galeria-grid video {
      width: 100%;
      border-radius: 8px;
      object-fit: cover;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(201,161,52,0.5);
      transition: transform 0.3s ease;
    }

    .galeria-grid img:hover, .galeria-grid video:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px rgba(201,161,52,0.9);
    }

    /* Sobre Nosotros */
    #nosotros h2 {
      color: var(--dorado);
      margin-bottom: 2rem;
      text-align: center;
    }

    #nosotros p {
      max-width: 900px;
      margin: auto;
      font-size: 1.1rem;
      line-height: 1.6;
      text-align: center;
    }

    /* Contacto */
    #contacto h2 {
      color: var(--dorado);
      margin-bottom: 2rem;
      text-align: center;
    }

    form {
      max-width: 600px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    input, textarea {
      padding: 0.8rem;
      border-radius: 6px;
      border: none;
      font-size: 1rem;
      font-family: inherit;
    }

    input:focus, textarea:focus {
      outline: 2px solid var(--dorado);
      background-color: #222;
      color: var(--blanco);
    }

    button {
      background-color: var(--dorado);
      border: none;
      padding: 1rem;
      border-radius: 30px;
      font-weight: bold;
      cursor: pointer;
      transition: background-color var(--transicion);
      color: var(--negro);
    }

    button:hover {
      background-color: #a87f23;
    }

    /* Footer */
    footer {
      background-color: var(--gris);
      text-align: center;
      padding: 1rem 0;
      color: var(--blanco);
      font-size: 0.9rem;
      margin-top: auto;
    }

    /* Carrito (básico visual) */
    #carrito {
      position: fixed;
      right: 20px;
      bottom: 20px;
      background-color: var(--dorado);
      color: var(--negro);
      padding: 1rem 1.5rem;
      border-radius: 30px;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 0 15px rgba(201,161,52,0.8);
      user-select: none;
      z-index: 1100;
      transition: background-color var(--transicion);
    }

    #carrito:hover {
      background-color: #a87f23;
    }

    /* Responsive */
    @media(max-width: 600px){
      header {
        flex-direction: column;
        gap: 1rem;
      }

      nav {
        gap: 1rem;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1 contenteditable="true" spellcheck="false">[Nombre de la Marca]</h1>
    <nav>
      <a href="#inicio">Inicio</a>
      <a href="#catalogo">Catálogo</a>
      <a href="#galeria">Galería</a>
      <a href="#nosotros">Sobre Nosotros</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <main>
    <section id="inicio" aria-label="Inicio">
      <h2>"No es para todos. Es para los que se atreven."</h2>
    </section>

    <section id="catalogo" aria-label="Catálogo">
      <h2>Catálogo</h2>
      <div class="productos" id="productos">
        <!-- Aquí se insertan productos dinámicamente -->
      </div>
    </section>

    <section id="galeria" aria-label="Galería">
      <h2>Galería</h2>
      <div class="galeria-grid" id="galeria-grid">
        <!-- Aquí puedes subir fotos/videos -->
        <img src="https://via.placeholder.com/300x400" alt="Foto muestra 1" />
        <img src="https://via.placeholder.com/300x400" alt="Foto muestra 2" />
        <video controls width="300" src="https://www.w3schools.com/html/mov_bbb.mp4"></video>
      </div>
    </section>

    <section id="nosotros" aria-label="Sobre Nosotros">
      <h2>Sobre Nosotros</h2>
      <p contenteditable="true" spellcheck="false">
        Esta marca nace del fuego y el hambre de dejar huella. Creamos prendas que combinan lujo, calle y actitud. Cada diseño es pensado para destacar. No seguimos tendencias, las dictamos. Nos esforzamos por entregar calidad, estilo y poder en cada pieza.
      </p>
    </section>

    <section id="contacto" aria-label="Contacto">
      <h2>Contacto</h2>
      <form id="form-contacto">
        <input type="text" name="nombre" placeholder="Tu nombre" required />
        <input type="email" name="correo" placeholder="Tu correo" required />
        <textarea name="mensaje" rows="5" placeholder="Mensaje..." required></textarea>
        <button type="submit">Enviar</button>
      </form>
      <p id="respuesta-form" style="text-align:center; margin-top: 1rem;"></p>
    </section>
  </main>

  <div id="carrito" title="Ver carrito">Carrito 🛒 (0)</div>

  <footer>
    &copy; 2025 <span contenteditable="true" spellcheck="false">[Nombre de la Marca]</span>. Todos los derechos reservados.
  </footer>

  <script>
    // Productos de ejemplo - remplaza o agrega los que quieras
    const productos = [
      {
        id: 1,
        nombre: "Hoodie Oversize Dorado",
        precio: 1200,
        imagen: "https://via.placeholder.com/300x400?text=Hoodie+Dorado"
      },
      {
        id: 2,
        nombre: "Camiseta Gráfica Alucín",
        precio: 700,
        imagen: "https://via.placeholder.com/300x400?text=Camiseta+Alucin"
      },
      {
        id: 3,
        nombre: "Pantalón Cargo Street",
        precio: 1100,
        imagen: "https://via.placeholder.com/300x400?text=Pantalon+Cargo"
      }
    ];

    const contenedorProductos = document.getElementById('productos');
    const carritoBtn = document.getElementById('carrito');
    let carrito = [];

    function mostrarProductos(){
      contenedorProductos.innerHTML = '';
      productos.forEach(p => {
        const div = document.createElement('div');
        div.classList.add('producto');
        div.innerHTML = `
          <img src="${p.imagen}" alt="${p.nombre}" />
          <h3>${p.nombre}</h3>
          <p>$${p.precio.toFixed(2)}</p>
          <button class="boton-agregar" data-id="${p.id}">Agregar al carrito</button>
        `;
        contenedorProductos.appendChild(div);
      });
    }

    function actualizarCarrito(){
      carritoBtn.textContent = `Carrito 🛒 (${carrito.length})`;
    }

    function agregarAlCarrito(id){
      const producto = productos.find(p => p.id === id);
      if(producto){
        carrito.push(producto);
        actualizarCarrito();
        alert(`${producto.nombre} agregado al carrito`);
      }
    }

    contenedorProductos.addEventListener('click', e => {
      if(e.target.classList.contains('boton-agregar')){
        const id = parseInt(e.target.dataset.id);
        agregarAlCarrito(id);
      }
    });

    // Formulario contacto (simulación)
    const formContacto = document.getElementById('form-contacto');
    const respuestaForm = document.getElementById('respuesta-form');
    formContacto.addEventListener('submit', e => {
      e.preventDefault();
      respuestaForm.textContent = "Gracias por contactarnos. Pronto responderemos.";
      formContacto.reset();
    });

    mostrarProductos();
    actualizarCarrito();

  </script>

</body>
</html>
