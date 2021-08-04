<template>
    <section id="Chancela">
        <b-container>
            <b-row>
                <b-col cols="4">
                    <img :src="chancela" />
                </b-col>
                <b-col>
                    <h2 class="display-3 text-secondary">{{title}}</h2>
                    <p v-for="(item, index) in description" :key="index">
                        {{item}}
                    </p>
                    <div>
                        <a class="btn btn-primary" :href="`${Contato.link}`">
                            <label> {{Contato.tipo}}:</label>
                            {{Contato.value}}
                        </a>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </section>
</template>

<script>
    import chancela from '../../assets/img/843471.png'
    export default {
        data: function(){
            return ({
                chancela: chancela,
                title: 'Chancela',
                description: [
                    'Os programas desenvolvidos pelos atores do ecossistema do Município que apresentem maior impacto para a comunidades terão a chancela do Vale dos Trilhos, demonstrando o comprometimento de Ponta Grossa em fomentar a criação de um ambiente de negócios propício para a inovação e desenvolvimento sustentável do município de Ponta Grossa, sendo de fato, uma cidade inovadora. '
                ],
                Contato: {
                    tipo: 'Email',
                    link: 'mailto://valedostrilhos@gmail.com',
                    value: 'valedostrilhos@gmail.com'
                }
            });
        }
    };
</script>

<style scoped>
    
    #Chancela {
        margin-top: 7rem;
        margin-bottom: 4rem;
    }

    #Chancela img {
        width: 100%;
    }
    #Chancela h2{
        margin-bottom: 2rem;
    }
    #Chancela h2::after{
        content: '';
        display: block;
        border: 2px solid #6c757d;
        width: 40%;
        
        margin-top: 1%;
    }
    #Chancela a{
        text-align: left;
    }
    #Chancela a label {
        font-weight: bolder;
        cursor: pointer
    }

</style>