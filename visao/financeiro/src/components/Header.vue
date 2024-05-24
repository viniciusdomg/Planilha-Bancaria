<script>
    import { RouterLink } from 'vue-router';
    export default {
        name: 'HeaderComponent',
        computed: {
            pagina() {
                return this.$route.path
            }
        },
        components: {
            RouterLink
        }
    }
</script>

<template>
    <header class="container">
        <h1>FinanTrack</h1>
        <nav class="nav-home" v-show="pagina==='/'">
            <a href="#features">Features</a>
            <a href="#blog">Blog</a>
            <a href="#contact">Contact</a>
            <router-link to="/login">
                <button class="btnSign">Sign Up</button>
            </router-link>
        </nav>
        <nav v-show="pagina==='/FinanTrack'">

        </nav>
    </header>
</template>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&family=Titillium+Web:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700&display=swap');
    
    .container {
        display: flex;
        justify-content: space-between;
        padding: 15px 55px;
    }

    h1 {
        margin: 0;
        font-family: "Titillium Web", sans-serif;
        font-weight: 400;
        font-style: normal;
    }

    a{
        text-decoration: none;
        color: inherit;
        font-family: sans-serif;
        transition: transform 0.3s;
    }

    a:hover{
        color: #FFFF99; 
        transform: scale(1.1);
    }

    .nav-home{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 25em;
    }

    .btnSign{
        height: 40px;
        width: 100px;
        background-color: #DDA0DD;
        font-family: sans-serif;
        font-size: 17px;
        border: none;
        cursor: pointer;
        transition: background-color 0.3s, transform 0.3s;
    }

    .btnSign:hover{
        background-color: #FFFF99; 
        transform: scale(1);
    }

</style>