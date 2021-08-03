<template>
    <b-container fluid id="Banner" :style="banner">
        <b-row class="justify-content-center" :style="center" align-v="center">
            <b-img class="logo" :src="logo" fluid/>
        </b-row>
    </b-container>
</template>

<script>
    import imgs from '../../assets/img/bg_vale-dos-trilhos.png';
    import logo from '../../assets/img/logo_vale-dos-trilhos.svg';

    export default {
        data: function() {
            return ({
                title: 'Vale dos Trilhos',
                logo: logo,
                banner: {
                    backgroundImage: `url(${imgs})`,
                    backgroundPosition: 'top',
                    backgroundRepeat: 'no-repeat'
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
        width: 35rem;
        padding-bottom: 20vh;
    }
</style>