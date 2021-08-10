<template>
    <section id="Agenda">
        <b-container>
            <h2 class="display-3 text-secondary text-center">{{title}}</h2>
            
            <b-row align-h="center" >
                <b-col cols="6">
                    <Carrousel />
                </b-col>
            </b-row>
            <b-row>
                <p class="text-dark " v-for="(paragraph, index) in apresentacao" :key="index">
                   {{paragraph.text}}
                   <a class="btn btn-primary" :href="paragraph.href">{{paragraph.link}}</a>
                </p>
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
                        text: "Lorem ipsum felis ultricies sit donec ligula hendrerit, faucibus mattis aliquam eros gravida eros elementum, netus quam vel litora eleifend curabitur. porta maecenas amet mi iaculis tempor pulvinar, eros blandit gravida curabitur est ut netus, leo nullam tincidunt molestie senectus",
                        href: '#',
                        link: 'Cadastre seu evento.'
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
        margin-bottom: 2rem;
    }
    #Agenda h2{
        margin-bottom: 3rem;
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
        margin-top: 2rem;
    }
    
</style>