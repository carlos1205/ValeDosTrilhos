<template>
    <b-container id="Newsletter">
        <b-row align-h="between"> 
            <b-col cols="6">
                <p class="display-6">
                    {{description}}
                </p>
            </b-col>
            <b-col cols="5">
                <b-form >
                    <b-form-group
                        id="newsletterName"
                        label="Nome:"
                        label-for="nameForNewsletter"
                    >
                        <b-form-input id="nameForNewsletter" required placeholder="Seu Nome"></b-form-input>
                    </b-form-group>

                    <b-form-group
                        id="newsletterEmail"
                        label="Email:"
                        label-for="emailForNewsletter"
                    >
                        <b-form-input id="emailForNewsletter" required placeholder="Digite seu email"></b-form-input>
                    </b-form-group>
                    <b-button pill type="submit" variant="outline-success">Submit</b-button>
                </b-form>
                <video width="400" preload="metadata">
                    <source src="https://www.w3schools.com/html/mov_bbb.mp4#t=8" type="video/mp4">
                </video>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
    export default {
        data: function() {
            return ({
                description: 'Quer ficar por dentro da nossa Newsletter?'
            });
        }
    };
</script>

<style scoped>
    #Newsletter .form-group{
        margin-bottom: .7rem;
    }
    #Newsletter button{
        width: 100%;
    }
    @media(max-width: 479px){
        ::-webkit-input-placeholder {
            font-size:0.6rem;
        }
       #Newsletter{
           font-size:0.8rem;
       }
       p{
           font-size:1.4rem;
       }
    }
</style>