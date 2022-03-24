<template>
  <div class="credits d-flex justify-content-between align-items-center text-white">
    <span>Enjoy the low price. We are tracking any intention of piracy.</span>
    <div>
      <span>&copy; 2020 NEXGEN is Proudly Powered by</span>
      <span class="blue"> Codings</span>
    </div>
    <i class="icon fa-solid fa-circle-arrow-up"></i>
  </div>
</template>

<script>
export default {
  name: 'FooterDue',
}
</script>

<style lang="scss" scoped>
@import '/src/assets/mixin';
@import '/src/assets/variabili';

.credits{
  height: 60px;
  background-color: black;
  font-size: 14px;
  padding-left: 350px;

  .blue{
    color: $bluelagoon;
  }

  .icon{
    color: $shark;
    font-size: 30px;
    padding-right: 15px;
  }
}

</style>
