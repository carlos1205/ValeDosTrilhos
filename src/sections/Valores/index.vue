<template>
    <section id="Valores">
        <b-container>
            <h2 class="display-3 text-secondary">
                {{title}}
            </h2>
            <b-row class="justify-content-center" >
                <b-col>
                    <p v-for="(paragraph, index) in description" :key="index">
                        {{paragraph}}
                    </p>
                </b-col>
                <b-col sm="6">
                    <Accordion 
                        :initList="valores"
                    />
                </b-col>
            </b-row>
        </b-container>
    </section>
</template>

<script>
    import Accordion from './Accordion';

    export default {
        components: {Accordion},
        data: function () {
            return ({
                title: 'O que é o Vale dos Trilhos?',
                description: [
                    'Em Ponta Grossa, cidade de oportunidades, o que nos conecta com o futuro é o Vale do Trilhos nosso ecossistema de inovação para construir uma cidade inteligente com essência criativa e inovadora.',
                    'Nosso  ecossistema de inovação para construir uma cidade inteligente com essência criativa e inovadora.'
                ],
                valores: [
                    {
                        name: 'Propósito',
                        description: ['Fomentar a criação de um ambiente de negócios propício para a inovação e desenvolvimento sustentável do município de Ponta Grossa, tendo alinhamento com os objetivos estratégicos do Governo Municipal.'],
                        subList: []
                    },
                    {
                        name: 'Missão',
                        description: ['Catalisar o desenvolvimento de inovações através da desburocratização e simplificação de processos internos e da integração dos atores do ecossistema de inovação de Ponta Grossa, gerando autonomia e melhorando a experiência dos cidadãos e negócios em prol de um desenvolvimento sustentável e da construção de uma cidade inteligente.'],
                        subList: []
                    },
                    {
                        name: 'Visão',
                        description: ['Conectar os atores do ecossistema de inovação de Ponta Grossa promovendo ações que inspirem e capacitem os cidadãos na formação de uma cidade inovadora e inclusiva.'],
                        subList: []
                    },
                    {
                        name: 'Valores',
                        description: null,
                        subList: [
                            'Empoderar os munícipes',
                            'Cultivar o ecossistema de inovação',
                            'Inspirar a inclusão',
                            'Transformar ideias em soluções',
                            'Incentivar a participação democrática'
                        ]
                    }
                ]
            });
        }
    }
</script>

<style scoped>
    #Valores h2 {
        width: 45%;
        margin: 5rem auto 4rem;
        text-align: center;
    }
    #Valores h2::after {
        content: '';
        display: block;
        border: 2px solid #6c757d;
        width: 70%;
        margin: 0 auto;
        margin-top: 1%;
    }
</style>