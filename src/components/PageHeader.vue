<script>
import ButtonTouch from './MiscellaneousComponents/ButtonTouch.vue'
export default{
    name: 'PageHeader',
    props: {
        navbar: Array
    },
    components:{
        ButtonTouch,
    }
}
</script>

<template>
<!-- sezione orari, numeri di telefono e social -->
<div id="info">
    <div class="container d-flex justify-between">
        <div>
            <i class="fa-solid fa-clock"></i>
            <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
        </div>
        <div>
            <i class="fa-solid fa-phone"></i>
            <span>+1 (305) 1234-5678</span>
            <i class="fa-solid fa-envelope"></i>
            <span>hello@example.com</span>
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-linkedin-in"></i>
        </div>
        
    </div>
</div>
<!-- fine sezione orari, numeri di telefono e social -->

<!-- inizio jumbotron -->
<div id="jumbotron">
    <div class="container d-flex justify-between align-center">
        <div>
            <img src="../assets/logo.PNG" alt="logo nexgen">
        </div>
        <!-- voci del menu generate automaticamente con relativo href -->
        <div class="d-flex align-center">
            <a v-for="(element,index) in navbar" :href="'#' + element">{{ element.toUpperCase() }}</a>
            <ButtonTouch/>
        </div>
        <!-- fine voci del menu generate automaticamente con relativo href -->
    </div>
    <div id="jumbo-text">
        <div class="d-flex align-center justify-center">
            <h1>Ready</h1>
            <h1>Team</h1>
        </div>
        <p class="text-center">No matter what your company needs, we will be ready to assist you in the best possible way.</p>
        <div class="d-flex justify-center">
            <ButtonTouch/>
            <div class="button-border">
                <span>READ MORE</span>
            </div>
        </div>
    </div>
</div>
<!-- fine jumbotron -->


</template>

<style scoped lang="scss">
@use '../styles/partials/variables';
@use '../styles/partials/mixins';
#info{
    background-color: variables.$bg-info;
    color: variables.$text-grey;
    padding: 10px 0px;
    span{
        margin-right: 20px ;
    }
    i{
        padding: 0px 10px;
    }
    .fa-facebook-f:hover, .fa-twitter:hover, .fa-linkedin-in:hover{
        color: white ;
        cursor: pointer;
    }


}
#jumbotron{
    height: 800px;
    background-image: url('../assets/bg-parallax.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    padding: 15px 0px;
    position: relative;
    img{
        width: 130px;
    }
    a{
        padding: 0px 10px;
        text-decoration: none;
        color: black;
    }
    #jumbo-text{
        width: 400px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        p{
            margin-top: 20px;
            margin-bottom: 35px;
            color: variables.$text-grey;
        }
        h1{
            font-size: 50px;
            font-weight: 900;
        }
        h1:first-child{
            color: variables.$bg-info ;
            margin-right: 10px;
        }
        h1:last-child{
            color: variables.$button-color;
            @include mixins.text-bg
        }
        .button-border{
            @include mixins.button-border;
            margin-left: 20px;
            color: variables.$button-color;
        }
        .button-border:hover{
            color: white;
        }
    }
}

</style>
