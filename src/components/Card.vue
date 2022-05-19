<template>
    <div id="sliderCardCap">
        <div id="sliderCardBack">
            <img :src="item.img">
            <p>{{item.name}}</p>
        </div>
        <div id="sliderCardFront">
            <div id="sliderCardImg">
                <img :src="item.img">
            </div>
            <div id="sliderCardİnformations">
                <div id="cardControll">
                    <div id="cardControllLeft">
                        <div><fa icon="play"></fa></div>
                        <div><fa icon="plus"></fa></div>
                        <div><fa icon="thumbs-up"></fa></div>
                        <div><fa icon="thumbs-down"></fa></div>
                    </div>
                    <div id="cardControllRight">
                        <div><fa icon="chevron-down"></fa></div>
                    </div>
                </div>
                <div id="cardİnfo">
                    <div id="cardİnfoPercentage">{{item.value}} Eşleme</div>
                    <div id="cardİnfoAge">{{item.age}}+</div>
                    <div id="cardİnfoDuraction">
                        <span id="cardİnfoDuc">{{item.date}}</span>
                        <span id="cardİnfoHd">HD</span>
                    </div>
                </div>
                <ul id="cardType">
                    <li v-for="(i,ı) in item.type" :key="ı">{{i}}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['item'],
}
</script>