<template>
    <section id="Eixos">
        <b-container>
            <h2 class="display-3 text-secondary">{{title}}</h2>
            <Accordion :initList="itens" :title="title"/>
        </b-container>
    </section>
</template>

<script>
    import Accordion from './Accordion';
    export default {
        components: {Accordion},
        data: function(){
            return({
                title: 'Eixos',
                itens: [
                    {
                        name: 'Comunidade participativa e gestão democrática',
                        description: [
                            'A cidade é um espaço coletivo, assim, o eico contempla a parceria entre a gestão pública e o cidadão. Todos podem se mobilizar e participar do processo de tomada de decisão das diversas áreas do minicípio.'
                        ],
                        color: '#f70889',
                        img: 'icon-comunidade-participativa-gestao-democratica-preenchida.png'
                    },
                    {
                        name: 'Democratização tecnológica e inclusão digital',
                        description: [
                            'Ter iniciativas que ampliem o acesso à tecnologia assim como capacitar as comunidades para interagirem digitalmente, possibilitando que o cidadão se torne autônomo em sua própria jornada, vislumbrando os benefícios que a tecnologia pode trazer às pessoas'
                        ],
                        color: '#3dc1ff',
                        img: 'icon-democratizacao-tecnologica-inclusao-digital.png'
                    },
                    {
                        name: 'Educação e Empreendedorismo',
                        description: [
                            'Considera desde a infância o desenvolvimento de habilidades fundamentais para a vida, em uma formação plural, e, que as pessoas sejam capazes de solucionar problemas e empreenderem a partir de iniciativas inovadoras e integradas com as novas tecnologias. Contempla as oportunidades para empresas e startups que possam influenciar positivamente a construção do futuro da humanidade.'
                        ],
                        color: '#ff4b22',
                        img: 'icon-educacao-empreendedorism.png'
                    },
                    {
                        name: 'Fomento e desenvolvimento',
                        description: [
                            'A promoção do desenvolvimento local e setorial a partir do fortalecimento dos negócios, da interação entre o público e privado, orientado a diposição de recursos, estrutura e execução de projetos que impulsionem o aumento da capacidade competitiva e o protagonismo dos atores locais.'
                        ],
                        color: '#bfd730',
                        img: 'icon-fomento-desenvolvimento.png'
                    },
                    {
                        name: 'Integração e cooeperação',
                        description: [
                            'O ecossistema de inovação de Ponta Grossa unirá esforços em prol do desenvolvimento conjunto de atividades que promovam o desenvolvimento sustentável. Os atores do ecossistema são: Instituições de Ensino, Entidades de Classe, Órgãos Públicos, Indústrias, Comércio, Terceiro Setor e Empresas norteados po uma cultura inovadora.'
                        ],
                        color: '#ffcb05',
                        img: 'icon-integracao-cooperacao.png'
                    },
                    {
                        name: 'Simplificação e desburocratização',
                        description: [
                            'Este eixo contempla a facilitação e modernização nos processos municipais, a geração da autonomia do cidadão através de um Governo Inteligente com o desenvolvimento amparado legalmente com base nos princípios preconizados na Lei de Liberdade Econômica e nas seis dimensões do Gorverno Digital preconizadas pelo OCDE.'
                        ],
                        color: '#6950a1',
                        img: 'icon-simplicacao-desburocratizacao.png'
                    }
                ]
            });
        }
    }
</script>

<style scoped>
    #Eixos {
        margin-top: 4rem;
        margin-bottom: 2rem;
    }
    #Eixos h2{
        margin-bottom: 2rem;
    }
    #Eixos h2::after{
        content: '';
        display: block;
        border: 2px solid #6c757d;
        width: 8rem;
        margin-top: 1%;
    }
</style>