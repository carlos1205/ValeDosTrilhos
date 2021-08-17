<template>
    <section id="Context">
        <b-container>
            <h2 class="display-3 text-secondary text-center">{{title}}</h2>
            <b-row class="justify-content-center">
                <p v-for="(paragraph, index) in text" :key="index">
                    {{paragraph}}
                </p>
            </b-row>
        </b-container>
    </section>
</template>

<script>
    export default {
        data: function () {
            return ({
                title: 'Contexto Inicial',
                text: [
                    'Ponta Grossa, cidade de oportunidades, tem passado por um processo de aceleração decorrente das mudanças causadas pelo crescimento exponencial da ciência e tecnologia, assim, a gestão pública através da Agência de Inovação, tem em seu planejamento a melhoria da eficiência e da produtividade dos processos.',
                    'À medida que a realidade se torna cada vez mais complexa, tem-se como estratégia a antecipação de possibilidades e tendências com foco na construção de um futuro sustentável, assim, queremos que a inovação esteja no nosso DNA, tendo uma genuína cultura de inovação.',
                    'Para tanto, a construção de uma cidade inteligente com essência criativa e inovadora se dá através da governança do ecossistema de inovação dos Campos Gerais, intitulada Vale dos Trilhos.'
                ]
            });
        }
    }
</script>

<style scoped>
    #Context {
        margin-top: 4rem;
        margin-bottom: 4rem;
        
    }
    #Context h2{
        margin-bottom: 2rem;
    }
    #Context h2::after{
        content: '';
        
        display: block;
        border: 2px solid #6c757d;
        width: 40%;
        margin: 0 auto;
        margin-top: 1%;
        justify-content: center;
    }
</style>