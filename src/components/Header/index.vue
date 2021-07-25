<template>
    <header>
        <b-navbar toggleable="lg" type="dark" variant="dark">
            <b-container fluid>
                <b-navbar-brand href="#">{{name}}</b-navbar-brand>

                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                
                <b-collapse id="nav-collapse" class="justify-content-end" is-nav>

                    <b-navbar-nav class="ml-auto">
                        <b-nav-item v-for="(item, index) in sections" :key="index" v-bind:href="'#'+item.id" right>
                            {{item.name}}
                        </b-nav-item>
                    </b-navbar-nav>

                </b-collapse>
            </b-container>
        </b-navbar>
    </header>
</template>

<script>
    export default {
        data: function () {
            return ({
                name: 'Vale dos Trilhos',
                sections: [{
                    name: 'Contexto Inicial',
                    id: 'Context'
                },
                {
                    name: 'Vale dos Trilhos',
                    id: 'Valores'
                },
                {
                    name: 'Eixos',
                    id: 'Eixos'
                },
                {
                    name: 'Chancela',
                    id: 'Chancela'
                },
                {
                    name: 'Agenda e Eventos',
                    id: 'Agenda'
                },
                {
                    name: 'Mapa de inovação',
                    id: 'Mapa'
                },
                {
                    name: 'Noticias',
                    id: 'Noticias'
                }]
            });
        }
    }
</script>

<style scoped>
    .navbar-dark .navbar-nav .nav-link{
        color: white;
    }
</style>