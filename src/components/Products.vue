<template>
    <div class="container">
      <div class="row">
        <h3 class="display-2">Products</h3>
      </div>
      <div class="row gap-2">
        <Card v-for="product in products" :key="product.id">
          <template #cardheader>
              <img class="img-fluid" :src="product.image" :alt="product.productName" loading="lazy">
              {{ product.productName }}</template>
          <template #cardbody>
            <p>Description: {{ product.description }}</p>
            <p>Price: {{ product.price }}</p>
            <p>Status: {{ product.status }}</p>
          </template>
        </Card>
      </div>
    </div>
  </template>
  
  <script>
  import Card from './Card.vue';
  
  export default {
    name: 'ProductComp',
    components: {
      Card,
    },
    data() {
      return {
        products:[
        {
          id: 1,
          productName: "Custom Cassette Bluetooth Speaker by sab_3d",
          description:
            "sab_3d custom-designed Bluetooth speaker, resembling a cassette tape, offers wireless streaming rechargeablebattery, and high-quality sound, making it a nostalgic conversation starter.",
          price: "R2799.99",
          image: "https://mardoqueiro.github.io/all_images/E-com_/Retro_Products/Retro.Queiro.record.player.jpeg",
          status: "Available"
            
        },
        {
          id: 2,
          productName: "Retro Style Headphones with SD Card and Bluetooth",
          description:
            "These retro-style headphones feature Bluetooth, an SD card slot, cushioned ear cups, leather headband, and metalaccents, blending classic design with modern functionality.",
          price: "R1399.99",
          image: "https://mardoqueiro.github.io/all_images/E-com_/Retro_Products/Retro.Queiro.Headphone.jpeg",
          status: "Available"
        },
        {
          id: 3,
          productName: "Vintage Bluetooth Speaker with Display",
          description:
            "This vintage-style Bluetooth speaker features a 1950s radio design, digital display, Apple Music and Spotifysupport, and retro dials, adding a touch of nostalgia to any room.",
          price: "R2499.99",
          image: "https://mardoqueiro.github.io/all_images/E-com_/Retro_Products/Retro.Queiro.Bluetooth.Speaker.jpeg",
          status: "Out of stock"
        },
        {
          id: 4,
          productName: "Classic Portable Record Player",
          description: "This portable record player, with a retro design and built-in speaker, offers a convenient way to enjoy your vinyl  collection on the go.",
          price: "R1699.99",
          image: "https://mardoqueiro.github.io/all_images/E-com_/Retro_Products/Retro.Queiro.Vinyl.Portable.Turntable.jpeg",
          status: "Out of stock"
        },
        {
          id: 5,
          productName: "Classic Jukebox with Karaoke and Streaming",
          description: "This retro jukebox features modern features like karaoke, AM/FM radio, Bluetooth, and Spotify & Apple Musicsupport, with vibrant LED lights and a classic design for home entertainment.",
          price: "R5499.99",
          image: "https://mardoqueiro.github.io/all_images/E-com_/Retro_Products/Retro.Queiro.Jukebox.jpeg",
          status: "Out of stock"
        },
        {
          id: 6,
          productName: "Retro Game Boy Gaming Console",
          description:
            "The Retro Game Boy Gaming Console offers a nostalgic gaming experience with its modern design, color LCDscreen rechargeable battery, and pre-loaded 300 classic games.",
          price: "R1499.99",
          image: "https://mardoqueiro.github.io/all_images/E-com_/Retro_Products/Retro.Queiro.Gaming.Console.jpeg",
          status: "Available"
        },
      ]
      };
    },
  };
  </script>
  