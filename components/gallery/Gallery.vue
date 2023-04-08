<template>
  <div class="gallery">
    <div class="gallery__card">
      <div class="gallery__picked">
        <img
          class="gallery__picked--image"
          :src="pickedImg.url"
          height="450"
          >
      </div>
      <div class="gallery__preview">
        <div
          class="gellery__picker"
          v-for="image in gallery"
          @click="pickImg(image.id)"
          :key="image.id"
          :class="{'gallery__picker--active': (image.id === pickedImg.id)}"
          >
          <img class="gellery__picker--image" :src="image.url" :alt="image.name" height="100">
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      pickedImg: null,
      gallery: [
        {
          id: 0,
          url: 'https://img.freepik.com/free-photo/wide-angle-shot-single-tree-growing-clouded-sky-during-sunset-surrounded-by-grass_181624-22807.jpg',
          name: 'Tree_1'
        },
        {
          id: 1,
          url: 'https://images.unsplash.com/photo-1618588507085-c79565432917?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8YmVhdXRpZnVsJTIwbmF0dXJlfGVufDB8fDB8fA%3D%3D&w=1000&q=80',
          name: 'Tree_2'
        },
        {
          id: 2,
          url: 'https://cdn.corporate.walmart.com/dims4/WMT/f7a8313/2147483647/strip/true/crop/1920x1080+0+0/resize/1200x675!/quality/90/?url=https%3A%2F%2Fcdn.corporate.walmart.com%2F7b%2F66%2F142c151b4cd3a19c13e1ca65f193%2Fbusinessfornature-banner.png',
          name: 'Tree_3'
        },
        {
          id: 3,
          url: 'https://wtop.com/wp-content/uploads/2022/07/AP22193553216841-scaled.jpg',
          name: 'Cosmos'
        },
        {
          id: 4,
          url: 'https://wallpaperaccess.com/full/429863.jpg',
          name: 'Forest'
        },
      ]
    }
  },
  methods: {
    pickImg(id) {
      this.pickedImg = this.gallery.find(img => img.id === id);
    }
  },
  created() {
    this.pickedImg = this.gallery[0];
  },
}
</script>

<style>
  .gallery {
    display: flex;
    justify-content: center;

    margin-top: 15px;
    padding: 15px;
  }

  .gallery__card {
    width: 50%;
    min-width: 700px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;

    border-radius: 5px;
    background-color: whitesmoke;
    padding: 20px;

    overflow: hidden;

    box-shadow: 0 2px 1px -1px #0003, 0 1px 1px #00000024, 0 1px 3px #0000001f;
  }

  .gallery__picked--image {
    max-width: 700px;
    border-radius: 5px;
    box-shadow: 0 2px 1px -1px #0003, 0 1px 1px #00000024, 0 1px 3px #0000001f;
  }

  .gallery__preview {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;

    width: 90%;
    margin-top: 20px;
  }

  .gellery__picker {
    border-radius: 5px;
    margin: 5px;
    transition: 0.5s;
  }

  .gellery__picker:hover {
    cursor: pointer;
    transform: scale(1.1);
    transition: 0.5s;
  }

  .gallery__picker--active {
    transform: scale(1.05);
    z-index: 100;
  }

  .gallery__picker--active > .gellery__picker--image {
    border-radius: 5px;
    transition: 0.2s;

    -webkit-box-shadow: 1px 5px 10px -2px rgba(66, 68, 90, 1);
    -moz-box-shadow: 1px 5px 10px -2px rgba(66, 68, 90, 1);
    box-shadow: 1px 5px 10px -2px rgba(66, 68, 90, 1);
  }

  .gellery__picker--image {
    border-radius: 5px;
    box-shadow: 0 2px 1px -1px #0003, 0 1px 1px #00000024, 0 1px 3px #0000001f;
  }

</style>
