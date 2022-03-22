<template>
  <div class="text-white main">
    <span class="blue fw-bold text-uppercase">road transport</span>
    <div class="titolo fw-bold d-flex">
      <h1>Main</h1>
      <h1 class="bg-blue">Services</h1>
    </div>
    <div class="d-flex align-items-center justify-content-between">
      <span class="col-8" >With all of this expertise and capability comes an unrivalled commitment to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.</span>
      <div class="d-flex bottone bottone_main">
        see all
      </div>
    </div>
    <div class="mycard-wrapper d-flex justify-content-between gap-4">
      <div v-for="(item,i) in card" :key="i" class="mycard d-flex flex-column gap-3 flex-grow-1">
        <div class="d-flex justify-content-between">
          <div class="icona-mycard"><i :class="item.icon" class="fa-solid"></i></div>
          <i class="arrow fa-solid fa-arrow-right"></i>
        </div>
        <h3>{{item.title}}</h3>
        <span>{{item.description}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionDue',
  data(){
    return{
      card:[
        {
          title: 'Technology',
          description: "We are continually focused on developing technology solutions adapted to our client's needs.",
          icon: 'fa-truck-ramp-box'
        },
        {
          title: 'Refer Cargo',
          description: "Regular and frequent monitoring from the receipt of the loaded container to final destination.",
          icon: 'fa-temperature-low'
        },
        {
          title: 'Dry Cargo',
          description: "We work with most types of dry cargo, from valuable cargo to the most dangerous requiring care.",
          icon: 'fa-boxes-stacked',
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
  }

  .bg-blue{
    background-color: rgba($bluelagoon, 0.2);
    padding: 0 10px;
    border-radius: 5px;
    margin-left: 5px;
  }

  .bottone{
    border-radius: 5px;
    padding: 10px 20px;
    text-transform: uppercase;
  }

  .bottone_main{
    border: 2px solid $bluelagoon;

    &:hover{
      color: $bluelagoon;
      border:  2px solid transparent;
      background-color: white;
    }
  }

  .mycard-wrapper{
    margin-top: 30px;
  }
  .mycard{
    height: 250px;
    width: calc(100% / 4);
    background-color: $shark;
    border-radius: 10px;
    padding: 40px 30px;

    i{
      font-size: 22px;
    }

    .arrow{
      color: $bluelagoon;
    }
    
    .icona-mycard{
      color: $fountainblue;
      font-size: 30px;
      background-color: rgba($bluelagoon, 0.2);
      text-align: center;
      aspect-ratio: 1;
      width: 50px;
      border-radius: 50%;
    }
  }
}
</style>
