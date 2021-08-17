<template>
    <Fragment>
        <b-card
            no-body
            style="max-width: 18rem;"
            :img-src="event.image"
            img-alt="Image"
            img-top
        >
            <b-card-body>
                <b-row>
                    <b-col cols="4">
                        <p class="text-dark fs-6 date">
                            <span>
                                {{event.date.day}}
                            </span>
                            <span>
                                {{event.date.month}}                                
                            </span>
                        </p>
                    </b-col>
                    <b-col cols="8">
                        <h3 class="fs-6 name">
                            {{event.name}}
                        </h3>
                    </b-col>
                </b-row>
            </b-card-body>

            <b-card-footer>
                <b-button :href="event.link" target="_blank" variant="outline-secondary">Ver Mais</b-button>
            </b-card-footer>
        </b-card>
    </Fragment>
</template>

<script>

    import {Fragment} from 'vue-fragment';
    
    export default {
        components: { Fragment},
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

<style scoped>
    span {
        font-weight: bolder;
    }
    .card { 
        background-color: rgba(255, 255, 255, .5);
        box-shadow: 5px 5px 5px grey;
        margin-bottom: .5rem;
    }
    .card .date {
        
        background-color: #ffcb05;
        margin-bottom: 0.5rem;
        border-radius: 0.3rem;
        padding-left: .5rem;
    }
    .card .name{
        padding-bottom: 0.5rem;
    }
    .card-footer {
        text-align: end;
    }
</style>