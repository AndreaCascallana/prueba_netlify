<template>

    <div>
        <img :src="source" :alt="alternativo">
        <h2>{{ saludo }}</h2>
    </div>
    
</template>


<script>

export default {
    name: "HeaderImage",
    props: ["source", "saludo", "alternativo"]
}

</script>


<style>

</style>
