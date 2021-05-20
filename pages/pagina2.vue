<template>
  <div>
    <header-image :source="'/img1.jpg'" :alternativo="'Imagen de un tlfn'" />

    <h1>Holaaaaa</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet
      perferendis, assumenda accusamus laudantium magnam cumque cupiditate
      provident doloremque quos reprehenderit est et iure consequuntur odio
      veniam culpa dolor atque hic.
    </p>

    <p v-if="$fetchState.pending">Fetching mountains...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p>
    <div v-else>
      <h1>Nuxt Mountains</h1>
      <ul>
        <li v-for="mountain of mountains" :key="mountain.updateAt">{{ mountain.title + ' ' + mountain.height }}</li>
      </ul>
      <button @click="$fetch">Refresh</button>
    </div>

  </div>
</template>


<script>
import HeaderImage from "../components/HeaderImage.vue";
export default {
    components: { HeaderImage },
    data() {
      return {
        mountains: []
      }
    },
    async fetch() {
      this.mountains = await fetch(
        'https://api.nuxtjs.dev/mountains'
      ).then(res => res.json())
    }
};
</script>


<style lang="scss">
div {
  h1 {
    color: tomato;
  }
}
</style>