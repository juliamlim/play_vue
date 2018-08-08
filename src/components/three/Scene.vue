<template>
  <div></div>
</template>

<script>
import * as THREE from 'three'

export default {
  name: 'three',
  props: {
    width: {
      type: Number,
      default: window.innerWidth
    },
    height: {
      type: Number,
      default: 300
    }
  },
  data () {
    return {
      scene: new THREE.Scene(),
      camera: new THREE.PerspectiveCamera(75, this.width / this.height, 0.1, 1000),
      renderer: new THREE.WebGLRenderer()
    }
  },
  created () {
    const vm = this

    vm.renderer.setSize(this.width, this.height)

    var geometry = new THREE.BoxGeometry(1, 3, 1)
    var material = new THREE.MeshNormalMaterial()
    var cube = new THREE.Mesh(geometry, material)
    cube.position.set(-2, -1, 0)
    vm.scene.add(cube)

    vm.camera.position.z = 5

    vm.renderer.render(vm.scene, vm.camera)
  },
  mounted () {
    const vm = this
    vm.$el.innerHTML = ''
    vm.$el.appendChild(vm.renderer.domElement)
  }
}
</script>
