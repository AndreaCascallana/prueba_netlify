<template>
    <nav>
        <ul>
            <li><NuxtLink to="/">Página 1</NuxtLink></li>
            <li><NuxtLink to="/pagina2">Página 2</NuxtLink></li>
            <li><NuxtLink to="/pagina3">Página 3</NuxtLink></li>
        </ul>
    </nav>
</template>


<script>
export default {}
</script>


<style lang="scss">

nav {
    padding: 2rem;
    background-color: $bg_color;
    ul {
        display: flex;

        list-style: none;

        li {
            margin-left: 2rem;

            a {
                text-decoration: none;
                color: #333;

                &.nuxt-link-exact-active {
                    font-weight: bold;
                }
            }
        }
    }
}

</style>