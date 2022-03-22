<template>
  <div class="main d-flex flex-column gap-3 align-items-center">
    <span>
      how it works in practice
    </span>
    <div class="titolo d-flex align-items-center gap-2">
      <h1 class="blue">Logistical</h1>
      <h1>Procedure</h1>
    </div>
    <span class="width">
      We work with innovative methodologies to ensure that the entire delivery process is done from start to finish as planned.
    </span>
    <div class="mycard-wrapper trattino d-flex gap-5 justify-content-around my-4">
      <div v-for="(item,i) in card" :key="i" class="mycard d-flex flex-column align-items-center">
        <span>{{item.number}}</span>
        <h4>{{item.title}}</h4>
        <span>{{item.description}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionTre',
  data(){
    return{
      card:[
        {
          number: '01',
          title: 'Collection of information',
          description: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          number: '02',
          title: 'Service Invoice Sending',
          description: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          number: '03',
          title: 'Withdrawal of Cargo',
          description: 'Lorem ipsum dolor sit amet consectetur.',
        },
        {
          number: '04',
          title: 'Transport Customer Order',
          description: 'Lorem ipsum dolor sit amet consectetur.',
        },
        {
          number: '05',
          title: 'Successful Delivery',
          description: 'Lorem ipsum dolor sit amet consectetur.',
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '/src/assets/variabili';

.main{
  background-color: $graynurse;
  padding-top: 50px;
  padding-bottom: 50px;
  font-size: 12px;
  text-align: center;

  span:first-child{
    color: $bluelagoon;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: bold;
  }

  .titolo{
    color: $shark;

    .blue{
      padding: 5px 10px;
      color: $bluelagoon;
      background-color: rgba($bluelagoon,0.2);
      border-radius: 5px;
    }
  }

  .width{
    max-width: 40%;
    font-size: 16px;
    color: $midgray;
  }

  .trattino::before{
    content: "";
    display: block;
    clear: both;
    border-bottom: 7px solid rgba($bluelagoon,0.2);
    width: 100%;
    position: absolute;
    transform: translateY(300%);
}

  .mycard{
    width: 200px;
    height:250px;
    z-index: 999;

    span{
      font-size: 16px;
      color: $midgray;
    } 
    span:first-child{
      font-size: 20px;
      background-color: rgb(201,222,223);
      padding: 10px;
      border-radius: 50%;
      color: $bluelagoon;
      width: 50px;
      display: flex;
      justify-content: center;
    }
    h4{
      margin: 20px 0;
    }
  }
}
</style>
