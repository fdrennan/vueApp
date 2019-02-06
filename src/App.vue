<template>
    <div class="container">
        <sidebar></sidebar>
        <app-header></app-header>
        <!-- <hr> -->
        <!-- <div class="row"> -->
            <!-- <servers></servers> -->
            <!-- <app-server-details></app-server-details> -->
        <!-- </div> -->
        <!-- <hr> -->
        <!-- <app-footer></app-footer> -->
    </div>
</template>

<script>
    import Header from './components/Shared/Header.vue';
    // import Footer from './components/Shared/Footer.vue';
    import Sidebar from './components/Shared/Sidebar.vue';
    // import Servers from './components/Server/Servers.vue';
    // import ServerDetails from './components/Server/ServerDetails.vue';

    export default {
        components: {
            'app-header': Header,
            // Servers,
            // 'app-server-details': ServerDetails,
            // 'app-footer': Footer,
            'sidebar': Sidebar
        }
    }
</script>

<style>

</style>
