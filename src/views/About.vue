<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Scene />
  </div>
</template>

<script>
// @ is an alias to /src
import Scene from '@/components/three/Scene.vue'

export default {
  name: 'home',
  components: {
    Scene
  }
}
</script>
