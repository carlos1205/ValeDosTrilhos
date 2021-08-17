<template>
    <b-container id="Noticias" fluid >
        <h2 class="text-secondary display-3">{{title}}</h2>
        <b-row align-h="center" >
                <b-col cols="9">
                    <Carrousel />
                </b-col>
            </b-row>
    </b-container>
    
</template>

<script>
    import Carrousel from './Carrousel';
    export default {
        components: {Carrousel},
        data: function () {
            return({
                title: 'Ultimas Noticias'
            });
        }
    };
</script>

<style Scoped>
    #Noticias{
        margin-bottom: 4rem;
    }
    #Noticias h2 {
        width: 45%;
        margin: 5rem auto 4rem;
        text-align: center;
    }
    #Noticias h2::after {
        content: '';
        display: block;
        border: 2px solid #6c757d;
        width: 70%;
        margin: 0 auto;
        margin-top: 1%;
        
    }

</style>