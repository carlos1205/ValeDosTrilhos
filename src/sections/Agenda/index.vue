<template>
    <section id="Agenda">
        <b-container>
            <h2 class="display-3 text-secondary text-center">{{title}}</h2>
            <b-row>
                <p class="text-dark " v-for="(paragraph, index) in apresentacao" :key="index"></p>
            </b-row>
            <b-row align-h="center" >
                <b-col cols="6">
                    <Carrousel />
                </b-col>
            </b-row>
        </b-container>
    </section>
</template>

<script>

import Carrousel from './Carrousel';
export default {
    components: {Carrousel},
    data: function () {
        return ({
            title: 'Agenda e Eventos',
            apresentacao: [
                    {
                        href: '#',
                        link: 'Cadastre seu evento'
                    }
            ]
        });
    }
};
</script>

<style scoped>
    #Agenda {
        background-color: white;
        margin-top: 4rem;
        padding-top: 2rem;
        padding-bottom: 8rem;
        margin-bottom: 6rem;
    }
    #Agenda h2{
        margin-bottom: 2rem;
    }
    #Agenda h2::after{
        content: '';
        display: block;
        border: 2px solid #6c757d;

        width: 50%;
        margin: 0 auto;
        margin-top: 1%;
    }
    #Agenda p {
        text-align: center;
        margin-bottom: 2rem;
    }
    
</style>