<template>
    <section id="Chancela">
        <h2>{{title}}</h2>
        <article>
            <p v-for="(item, index) in description" :key="index">
                {{item}}
            </p>
        </article>
    </section>
</template>

<script>
    export default {
        data: function(){
            return ({
                title: 'Chancela',
                description: [
                    'Os programas desenvolvidos pelas Secretarias do Município que apresentem maior impacto para os serviços prestados aos munícipes terão a chancela do Vale dos Trilhos, demonstrando o comprometimento de Ponta Grossa em fomentar a criação de um ambiente de negócios propício para a inovação e desenvolvimento sustentável do município de Ponta Grossa, sendo de fato, uma cidade inovadora. '
                ]
            });
        }
    };
</script>