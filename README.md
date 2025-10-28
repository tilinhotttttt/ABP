<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Proyecto ABP</title>
<style>
  body {
    background-color: #e0e0db;
    font-family: 'Arial Rounded MT Bold', sans-serif;
    margin: 0;
    padding: 0;
  }

  header {
    background-color: #2e8b57;
    color: rgb(255, 255, 255);
    text-align: center;
    padding: 20px 0;
    font-size: 28px;
    font-weight: bold;
    box-shadow: 0 4px 6px rgba(0,0,0,0.2);
  }

  h1 {
    color: #010202;
    font-size: 40px;
    text-align: center;
    margin-top: 20px;
  }

  p {
    text-align: center;
    font-size: 20px;
    color: #333;
  }

  .card-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
    padding: 20px;
  }

  .card {
    background-color: rgb(10, 228, 210);
    border-radius: 15px;
    width: 300px;
    padding: 25px;
    box-shadow: 0 0 10px rgba(0,0,0,0.3);
    cursor: pointer;
    transition: transform 0.3s;
    text-align: center;
    font-size: 22px;
    font-weight: bold;
  }

  .card:hover {
    transform: scale(1.05);
    background-color: #d7f8e3;
  }

  .subject-content {
    display: none;
    padding: 20px;
    width: 90%;
    margin: 20px auto;
    background-color: white;
    border-radius: 15px;
    box-shadow: 0 0 15px rgba(0,0,0,0.2);
    animation: fadeIn 0.4s ease-in-out;
  }

  .subject-layout {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }

  .student-list {
    flex: 1;
    min-width: 250px;
    background-color: #e8f5ec;
    border-radius: 15px;
    padding: 15px;
    text-align: center;
  }

  .student-list div {
    background-color: white;
    border-radius: 10px;
    margin: 10px 0;
    padding: 15px;
    font-size: 22px;
    cursor: pointer;
    box-shadow: 0 0 8px rgba(0,0,0,0.2);
    transition: background-color 0.3s, transform 0.3s;
  }

  .student-list div:hover {
    background-color: #b7e7c2;
    transform: scale(1.05);
  }

  .student-work {
    flex: 2;
    min-width: 300px;
    text-align: center;
  }

  .student-work img, .student-work iframe, .student-work video {
    max-width: 90%;
    border-radius: 10px;
    margin-top: 10px;
  }

  .back-btn {
    display: block;
    background-color: #2e8b57;
    color: white;
    border: none;
    border-radius: 10px;
    padding: 10px 15px;
    cursor: pointer;
    font-size: 16px;
    margin: 20px auto 0;
  }

  .back-btn:hover {
    background-color: #256b45;
  }

  @keyframes fadeIn {
    from {opacity: 0; transform: scale(0.95);}
    to {opacity: 1; transform: scale(1);}
  }
</style>
</head>
<body>

<header>Proyecto ABP</header>
<h1>Salud sexual, nutrición y autocuidado corporal</h1>

<div class="card-container" id="main-menu">
  <div class="card" onclick="mostrarMateria('fisica')">Física</div>
  <div class="card" onclick="mostrarMateria('quimica')">Química</div>
  <div class="card" onclick="mostrarMateria('edfisica')">Educación Física</div>
  <div class="card" onclick="mostrarMateria('lenguaje')">Lenguaje y Comunicación</div>
  <div class="card" onclick="mostrarMateria('sexualidad')">Educación en Integridad y Sexualidad</div>
  <div class="card" onclick="mostrarMateria('ingles')">Inglés</div>
  <div class="card" onclick="mostrarMateria('biologia')">Biología</div>
  <div class="card" onclick="mostrarMateria('cultural')">Cultura y Arte</div>
</div>

