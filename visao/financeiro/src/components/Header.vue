<script>
    import { RouterLink } from 'vue-router';
    export default {
        name: 'HeaderComponent',
        components: {
            RouterLink
        }
    }
</script>

<template>
    <header>
        <h1></h1>
        <nav>
            <router-link to="/products"><router-link/>
            <router-link to="/About"><router-link/>
        </nav>
    </header>
</template>