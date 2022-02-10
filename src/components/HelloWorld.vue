<template>
  <div >
    <table id="tabla">
      <tr>
        <td>nombre</td>
        <td>paterno</td>
        <td>materno</td>
        <td>genero</td>
        <td>nacionalidad</td>
      </tr>
      <tr v-for="estudiante in datos" :key="estudiante">
        <td >{{estudiante.nombre}}</td>
        <td >{{estudiante.paterno}}</td>
        <td >{{estudiante.materno}}</td>
        <td >{{estudiante.genero}}</td>
        <td >{{estudiante.nacionalidad}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
import datosBD from '@/assets/datos.json'
export default {
  
  data: () => ({
      datos: datosBD
    })
  }
</script>

<style>
  table {
    width: 60%;
  }
  th, td {
    width: 2%;
    text-align: left;
    vertical-align: top;
    border: 1px solid #000;
    border-spacing: 0;
    border-collapse: collapse;
  }
  
</style>