<!-- Física -->
<div id="fisica" class="subject-content">
  <h2>Física</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('fisica','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('fisica','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('fisica','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('fisica','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('fisica','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="fisica-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Química -->
<div id="quimica" class="subject-content">
  <h2>Química</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('quimica','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('quimica','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('quimica','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('quimica','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('quimica','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="quimica-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Educación Física -->
<div id="edfisica" class="subject-content">
  <h2>Educación Física</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('edfisica','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('edfisica','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('edfisica','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('edfisica','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('edfisica','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="edfisica-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Lenguaje -->
<div id="lenguaje" class="subject-content">
  <h2>Lenguaje y Comunicación</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('lenguaje','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('lenguaje','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('lenguaje','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('lenguaje','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('lenguaje','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="lenguaje-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Sexualidad -->
<div id="sexualidad" class="subject-content">
  <h2>Educación en Integridad y Sexualidad</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('sexualidad','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('sexualidad','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('sexualidad','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('sexualidad','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('sexualidad','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="sexualidad-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Inglés -->
<div id="ingles" class="subject-content">
  <h2>Inglés</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('ingles','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('ingles','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('ingles','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('ingles','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('ingles','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="ingles-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Biología -->
<div id="biologia" class="subject-content">
  <h2>Biología</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('biologia','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('biologia','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('biologia','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('biologia','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('biologia','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="biologia-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<!-- Cultura -->
<div id="cultural" class="subject-content">
  <h2>Cultura y Arte</h2>
  <div class="subject-layout">
    <div class="student-list">
      <div onclick="mostrarTrabajo('cultural','carlos')">Carlos Merino</div>
      <div onclick="mostrarTrabajo('cultural','santiago')">Santiago Bajaña</div>
      <div onclick="mostrarTrabajo('cultural','jhorel')">Jhorel Carvajal</div>
      <div onclick="mostrarTrabajo('cultural','angel')">Ángel Paguay</div>
      <div onclick="mostrarTrabajo('cultural','davide')">Davide Paredes</div>
    </div>
    <div class="student-work" id="cultural-trabajo">
      <p>Selecciona un estudiante para ver su trabajo.</p>
    </div>
  </div>
  <button class="back-btn" onclick="volver()">⬅ Volver</button>
</div>

<script>
function mostrarMateria(id) {
  document.getElementById("main-menu").style.display = "none";
  document.querySelectorAll(".subject-content").forEach(div => div.style.display = "none");
  document.getElementById(id).style.display = "block";
}

function volver() {
  document.querySelectorAll(".subject-content").forEach(div => div.style.display = "none");
  document.getElementById("main-menu").style.display = "flex";
}

const nombres = {
  carlos:'Carlos Merino',
  santiago:'Santiago Bajaña',
  jhorel:'Jhorel Carvajal',
  angel:'Ángel Paguay',
  davide:'Davide Paredes'
};

function mostrarTrabajo(materia, estudiante) {
  const contenedor = document.getElementById(materia + '-trabajo');
  let contenido = '';

  if (materia === 'fisica') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><iframe src="https://drive.google.com/file/d/1arxGaouYIuGnD5Hc5vovVqrit9Vi8TbS/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/1CqfkSc4xGIbScOQQoo6piDfljXf2mBrM/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><iframe src="https://drive.google.com/file/d/1arxGaouYIuGnD5Hc5vovVqrit9Vi8TbS/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><iframe src="https://drive.google.com/file/d/1aAFk6IJ09Js7fvBCDR_D516nnMdtW6fX/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><p>Experimento de fuerza y aceleración.</p>`;
        break;
    }
  }

  if (materia === 'quimica') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><iframe src="https://drive.google.com/file/d/1XkP5iGuS30db2L743Dpn_U4yZzkqrw0_/preview" width="640" height="480" allow="autoplay"></iframe>`;
         break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/180C_1ZGXz67840OfHnN9rz4lb81alxph/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><p>Trabajo de Química de Jhorel.</p>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><iframe src="https://drive.google.com/file/d/1HbAN327rOu0JrWa61_5hW3m-mgxgivyh/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><p>Trabajo de Química de Davide.</p>`;
        break;
    }
  }

  if (materia === 'edfisica') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><iframe src="https://drive.google.com/file/d/1_n70HBOnxqVkh9PnPU0SmTnwz14c9nGw/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/1IHxA8UyBLjt3odLg1nSCWM67B8Ee89on/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><p>Video de ejercicios de Jhorel.</p>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><iframe src="https://drive.google.com/file/d/1y1fRCsYE0bU1weecKX_Hc7lS1DnrfNyL/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><p>Plan de ejercicios de Davide.</p>`;
        break;
    }
  }

  if (materia === 'lenguaje') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><p>Ensayo de Carlos sobre literatura.</p>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/1Xp3dLGRarAMcOlfN1BMBpojEc77_D2WP/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><p>Análisis de texto de Jhorel.</p>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><iframe src="https://drive.google.com/file/d/18uFqCZWDfZ1QG1IgAIGh7xZsoTZik-KT/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><p>Trabajo literario de Davide.</p>`;
        break;
    }
  }

  if (materia === 'sexualidad') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><iframe src="https://drive.google.com/file/d/1bp9hnJfaeqctCxM9hhb4wPnunN_01mEU/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/1Wsb-x7cwxgqqcvB_es8sYhxQap2470Ha/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><iframe src="https://drive.google.com/file/d/1bp9hnJfaeqctCxM9hhb4wPnunN_01mEU/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><<iframe src="https://drive.google.com/file/d/1PykxasqKWWeKo93yKnDaA6lPZIBhjX7u/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><iframe src="https://drive.google.com/file/d/1bp9hnJfaeqctCxM9hhb4wPnunN_01mEU/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
    }
  }

  if (materia === 'ingles') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><p>Trabajo de inglés de Carlos.</p>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/1nKMxmTgpsrLqKdLr02xPYrZY-9dZFtOz/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><p>Trabajo de inglés de Jhorel.</p>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><p>Trabajo de inglés de Ángel.</p>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><p>Trabajo de inglés de Davide.</p>`;
        break;
    }
  }

  if (materia === 'biologia') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><iframe src="https://drive.google.com/file/d/10xOXNsTeHddseXkgJBV_L0RAKMN4s5Kt/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><iframe src="https://drive.google.com/file/d/10xOXNsTeHddseXkgJBV_L0RAKMN4s5Kt/preview" width="640" height="480" allow="autoplay"></iframe>`;;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><iframe src="https://drive.google.com/file/d/10xOXNsTeHddseXkgJBV_L0RAKMN4s5Kt/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><iframe src="https://drive.google.com/file/d/10xOXNsTeHddseXkgJBV_L0RAKMN4s5Kt/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><iframe src="https://drive.google.com/file/d/10xOXNsTeHddseXkgJBV_L0RAKMN4s5Kt/preview" width="640" height="480" allow="autoplay"></iframe>`;
        break;
    }
  }

  if (materia === 'cultural') {
    switch(estudiante) {
      case 'carlos':
        contenido = `<h3>Carlos Merino</h3><p>Trabajo cultural de Carlos.</p>`;
        break;
      case 'santiago':
        contenido = `<h3>Santiago Bajaña</h3><p>Trabajo cultural de Santiago.</p>`;
        break;
      case 'jhorel':
        contenido = `<h3>Jhorel Carvajal</h3><p>Trabajo cultural de Jhorel.</p>`;
        break;
      case 'angel':
        contenido = `<h3>Ángel Paguay</h3><p>Trabajo cultural de Ángel.</p>`;
        break;
      case 'davide':
        contenido = `<h3>Davide Paredes</h3><p>Trabajo cultural de Davide.</p>`;
        break;
    }
  }

  contenedor.innerHTML = contenido;
}
</script>
