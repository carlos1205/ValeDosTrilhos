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
                    <a class="col-3 btn btn-outline-light" :href="linkCadastro" target="_blank">{{labelCadastro}}</a>
                </b-row>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
    export default {
        data: function(){
            return ({
                description: 'Mapa de Inovação',
                iframe: 'https://www.google.com/maps/d/u/0/embed?mid=1keVxvbqhj7df8dH95oUPABweNtJQ94f9',
                linkCadastro: 'https://docs.google.com/forms/d/e/1FAIpQLSeMpjjSRj4kNPk6UagJlvzreqEse4t7VPBeHFlHuONbeazZ6Q/viewform?usp=sf_link',
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