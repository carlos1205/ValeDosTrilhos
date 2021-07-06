<template>
    <b-container fluid id="Banner" :style="banner">
        <b-row class="justify-content-center" :style="center" align-v="center">
            <b-img class="logo" :src="logo" fluid/>
        </b-row>
    </b-container>
</template>

<script>
    import imgs from '../../assets/img/estacaoDaSaudade.jpg';
    import logo from '../../assets/img/logo-negativa-hor-pos.png';

    export default {
        data: function() {
            return ({
                title: 'Vale dos Trilhos',
                logo: logo,
                banner: {
                    backgroundImage: `url(${imgs})`,
                    backgroundPosition: 'bottom',
                    backgroundRepeat: 'no-repeat',
                    backgroundSize: 'cover'
                },
                center: {
                    height: '100%'
                }
            });
        }
    };
</script>

<style>
    #Banner{
        width: 100%;
        height: 100vh;
        max-height: 100%;
    }
    #Banner .logo{
        width: 40rem;
    }
</style>