<template>
    <Fragment>
        <b-card-header header-tag="header" class="p-0" role="tab">
            <b-button
                v-b-toggle="`accordion-${title}-${index}`"
                block
                :style="styleObject"
            >   
                <img :src="img"/>
                <label>
                    {{name}}
                </label>
            </b-button>
        </b-card-header>
        <b-collapse
            :id="`accordion-${title}-${index}`"
            accordion="`accordion-${title}-${name}`"
            role="tabpanel"
        >

            <b-card-body>
                <b-card-text
                    v-for="(paragraph, number) in description"
                    :key="`${title}-${index}-P${number}`"
                >
                    {{paragraph}}
                </b-card-text>
            </b-card-body>

        </b-collapse>
    </Fragment>
</template>

<script>
    import {Fragment} from 'vue-fragment';

    export default {
        components: {Fragment},
        props: {
            initTitle: String,
            initIndex: Number,
            initName: String,
            initDescription: Array,
            initColor: String,
            imgName: String
        },
        data: function() {
            return ({
                title: this.initTitle,
                index: this.initIndex,
                name: this.initName,
                description: this.initDescription,
                color: this.initColor,
                img: require('../../../../assets/img/' + this.imgName)
            });
        },
        computed: {
            styleObject: function(){
                return {
                    '--color-hover': this.color
                }
            }
        }
    }
</script>

<style scoped>
    .card-header{
        border-bottom: none;
    }
    button{
        width: 100%;
        height: 4rem;
        transition: linear .5s;
        font-size: 1.25rem;
        display: flex;
        align-items: center;
    }
    button label{
        text-align: right;
        flex: 25;
        cursor: pointer;
    }
    button img{
        flex: 1;
        width: 2rem;
        cursor: pointer;
    }
    button:focus{
        outline: none;
        box-shadow: none;
    }
    button:hover, button:focus, button.not-collapsed{
        background-color: var(--color-hover);
        border-color: var(--color-hover);
    }
   @media(max-width: 479px){
       button{
           font-size:0.8rem;
       }
   }
   </style>