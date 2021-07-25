<template>
    <section id="Agenda">
        <b-container>
            <h2 class="display-3 text-light">{{title}}</h2>
            <Carrousel />
        </b-container>
    </section>
</template>

<script>
import Carrousel from './Carrousel';
export default {
    components: {Carrousel},
    data: function () {
        return ({
            title: 'Agenda e Eventos'
        });
    }
};
</script>

<style scoped>
    #Agenda {
        background-color: #bfd730;
        margin-top: 4rem;
        padding-top: 2rem;
        padding-bottom: 2rem;
        margin-bottom: 2rem;
    }
    #Agenda h2{
        margin-bottom: 2rem;
    }
    #Agenda h2::after{
        content: '';
        display: block;
        border: 2px solid #f8f9fa;
        width: 30rem;
        margin-top: 1%;
    }
</style>