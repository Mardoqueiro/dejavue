<template>
    <div class="row">
        <div v-if="friends.length">
          <Card v-for="friend in friends" :key="friend.id" :gender="friend.gender">
            <template #cardheader>
                <img class="img-fluid" :src="friend.profile" :alt="friend.firstName" loading="lazy">
              {{ friend.firstName }} {{ friend.lastName }}
              </template>
            <template #cardbody>
              <p>Gender: {{ friend.gender }}</p>
              <p>Profile: {{ friend.profile }}</p>
            </template>
          </Card>
        </div>
        <div v-else>
          <div class="spinner-border" role="status">
            <span class="sr-only">Loading...</span>
          </div>
        </div>
    </div>
  </template>
  
  <script>
  import Card from './Card.vue';
  
  export default {
    name: 'FriendComp',
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
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/Gitprofil.jpg'
      },
      {
        id: 2,
        firstName: "Ordi",
        lastName: "Kitoko",
        gender: "female",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/IMG_20240607_135942_589.jpg'
      },
      {
        id: 3,
        firstName: "Terence",
        lastName: "Tweng",
        gender: "male",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/IMG_20240607_150343_596.jpg'
      },
      {
        id: 4,
        firstName: "Kamva",
        lastName: "Banzi",
        gender: "female",
        profile: 'https://mardoqueiro.github.io/all_images/E-com_/Team-photo/Screenshot_20240607_150245_WhatsApp.jpg'
      },
      ]
      };
    },
  };
  </script>
  