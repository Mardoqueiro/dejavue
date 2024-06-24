<template>
  <div class="container">
    <div class="row">
        <h3 class="display-2">Friends</h3>
    </div>
    <div class="row gap-2" v-if="friends.length">
      <Card v-for="friend in friends" :key="friend.id" :class="{male: friend.gender == 'male', female: friend.gender == 'female'}" >
        <template #cardheader>
            <img class="img-fluid" :src="friend.profile" :alt="friend.firstName" loading="lazy">
          {{ friend.firstName }} {{ friend.lastName }}
          </template>
        <template #cardbody>
          <p>Gender: {{ friend.gender }}</p>
          <p>contact: {{ friend.contact }}</p>
        </template>
      </Card>
    </div>
    <div class="d-flex justify-content-center" v-else>
      <div class="spinner-border" role="status">
        <span class="visually-hidden">Loading...</span>
      </div>
    </div>
  </div>
</template>

<script>
import Card from './Card.vue';

export default {
  name: 'FriendsComp',
  components: {
    Card,
  },
  
  data() {
    return {
      friends: [
          {
            id: 1,
            firstName: "Mardoqueiro",
            lastName: "Dimbu",
            gender: "male",
            contact: "+555 555 5555",
            profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/Gitprofil.jpg'
          },
          {
            id: 2,
            firstName: "Ordi",
            lastName: "Kitoko",
            gender: "female",
            contact: "+555 555 5555",
            profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/IMG_20240607_135942_589.jpg'
          },
          {
            id: 3,
            firstName: "Terence",
            lastName: "Tweng",
            gender: "male",
            contact: "+555 555 5555",
            profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/IMG_20240607_150343_596.jpg'
          },
          {
            id: 4,
            firstName: "Kamva",
            lastName: "Banzi",
            gender: "female",
            contact: "+555 555 5555",
            profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/Screenshot_20240607_150245_WhatsApp.jpg'
          },
      ]
    };
  },
};
</script>

<style scoped>
.card {
  width: 18rem;
}
.male {
  border: 2px solid gold;
}
.female {
  border: 2px solid pink;
}
</style>
