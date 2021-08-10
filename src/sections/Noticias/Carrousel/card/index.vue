<template>
    <b-card
        no-body
        style="max-width: 16rem; box-shadow: 2px 2px 2px grey; margin-bottom: .5rem;"
        :img-src="event.image"
        img-alt="Image"
        img-top
        class="new"
    >
        <b-card-body>
            <b-row>
                <b-col>
                    <p class="text-dark fs-6">
                        <span class="text-dark">
                            {{event.title}}
                        </span>
                    </p>
                    <h3 class="text-dark fs-6">
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
        font-weight: bold;
    }
    .card { 
        background-color: rgba(255, 255, 255, .5);
        
    }
    .card h3 {
        text-align: left;
        text-decoration: none;
       
    }
    .card.new:hover{
        background-color: rgba(0, 0, 0, .2);
    }
    
</style>