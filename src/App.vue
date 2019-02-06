<template>
    <div class="container">
        <sidebar></sidebar>
        <app-header></app-header>
        <main-div></main-div>
        <!-- <hr> -->
        <!-- <div class="row"> -->
            <!-- <servers></servers> -->
            <!-- <app-server-details></app-server-details> -->
        <!-- </div> -->
        <!-- <hr> -->
        <app-footer></app-footer>
    </div>
</template>

<script>
    import Header from './components/Shared/Header.vue';
    import Footer from './components/Shared/Footer.vue';
    import Sidebar from './components/Shared/Sidebar.vue';
    import Main from './components/Shared/Main.vue';
    // import Servers from './components/Server/Servers.vue';
    // import ServerDetails from './components/Server/ServerDetails.vue';

    export default {
        components: {
            'sidebar': Sidebar,
            'app-header': Header,
            'main-div': Main,
            // Servers,
            // 'app-server-details': ServerDetails,
            'app-footer': Footer
        }
    }

</script>

<style scoped>
body {
    background-color: rgb(28, 28, 28, .1);
}
</style>
