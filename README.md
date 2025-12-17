# Odara
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>ODARA Nails</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: #ffffff;
      color: #333;
    }

    header {
      text-align: center;
      padding: 40px 20px;
    }

    h1 {
      color: #e8a7b7;
      font-size: 36px;
      margin-bottom: 10px;
    }

    .bienvenida {
      max-width: 600px;
      margin: auto;
      font-size: 16px;
    }

    .intro {
      margin-top: 15px;
      font-size: 14px;
      color: #666;
    }

    .botones {
      margin-top: 25px;
    }

    button {
      background: #f6c1d1;
      border: none;
      padding: 12px 20px;
      border-radius: 25px;
      font-size: 15px;
      margin: 8px;
      cursor: pointer;
    }

    section {
      display: none;
      padding: 40px 20px;
      text-align: center;
    }

    .servicio {
      background: #fafafa;
      padding: 15px;
      margin: 10px auto;
      max-width: 400px;
      border-radius: 15px;
    }

    iframe {
      width: 100%;
      max-width: 600px;
      height: 300px;
      border: 0;
      border-radius: 15px;
      margin-top: 25px;
    }

    .pago {
      background: #fafafa;
      padding: 20px;
      border-radius: 15px;
      max-width: 400px;
      margin: 15px auto;
    }

    .copiar {
      background: #e8a7b7;
      color: white;
      margin-top: 10px;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #f6c1d1;
      margin-top: 30px;
    }
  </style>
</head>

<body>

<header>
  <h1>ODARA</h1>

  <p class="bienvenida">
    En ODARA te ofrecemos un servicio único para realzar tu estilo, cuidando cada detalle
    y utilizando productos de calidad para lograr un acabado prolijo y duradero.
  </p>

  <p class="intro">
    Aquí podrás encontrar toda la información sobre nuestros servicios.
  </p>

  <div class="botones">
    <button onclick="mostrar('servicios')">Servicios</button>
    <button onclick="whatsapp()">Consultas</button>
    <button onclick="mostrar('turnos')">Turnos</button>
    <button onclick="mostrar('pagos')">Métodos de pago</button>
  </div>

  <iframe
    src="https://www.google.com/maps?q=-34.6037,-58.3816&output=embed"
    loading="lazy">
  </iframe>
</header>

<section id="servicios">
  <h2>Servicios</h2>

  <div class="servicio">Semipermanente – $12.000</div>
  <div class="servicio">Kapping – $13.500</div>
  <div class="servicio">Soft Gel – $14.000</div>
  <div class="servicio">Esculpidas en Polygel – $16.000</div>
  <div class="servicio">Retiro – $3.000</div>

  <button onclick="volver()">Volver</button>
</section>

<section id="turnos">
  <h2>Solicitar turno</h2>

  <p>Completá tus datos y te responderemos por WhatsApp.</p>

  <input id="nombre" placeholder="Nombre" style="padding:10px;width:80%;margin:5px;"><br>
  <input id="dia" placeholder="Día preferido" style="padding:10px;width:80%;margin:5px;"><br>
  <input id="hora" placeholder="Horario preferido" style="padding:10px;width:80%;margin:5px;"><br>

  <button onclick="enviarTurno()">Enviar por WhatsApp</button>
  <br><br>
  <button onclick="volver()">Volver</button>
</section>

<section id="pagos">
  <h2>Métodos de pago</h2>

  <div class="pago">
    <strong>Efectivo</strong>
  </div>

  <div class="pago">
    <strong>Transferencia</strong>
    <p>Ana Molina</p>
    <p>Alias: <span id="alias">aanamolina</span></p>
    <p>CVU: 0000003100003776004982</p>
    <p>CUIT: 27469725826</p>
    <p>Mercado Pago</p>

    <button class="copiar" onclick="copiarAlias()">Copiar alias</button>
  </div>

  <button onclick="volver()">Volver</button>
</section>

<footer>
  ODARA Nails 💅
</footer>

<script>
  function mostrar(id) {
    document.querySelectorAll("section").forEach(s => s.style.display = "none");
    document.getElementById(id).style.display = "block";
    window.scrollTo(0, 0);
  }

  function volver() {
    document.querySelectorAll("section").forEach(s => s.style.display = "none");
  }

  function whatsapp() {
    window.open("https://wa.me/549XXXXXXXXXX", "_blank");
  }

  function enviarTurno() {
    let nombre = document.getElementById("nombre").value;
    let dia = document.getElementById("dia").value;
    let hora = document.getElementById("hora").value;

    let mensaje = `Hola, soy ${nombre}. Quisiera un turno para el día ${dia} en el horario ${hora}.`;
    window.open(`https://wa.me/549XXXXXXXXXX?text=${encodeURIComponent(mensaje)}`, "_blank");
  }

  function copiarAlias() {
    navigator.clipboard.writeText("aanamolina");
    alert("Alias copiado");
  }
</script>

</body>
</html>
