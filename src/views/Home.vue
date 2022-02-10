<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h2>Listado de estudiantes </h2>
    <Read/>
  </div>
</template>

<script>
// @ is an alias to /src
import Read from '@/components/ReadCrud.vue'

export default {
  name: 'Home',
  components: {
    Read
  }
}
</script>
