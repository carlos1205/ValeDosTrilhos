<template>
    <div :id="`accordion-eixos`" class="accordion" role="tablist">
        <b-card 
            class="mb-1"
            no-body
            v-for="(item, index) in itens"
            :key="index"
        >
           <Card 
                :initTitle="title"
                :initIndex="index"
                :initName="item.name"
                :initDescription="item.description"
                :initColor="item.color"
                :imgName="item.img"
           />
        </b-card>
    </div>
</template>

<script>
    import Card from './Card';

    export default {
        components: {Card},
        props: {
            initList: Array,
            initTitle: String
        },
        data: function() {
            return ({
                title: this.initTitle,
                itens: this.initList
            });
        }
    }
</script>

