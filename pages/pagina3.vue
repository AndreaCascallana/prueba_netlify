<template>

    <div>
        <header-image :source="'/img2.jpg'" :saludo="'hola'" :alternativo="'Imagen de París'" />
        <h1>Página 3</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus, omnis asperiores iusto illo temporibus atque harum quis sed distinctio libero. Dolorum repellendus aliquid pariatur asperiores soluta non expedita perferendis recusandae.</p>
    </div>
    
</template>


<script>
import HeaderImage from '../components/HeaderImage.vue'
export default {
  components: { HeaderImage },}
</script>


<style lang="scss">

</style>