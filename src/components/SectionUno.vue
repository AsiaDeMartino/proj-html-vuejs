<template>
  <div class="main row">
    <div class="col-8 d-flex flex-column gap-2">
      <span class="sottotitolo text-uppercase">who we are</span>
      <div class="titolo">
        <span class="blue"><i class="fa-regular fa-gem"></i> Excellence</span>
        <span class="text-dark"> in Transport</span>
      </div>
      <div class="content d-flex flex-column gap-4">
        <span >
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum velit tortor, interdum sed cursus eu, sagittis ut nunc. Sed vitae tellus et arcu aliquet faucibus fermentum non lacus. 
        </span>
        <span>
          Praesent fringilla quis massa et placerat. Mauris eu dui eget urna pellentesque gravida vitae quis nibh. Ut at augue tortor. Pellentesque quis suscipit magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quam tortor, ultrices accumsan mauris eget, pulvinar tincidunt erat. Sed nisi nisi, rutrum sit amet elit.
        </span>
        <div class="bordo">
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quam tortor, ultrices accumsan mauris eget, pulvinar tincidunt erat. Sed nisi nisi, rutrum sit amet elit.</span>
        </div>
        <span>Sed mauris nulla, tempor eu est vel, dapibus hendrerit mauris curabitur dictum pharetra.</span>
        <ul>
          <li>Lorem ipsum dolor sit amet</li>
          <li>Consectetur adipiscing elit</li>
          <li>Integer molestie lorem at massa</li>
          <li>Facilisis in pretium nisl aliquet</li>
          <li>Dapibus hendrerit mauris curabitur</li>
        </ul>
      </div>
    </div>
    <div class="col-4">
      <span class="text-dark fw-bold">Vehicle Types</span>
      <div>
        <div v-for="(item,i) in card" :key="i" class="mycard d-flex gap-3" style="width: 18rem;">
          <img src="../assets/img/truck-1.png">
          <div>
            <h5 class="fw-bold text-dark">{{item.title}}</h5>
            <p class="card-text">Max Weight {{item.weight}} Kg</p>
          </div>
        </div>
      </div>
      <div class="certificate fw-bold text-dark">
        <span>Certifications</span>
        <div class="d-flex gap-3">
          <img src="../assets/img/certificate.png" alt="">
          <img src="../assets/img/certificate.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionUno',
  data(){
    return{
      card:[
        {
          title: 'Light',
          weight: '1200'
        },
        {
          title: 'Medium',
          weight: '6000'
        },
        {
          title: 'Heavy',
          weight: '24000'
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
  @include padding-laterale;
  color: $midgray;
  height: 580px;
  padding-top: 100px;

  .sottotitolo{
    font-weight: bold;
    font-size: 12px;
    color: $bluelagoon;
  }
  
  .titolo{
    font-size: 40px;
    font-weight: bold;
  }

  .blue{
    color: $bluelagoon;
    background-color: rgba($bluelagoon, 0.2);
    border-radius: 5px;
    padding: 0 8px;
  }
  
  .content{
    font-size: 12px;

    .bordo{
    padding: 10px 20px;
    border-left: 4px solid rgba($bluelagoon, 0.2);
    font-style: italic;
    }
  }

  .mycard{
    border-bottom: 1px solid $midgray;
    padding: 15px 0;

    &:last-child{
      border: none;
    }

    img{
      height: 60px;
      padding: 10px;
      background-color: rgba($bluelagoon, 0.2);
      border-radius: 5px;
    }

    .card-text{
      font-size: 12px;
    }
  }

  .certificate{
    margin-top: 20px;   

    img{
      height: 80px;
      margin-top: 20px;
    }
  } 
}


</style>
