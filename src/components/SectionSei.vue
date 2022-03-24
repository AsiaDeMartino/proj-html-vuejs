<template>
  <div class="main row">
    <div class="col-9 d-flex flex-column gap-3">
      <span class="blue fw-bold text-uppercase">send a message</span>
      <div class="titolo fw-bold d-flex">
        <h1>Get in</h1>
        <h1 class="blue bg-blue">Touch</h1>
      </div>
        <span>We will respond to your message as soon as possible.</span>
        <div class="d-flex flex-wrap gap-3">
          <input placeholder="Name" type="text">
          <input placeholder="Email" type="text">
          <input placeholder="Phone" type="text">
          <select name="" id="">
            <option value="">More Info</option>
          </select>
          <input placeholder="Message" class="message" type="text">
        </div>
        <button>send</button>
    </div>
    <div class="col-3 d-flex flex-column gap-3">
      <h5>Example Inc.</h5>
      <span>Lorem ipsum dolor sit amet, consectetura dipiscing elit.</span>
      <span>Praesent diam lacus, dapibus sed imperdiet consectetur.</span>
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
      <button>view map</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionSei',
}
</script>

<style lang="scss" scoped>
@import '/src/assets/mixin';
@import '/src/assets/variabili';

.main{
  @include padding-laterale;
  color: $midgray;
  padding-top: 50px;
  padding-bottom: 50px;
  font-size: 12px;

  .col-9{
    .blue{
      color: $bluelagoon;
    }

    .titolo{
      margin-top: 20px;
      margin-bottom: 15px;
      color: black;
    }

    .bg-blue{
      background-color: rgba($bluelagoon, 0.2);
      padding: 0 10px;
      border-radius: 5px;
      margin-left: 5px;
    }

    input,select{
      width: 49%;
      border: none;
      background-color: $graynurse;
      height: 30px;
      border-radius: 5px;
      color: $midgray;
      padding: 0 5px;
    }

    .message{
      width: 100%;
      height: 100px;

      &::placeholder{
        position: absolute;
        padding-top: 5px;
      }
    }

    button{
      text-transform: uppercase;
      color: white;
      background-color: $bluelagoon;
      border: none;
      width: 65px;
      height: 30px;
      border-radius: 5px;
    }
  }

  .col-3{
    h5{
      color: black;
      font-weight: bold;
    }

    div{
      color: $bluelagoon;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    i{  
      background-color: rgba($bluelagoon, 0.2);
      height: 25px;
      width: 25px;
      border-radius: 50%;
      text-align: center;
      line-height: 25px;
    }

    button{
      height: 30px;
      width: 90px;
      background-color: transparent;
      border: 1px solid $bluelagoon;
      border-radius: 5px;
      text-transform: uppercase;
      color: $bluelagoon;
    }
  }

}


</style>
