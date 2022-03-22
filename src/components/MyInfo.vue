<template>
  <div class="info d-flex justify-content-between text-white">
    <div class="info-sx d-flex align-items-center gap-2 ">
      <i class="fa-solid fa-clock"></i>
      <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
    </div>
    <div class="info-dx d-flex align-items-center gap-2 ">
      <i class="fa-solid fa-phone"></i>
      <span>+1 (305) 1234-5678</span>
      <i class="fa-solid fa-envelope"></i>
      <span>hello@example.com</span>
      
    
   </div>
  </div>
</template>

<script>
export default {
  name: 'MyInfo',
}
</script>

<style lang="scss" scoped>
@import '/src/assets/mixin';

.info{
  height: 33px;
  background-color: rgb(26,38,47);
  font-size: 12px;
  @include padding-laterale;

  .info-sx{
  height: 33px;
  }

  .info-dx i{ 
    margin-left: 12px;
  }
}

</style>
