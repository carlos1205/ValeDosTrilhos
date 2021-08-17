<template>
    <div id="accordion" class="accordion" role="tablist">
        <b-card 
            class="mb-1"
            no-body
            v-for="(item, index) in List"
            :key="index"
        >
            <b-card-header header-tag="header" class="p-0" role="tab">
                <b-button 
                    v-b-toggle="`accordion-${index}`"
                    block
                    :style="{
                        backgroundColor: `rgb(${colorButton[index]})`,
                        borderColor: `rgb(${colorButton[index]})`
                    }"
                >
                    {{item.name}}
                </b-button>
            </b-card-header>
            <b-collapse
                :id="`accordion-${index}`"
                accordion="`accordion-${item.name}`"
                role="tabpanel"
            >
                <b-card-body>
                    <b-card-text
                        v-for="(paragraph, number) in item.description"
                        :key="`${index}-P${number}`"
                    >
                        {{paragraph}}
                    </b-card-text>
                    <b-card-text>
                        <ul>
                            <li
                                v-for="(element, number) in item.subList"
                                :key="`${index}-L${number}`"
                            >
                                {{element}}
                            </li>
                        </ul>
                    </b-card-text>
                </b-card-body>
            </b-collapse>
        </b-card>
    </div>
</template>

<script>
    const getButtonsColor = (size) => {
        var R = 247, G = 8, B = 137;
        const colors = [];
        for(let i = 0; i < size; i++){
            //RGB
            colors.unshift(`${R}, ${G}, ${B}`);
            
        }

        return colors;
    }
    export default {
        props: {
            initList: Array
        },
        data: function(){
            return ({
                colorButton: getButtonsColor(this.initList.length),
                List: this.initList
            });
        }
    }
</script>

<style scoped>
    #accordion .card-header{
        border-bottom: none;
    }
    #accordion button{
        width: 100%;
    }
    #accordion button:focus{
        outline: none;
        box-shadow: none;
    }
    #accordion p{
        font-size: 1rem;
    }
</style>