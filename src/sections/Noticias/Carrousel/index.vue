<template>
    <carousel id="news" :responsive="responsive" >
        <a :href="event.link" target="_blank" v-for="(event, index) in events" :key="index">
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
                    600:{
                        items: 5,
                        nav: false
                    }

     
                },
                events: [
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Saúde Financeira da empresa.',
                        title:'Papo Reto com Especialista ep. 7',
                        link:'https://www.facebook.com/watch/live/?v=280620167076240&ref=external'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'E-commerce para pequenos negócios.',
                        title:'Papo Reto com Especialista ep. 6',
                        link:'https://www.facebook.com/watch/live/?v=348099836919958&ref=external'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Cuidados para o setor de alimentos.',
                        title:'Papo Reto com Especialista ep. 5',
                        link:'https://www.facebook.com/watch/live/?v=4311260125574519&ref=external'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Comunicação nas redes sociais.',
                        title:'Papo Reto com Especialista ep. 4',
                        link:'https://www.facebook.com/watch/live/?v=217606766773416&ref=external'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Como trabalhar sua marca na pandemia.',
                        title:'Papo Reto com Especialista ep. 3',
                        link:'https://www.facebook.com/watch/live/?v=350451999760065&ref=external'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'Tudo sobre pix e como ele pode ajudar no seu negócio.',
                        title:'Papo Reto com Especialista ep. 2',
                        link:'https://www.facebook.com/watch/live/?v=455213165921436&ref=watch_permalink'
                    },
                    {
                        image: 'https://placekitten.com/380/200',
                        name: 'O primeiro bate papo do “Papo Reto com Especialista”.',
                        title:'Papo Reto com Especialista ep. 1',
                        link:'https://www.facebook.com/watch/live/?v=694650621178152&ref=watch_permalink'
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