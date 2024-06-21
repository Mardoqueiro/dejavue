<template>
 <div class="container">
  <div class="row">
    <h1>Dejavue</h1>
  </div>
  <div class="row">
    <Friends/>
  </div>
  <div class="row">
    <Products/>
  </div>
 </div>
  
</template>

<script>
import Friends from '@/components/Friends.vue'
import Products from '@/components/Products.vue'
export default {
  name: 'App',
  components: {
    Friends,
    Products,
  },
  data() {
    return {
      friends: [
      {
        firstName: "Mardoqueiro",
        lastName: "Dimbu",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/Gitprofil.jpg'
      },
      {
        firstName: "Ordi",
        lastName: "Kitoko",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/IMG_20240607_135942_589.jpg'
      },
      {
        firstName: "Terence",
        lastName: "Tweng",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/IMG_20240607_150343_596.jpg'
      },
      {
        firstName: "Kamva",
        lastName: "Banzi",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/Screenshot_20240607_150245_WhatsApp.jpg'
      },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.card {
  display: grid;
}
</style>
