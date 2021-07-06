<template>
    <div :id="`accordion-${title}`" class="accordion" role="tablist">
        <b-card 
            class="mb-1"
            no-body
            v-for="(item, index) in itens"
            :key="index"
        >
            <b-card-header header-tag="header" class="p-0" role="tab">
                <b-button 
                    v-b-toggle="`accordion-${title}-${index}`"
                    block
                >
                    {{item.name}}
                </b-button>
            </b-card-header>
            <b-collapse
                :id="`accordion-${title}-${index}`"
                accordion="`accordion-${title}-${item.name}`"
                role="tabpanel"
            >
                <b-card-body>
                    <b-card-text
                        v-for="(paragraph, number) in item.description"
                        :key="`${title}-${index}-P${number}`"
                    >
                        {{paragraph}}
                    </b-card-text>
                </b-card-body>
            </b-collapse>
        </b-card>
    </div>
</template>

<script>
    export default {
        props: {
            initList: Array
        },
        data: function() {
            return ({
                itens: this.initList
            });
        }
    }
</script>