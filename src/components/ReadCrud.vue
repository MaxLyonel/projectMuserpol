<template>
  <div class="contenedor">
    <div class="contenedor-estudiantes">
      <div class="contenedor-tabla">
        <table id="tabla" class="listado-estudiantes">
          <thead>
            <tr>
              <td>nombre</td>
              <td>paterno</td>
              <td>materno</td>
              <td>genero</td>
              <td>nacionalidad</td>
            </tr>
          </thead>
          <tbody>
            <tr v-for="estudiante in datos" :key="estudiante">
              <td>{{ estudiante.nombre }}</td>
              <td>{{ estudiante.paterno }}</td>
              <td>{{ estudiante.materno }}</td>
              <td>{{ estudiante.genero }}</td>
              <td>{{ estudiante.nacionalidad }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import datosBD from "@/assets/datos.json"; //include
export default {
  data: () => ({
    datos: datosBD,
  }),
};
</script>

<style>
.contenedor {
  max-width: 1100px;
  margin: 0 auto;
}
.contenedor-estudiantes {
  max-width: 800px;
  margin: 1rem auto 0 auto;
}
/* .contenedor-tabla {
  overflow: scroll;
} */
.listado-estudiantes {
  width: 100%;
  margin-top: 1rem;
  border-collapse: collapse;
}
.listado-estudiantes thead {
  background-color: #52be80;
  color: #2471a3;
  text-transform: uppercase;
  font-weight: bold;
}
.listado-estudiantes thead th {
  padding: 1rem 0;
}
.listado-estudiantes tbody td {
  padding: 0.5rem;
  background-color: #e8f9ff;
}
.listado-estudiantes tbody td:nth-child(4) {
  text-align: center;
}
</style>
