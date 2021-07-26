<template>
    <b-card
        no-body
        style="max-width: 15rem;"
        :img-src="event.image"
        img-alt="Image"
        img-top
        class="new"
    >
        <b-card-body>
            <b-row>
                <b-col>
                    <h3 class="text-secondary">
                        {{event.name}}
                    </h3>
                </b-col>
            </b-row>
        </b-card-body>
    </b-card>
</template>

<script>
    
    export default {
        props: {
            event: Object
        },
        data: function(){
            return({
                currentEvent: this.event
            });
        }
    }
</script>

<style Scoped>
    span {
        font-weight: bolder;
    }
    .card { 
        background-color: rgba(255, 255, 255, .5);
    }
    .card h3 {
        text-align: left;
        font-size: 1.2rem;
        text-decoration: none;
    }
    .card.new:hover{
        background-color: rgba(0, 0, 0, .2);
    }
</style>