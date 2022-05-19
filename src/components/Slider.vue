<template>
    <div id="sliderContainer">
        <div id="sliderTitle">{{name}}</div>
        <div id="sliderMain">
            <button @click="Back" class="buttonBN" id="buttonBack"><span><fa icon="angle-left"></fa></span></button>
            <button @click="Next" class="buttonBN" id="buttonNext"><span><fa icon="angle-right"></fa></span></button>
            <div id="sliderScroll">
                <Card v-for="index in 20" :key="index" :item="item[0]" :name="name"/>
            </div>
        </div>
    </div>
</template>

<script>
import Card from './Card.vue';

export default {
    props:['item','name'],
    components:{Card},
    data() {
        return {
            number : 1,
        }
    },
    methods: {
        Next(e){

            if(this.number == 4){
                this.number = 0;
            }

            e.path.forEach(element =>{
                if(element.id == "sliderMain"){
                    element.children[2].style.transform = `translateX(${this.number * -100}%)`;
                }
            });
            this.number = this.number + 1;

        },
        Back(e){

            if(this.number <= 1){
                this.number = 5;
            }

            e.path.forEach(element =>{
                if(element.id == "sliderMain"){
                    element.children[2].style.transform = `translateX(${(this.number - 2) * -100}%)`;
                }
            });
            this.number = this.number - 1;

        },
    },
}
</script>