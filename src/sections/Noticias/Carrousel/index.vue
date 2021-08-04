<template>
    <carousel id="news" :responsive="responsive" >
        <a href="#" v-for="(event, index) in events" :key="index">
            <Card  :event="event"/>
        </a>
    </carousel>
</template>

<script>
    import Card from './card';
    import carousel from 'vue-owl-carousel';

    export default {
        components: {
            Card,
            carousel
        },
        data: function (){
            return ({
                responsive: {
                    0:{
                        items: 1,
                        nav: false
                    },
                    600: {
                        items: 4,
                        nav: false
                    },
                    900: {
                        items: 5,
                        nav: false
                    }
                },
                events: [
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    }
                ]
            });
        }
    }
</script>

<style Scoped>
    #news a{
        text-decoration: none !important;
    }
   
</style>