<template>
  <div class="d-flex text-white gap-5 main justify-content-between">
    <div class="col-3 d-flex flex-column gap-3">
    <div class="titolo fw-bold text-uppercase d-flex align-items-center">
      <div class="bg-blue d-flex justify-content-end align-items-center">
        <h4>nex</h4>
      </div>
      <h4>gen</h4>
    </div>
    <span>A Functional HTML Template for Corporate & Business.</span>
    <div class="d-flex flex-column gap-2">
      <div>
        <i class="fa-solid fa-phone"></i>
        <span>+1 (305) 1234-5678</span>
      </div>
      <div>
        <i class="fa-solid fa-envelope"></i>
        <span>hello@example.com</span>
      </div>
      <div>
        <i class="fa-solid fa-location-dot"></i>
        <span>Main Avenue, 987</span>
      </div>
    </div>
    <button class="bottone">get in touch</button>
    </div>
    <div class="mycard-wrapper col-9 d-flex gap-5">
      <div v-for="(item,i) in card" :key="i" class="mycard d-flex flex-column gap-3">
        <h5>{{item.title}}</h5>
        <ul>
          <li v-for="(element,j) in item.content" :key="j"><i class="fa-solid fa-chevron-right"></i>{{element}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyFooter',
  data(){
    return{
      card:[
        {
          title: 'About',
          content: ['The Company','Institutional','Social & Events','Innovation','Environment','Technology'],
        },
        {
          title: 'Transport',
          content: ['Industrialized','Chemicals','Packaged Liquids','Construction','Laminated Wood','And others'],
        },
        {
          title: 'Support',
          content: ['Responsibility','Terms of Use','About Cookies','Privacy Policy','Accessibility','Information'],
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '/src/assets/mixin';
@import '/src/assets/variabili';
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.main{
  height: 545px;
  background-color: $woodsmoke;
  @include padding-laterale;
  padding-top: 50px;
  font-size: 12px;

  .blue{
    color: $fountainblue;
  }

  .titolo{
    margin-top: 20px;
    margin-bottom: 15px;
    letter-spacing: 6px;
  }

  .bg-blue{
    background-color: rgba($bluelagoon, 0.2);
    height: 50px;
    width: 90px;
    border-top-left-radius: 40px;
    border-bottom-left-radius: 40px;
    color: $fountainblue;
  }

  .bottone{
    border: 2px solid $bluelagoon;
    border-radius: 5px;
    padding: 10px 20px;
    text-transform: uppercase;
    width: 170px;
    background-color: transparent;
    color: white;

    &:hover{
      color: $bluelagoon;
      border:  2px solid transparent;
      background-color: white;
    }
  }

  .col-3 i{
    margin-right: 10px;
  }

  .mycard-wrapper{
    margin-top: 30px;
  }
  .mycard{
    height: 215px;
    width: 170px;
    background-color: rgba(white,0.1);
    border-radius: 10px;
    padding: 20px;

    ul{
      list-style: none;
      padding: 0;

      i{
        margin-right: 10px;
      }
    }
  }
}
</style>
