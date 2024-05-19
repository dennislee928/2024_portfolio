<template>
  <div>
    <Header />
    <div id="three-background"></div>
    <!-- Container for the 3D scene -->

    <div class="page-title">
      <h1>CV Page</h1>
    </div>
    <!-- Your CV content here -->
    <cvCard />
    <Footer />
  </div>
</template>

<script>
import * as THREE from "three";

export default {
  name: "CVPage",
  mounted() {
    this.initThreeJS();
  },
  methods: {
    initThreeJS() {
      const scene = new THREE.Scene();
      const camera = new THREE.PerspectiveCamera(
        75,
        window.innerWidth / window.innerHeight,
        0.1,
        1000
      );

      const renderer = new THREE.WebGLRenderer({ alpha: true }); // Set alpha to true for transparent background
      renderer.setSize(window.innerWidth, window.innerHeight);
      document
        .getElementById("three-background")
        .appendChild(renderer.domElement);

      const geometry = new THREE.TorusKnotGeometry(10, 3, 100, 16);
      const material = new THREE.MeshBasicMaterial({
        color: 0x00ff00,
        wireframe: true,
      });
      const torusKnot = new THREE.Mesh(geometry, material);
      scene.add(torusKnot);

      camera.position.z = 25;

      function animate() {
        requestAnimationFrame(animate);
        torusKnot.rotation.x += 0.01;
        torusKnot.rotation.y += 0.01;
        renderer.render(scene, camera);
      }

      animate();
    },
  },
};
</script>

<style>
#three-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}
.page-title {
  align-items: center;
  align-content: center;
  text-align: center;
  position: relative; /* Ensures the title appears above the 3D background */
}
</style>
