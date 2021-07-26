<template>
    <carousel :responsive="responsive" :nav="false">
        <Card v-for="(event, index) in events" :key="index" :event="event"/>
    </carousel>
</template>

<script>
    import Card from './Card';
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
                        items: 3,
                        nav: false
                    }
                },
                events: [
                    {
                        date: {
                            day: '09',
                            month: 'JUL'
                        },
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        date: {
                            day: '09',
                            month: 'JUL'
                        },
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        date: {
                            day: '09',
                            month: 'JUL'
                        },
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        date: {
                            day: '09',
                            month: 'JUL'
                        },
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                    {
                        date: {
                            day: '09',
                            month: 'JUL'
                        },
                        image: 'https://placekitten.com/380/200',
                        name: 'Semana Empreendedora'
                    },
                ]
            });
        }
    }
</script>