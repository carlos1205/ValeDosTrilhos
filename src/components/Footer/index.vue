<template>
    <footer>
        <p class="text-light">{{copy}}</p>
    </footer>
</template>

<script>
    export default {
        data: function () {
            return ({
                copy: '© Sala do Empreendedor | PMPG'
            });
        }
    }
</script>

<style scoped>
    footer {
        margin-top: 3rem;
        background-color: #212529;
    }
    footer p {
        margin-bottom: 0;
        text-align: center;
    }
</style>