<template>
    <carousel :responsive="responsive" :nav="false" >
        <Card v-for="(event, index) in events" :key="index" :event="event"/>
    </carousel>
</template>

<script>
    import Card from './Card';
    import carousel from 'vue-owl-carousel';
    import evento1 from '../../../assets/img/banner-evento1.jpg';
    import evento2 from '../../../assets/img/banner-evento2.jpg';
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
                        items: 2,
                        nav: false
                    }
                },
                events: [
                    {
                        date: {
                            day: '18',
                            month: 'AGO'
                        },
                        image: evento1,
                        name: 'Como Design Sprint pode auxiliar o seu negócio',
                        link: 'https://www.sympla.com.br/como-design-sprint-pode-auxiliar-o-seu-negocio__1291049'
                    },
                    {
                        date: {
                            day: '25',
                            month: 'AGO'
                        },
                        image: evento2,
                        name: 'Como Scrum pode auxiliar o seu negócio',
                        link:'https://www.sympla.com.br/como-scrum-pode-auxiliar-o-seu-negocio__1291058'
                    },
                ]
            });
        }
    }
</script>