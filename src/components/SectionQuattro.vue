<template>
  <div class="main d-flex flex-column gap-3 align-items-center">
    <span>
      what are we doing
    </span>
    <div class="titolo d-flex align-items-center gap-2">
      <h1 class="blue">Results</h1>
      <h1>in Numbers</h1>
    </div>
    <div class="d-flex gap-5 justify-content-around my-4">
      <div v-for="(item,i) in card" :key="i" class="mycard d-flex flex-column align-items-center">
        <span>{{item.number}}</span>
        <h4>{{item.description}}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'SectionQuattro',
    data(){
        return{
            card:[
                {
                number: '128',
                description: 'Certifications'
                },
                {
                number: '230',
                description: 'Employees'
                },
                {
                number: '517',
                description: 'Customers'
                },
                {
                number: '94',
                description: 'Country Served'
                }
            ]
        }
    }
}

</script>

<style scoped lang="scss">
@import '/src/assets/variabili';
@import '/src/assets/mixin';


.main{
    height: 385px;
    padding-top: 50px;
    padding-bottom: 50px;
    background-image: url('/src/assets/img/bg-10.jpg');
    background-position: center;
    background-size: cover;

    span:first-child{
    color: $fountainblue;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: bold;
    }

    .titolo{
    color: white;

    .blue{
      padding: 5px 10px;
      background-color: rgba($bluelagoon,0.2);
      border-radius: 5px;
      }
    }

    .mycard{
    width: 200px;
    height:250px;
    margin-top: 30px;

    span{
      font-size: 16px;

    } 
    span:first-child{
      font-size: 20px;
      color: $fountainblue;

    }
    h4{
      color: white;
      margin: 10px 0;
    }
  }

}
</style>