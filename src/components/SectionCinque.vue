<template>
  <div class="text-white main d-flex flex-column gap-3 align-items-center">
    <span>
      customer testimonials
    </span>
    <div class="titolo d-flex align-items-center gap-2">
      <h1>Trusted</h1>
      <h1 class="highlight">Feedback</h1>
    </div>
    <span class="width">
      We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for the recognition.
    </span>
    
    <div class="mycard-wrapper d-flex justify-content-between gap-4">
      <div v-for="(item,i) in card" :key="i" class="mycard d-flex flex-column gap-3 flex-grow-1">
        <img :src="item.src" alt="">
        <span>{{item.description}}</span>
        <i class="d-flex justify-content-end fa-solid fa-quote-right"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionCinque',
  data(){
    return{
      card:[
        {
          src: require('../assets/img/logo-1.png'),
          description: "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
        {
          src: require('../assets/img/logo-2.png'),
          description: "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
        {
          src: require('../assets/img/logo-3.png'),
          description: "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '/src/assets/mixin';
@import '/src/assets/variabili';

.main{
  height: 505px;
  background-color: $woodsmoke;
  @include padding-laterale;
  padding-top: 30px;
  font-size: 12px;
  text-align: center;

  span:first-child{
    color: $bluelagoon;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: bold;
  }

  .titolo{
    margin-top: 15px;
    margin-bottom: 15px;
  }

  .highlight{
    padding: 5px 10px;
    background-color: rgba($bluelagoon,0.2);
    border-radius: 5px;
  }

  .width{
    max-width: 50%;
    font-size: 12px;
    color: white;
  }

  .mycard-wrapper{
    margin-top: 30px;

    .mycard{
      width: calc(100% / 4);
      background-color: $shark;
      border-radius: 10px;
      padding: 30px 30px;
      text-align: justify;

      img{
        width: 81px;
        filter: invert(1);
      }
    
      i{
        font-size: 20px;
        color: $midgray;
      }
    }
  }

  
}
</style>