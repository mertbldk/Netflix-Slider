<template>
  <div id="main">
    <Slider :item="korku.info" :name="korku.name"/>
    <Slider :item="fantastik.info" :name="fantastik.name"/>
    <Slider :item="aksiyon.info" :name="aksiyon.name"/>
  </div>
</template>

<script>
import Slider from './components/Slider.vue';

export default {
  components:{Slider},
  data() {
    return {
      fantastik:{
        name : 'Fantastik Filmleri',
        info : [
          {
            img : 'https://im.haberturk.com/2021/08/06/ver1628260922/3155150_810x458.jpg',
            name : 'Karayip korsanları',
            value : '92%',
            age : '18',
            date : '2sa. 23dk.',
            type : ['Aksiyon','•','Komedi','•','Macera']
          },
        ]
      },
      korku:{
        name : 'Korku Filmleri',
        info : [
          {
            img : 'https://img.paratic.com/dosya/2018/04/dusuk-butcesine-ragmen-gisede-harikalar-yaratan-sessiz-bir-yerin-ikincisi-geliyor-687x400.jpg',
            name : 'Sessiz Bir Yer',
            value : '85%',
            age : '18',
            date : '1sa. 30dk.',
            type : ['Korku','•','Gerilim','•','Bilim Kurgu','•','Dram']
          },
        ]
      },
      aksiyon:{
        name : 'Aksiyon Filmleri',
        info : [
          {
            img : 'https://i01.sozcucdn.com/wp-content/uploads/2019/02/iecrop/hizli-ve-ofkeli-7_16_9_1549537811.jpg',
            name : 'Hızlı ve Öfkeli 7',
            value : '86%',
            age : '18',
            date : '2sa. 20dk.',
            type : ['Aksiyon','•','Macera','•','Suç','•','Gerilim','•','Gizem']
          },
        ]
      },
    }
  },
}
</script>

<style lang="scss">
@import './scss/main.scss';
</style>
