<template>
    <div>
        <MyInfo />
        <div class="header text-white">
            <div class="background">
                <div class="menu d-flex justify-content-between align-items-center">
                    <div class="menu-sx">
                        <div class="logo fw-bold text-uppercase d-flex align-items-center">
                            <div class="bg-blue d-flex justify-content-end align-items-center">
                                <h5>nex</h5>
                            </div>
                             <h5>gen</h5>
                        </div>
                    </div>
                    <div class="menu-dx d-flex align-items-center gap-4">
                        <ul>
                            <li v-for="(items,i) in menu" :key="i"><a href="#">{{items}}</a></li>
                            <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
                            <li>
                                <div class="bottone bottone_menu">
                                    get in touch
                                </div>
                            </li>  
                        </ul>
                    </div>
                </div>
                <div class="contenuto row">
                    <div class="main-content col-6 d-flex flex-column gap-3">
                        <span class="text-uppercase">logistics services</span>
                        <h1 class="text-uppercase">cargo transport</h1>
                        <span class="gray">Fractional or exclusive road cargo transportation to all regions, with small, medium and large vehicles.</span>
                        <div class="d-flex align-items-center gap-4">
                            <div class="bottone bottone_menu">
                                get in touch
                            </div>
                            <div class="bottone bottone_main">
                                read more
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>    
</template>

<script>
import MyInfo from './MyInfo';

export default {
    name: 'MyHeader',
    components: {
    MyInfo
    },
    data(){
        return{
            menu:['home','about','services','process','testimonials'],
        }
    }
}
</script>

<style scoped lang="scss">
@import '/src/assets/mixin';
@import '/src/assets/variabili';

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.header{
    height: 562px;
    background: url('/src/assets/img/bg-9.jpg');
    background-position: center;
    background-size: cover;
    

    .background{
        height: 100%;
        background-color: rgba(black, 0.6);
        @include padding-laterale;
        padding-top: 15px;
    }

    .menu{
        font-size: 15px;
        text-transform: uppercase;
        margin-bottom: 100px;
    }

    .logo{
        letter-spacing: 4px;
    }

    .bg-blue{
    background-color: rgba($bluelagoon, 0.3);
    height: 40px;
    width: 80px;
    border-top-left-radius: 40px;
    border-bottom-left-radius: 40px;
    color: $fountainblue;
  }


    ul{
        list-style: none;
        display: contents;
    }

    a {
    text-decoration: none;
    color: currentColor;

        &:hover{
            color: $bluelagoon;
        }
    }

    .bottone{
        border-radius: 5px;
        padding: 10px 20px;
        text-transform: uppercase;
    }

    .bottone_menu{
        background-color: $bluelagoon;

        &:hover{
            color: $bluelagoon;
            background-color: white;
        }
    }

    .bottone_main{
        border: 2px solid $bluelagoon;

        &:hover{
            color: $bluelagoon;
            border:  2px solid transparent;
            background-color: white;
        }
    }

    .main-content span:first-child{
        color: $bluelagoon;
        font-weight: bold;
    }

    h1{
        font-weight: bold;
        font-size: 4rem;
    }

    .gray{
        color: $silversand;
    }
}
</style>