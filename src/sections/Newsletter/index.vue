<template>
    <section id="Newsletter">
        <h2>{{title}}</h2>  
        <p>{{description}}</p>
    </section>
</template>

<script>
    export default {
        data: function() {
            return ({
                title: 'Newsletter',
                description: 'Quer ficar por dentro da nossa newsletter'
            });
        }
    };
</script>