<template>
    <div class="container">
        <div class="row">
            <h3>Friends</h3>
        </div>
        <div class="row gap-2">
            <div v-if="friends.length">
              <Card v-for="friend in friends" :key="friend.id" :gender="friend.gender">
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
            <div v-else>
                <span class="loader"></span>
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

  <style>
  .loader {
  display: block;
  width: 84px;
  height: 84px;
  position: relative;
}

.loader:before , .loader:after {
  content: "";
  position: absolute;
  left: 50%;
  bottom: 0;
  width: 64px;
  height: 64px;
  border-radius: 50%;
  background: #FFF;
  transform: translate(-50% , -100%)  scale(0);
  animation: push_401 2s infinite linear;
}

.loader:after {
  animation-delay: 1s;
}

@keyframes push_401 {
  0% , 50% {
    transform: translate(-50% , 0%)  scale(1)
  }

  100% {
    transform: translate(-50%, -100%) scale(0)
  }
}
  </style>
  