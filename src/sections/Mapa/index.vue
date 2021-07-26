<template>
    <b-container id="Mapa">
        <b-row align-h="center">
            <b-col cols="10">
                <iframe :src="iframe" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
            </b-col>
        </b-row>
        <b-row align-h="center">
            <b-col class="mapaTitle" cols="10">
                <b-row align-h="between">
                    <h2 class="text-light col-9">{{title}}</h2>
                    <a class="col-3 btn btn-outline-light" :href="linkCadastro">{{labelCadastro}}</a>
                </b-row>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
    export default {
        data: function(){
            return ({
                title: 'Mapa de Inovação',
                description: 'Mapa de Inovação',
                iframe: 'https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d28907.56780758095!2d-50.17528109417986!3d-25.08676043576863!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1spt-BR!2sbr!4v1627255006239!5m2!1spt-BR!2sbr',
                linkCadastro: '#',
                labelCadastro: 'Faça Parte'
            });
        }
    };
</script>

<style Scoped>
    #Mapa{
        margin-top: -8rem;
        margin-bottom: 5rem;
    }
    #Mapa iframe{
        width: 100%;
        height: 25rem;
        margin-bottom: -0.4rem;
    }
    #Mapa .mapaTitle div{
        background-color: #632691;
        padding: .5rem .5rem;
        margin: 0;
    }
    #Mapa .mapaTitle div h2{
        margin-bottom: 0;
    }
</style>