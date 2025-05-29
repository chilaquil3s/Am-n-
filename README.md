<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Accidentes en Motocicletas</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Prevención de Accidentes en Motocicleta</h1>
  </header>

  <main>
    <section>
      <h2>¿Por qué ocurren los accidentes?</h2>
      <p>Los accidentes en motocicleta suelen ser causados por exceso de velocidad, falta de equipo de protección, poca visibilidad y fallas humanas.</p>
    </section>

    <section>
      <h2>Imágenes</h2>
      <img src="img/accidente1.jpg" alt="Accidente en motocicleta" class="responsive-img">
    </section>

    <section>
      <h2>Video informativo</h2>
      <video controls width="100%">
        <source src="video/accidentes.mp4" type="video/mp4">
        Tu navegador no soporta video HTML5.
      </video>
    </section>

    <section>
      <h2>Formulario de Registro</h2>
      <form id="registro">
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required>
        <label for="email">Correo:</label>
        <input type="email" id="email" name="email" required>
        <button type="submit">Registrarse</button>
      </form>
      <p id="mensaje"></p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Proyecto Escolar</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header, footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1em;
}

main {
  padding: 1em;
}

.responsive-img {
  max-width: 100%;
  height: auto;
}

form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
}

input, button {
  margin: 0.5em 0;
  padding: 0.5em;
}document.getElementById('registro').addEventListener('submit', function(e) {
  e.preventDefault();
  const nombre = document.getElementById('nombre').value;
  document.getElementById('mensaje').textContent = `Gracias por registrarte, ${nombre}.`;
});
