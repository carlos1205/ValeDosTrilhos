<template>
    <header>
        <b-navbar  class="fixed-top" toggleable="lg" type="dark" variant="dark">
            <b-container fluid>
                <a href="#">
                    <img :src="logoHorizontal" class="icon-bar" />
                </a>
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                
                <b-collapse id="nav-collapse" class="justify-content-end" is-nav>

                    <b-navbar-nav class="ml-auto justify-content-between">
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
    import logoHorizontal from '../../assets/img/icon-home-logo-vale.png'

    export default {
        data: function () {
            return ({
                logoHorizontal: logoHorizontal,
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
                }]
            });
        }
    }
</script>

<style scoped>
    .navbar-dark .navbar-nav .nav-link{
        color: white;
        
    }
    .icon-bar{
        width:2rem;
        
    }
</style>