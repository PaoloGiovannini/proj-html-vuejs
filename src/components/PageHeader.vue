<script>
export default{
    name: 'PageHeader',
    props: {
        navbar: Array
    }
}
</script>

<template>

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
<div id="jumbotron">
    <div class="container d-flex justify-between align-center">
        <div>
            <img src="../assets/logo.PNG" alt="logo nexgen">
        </div>
        <div>
            <a v-for="(element,index) in navbar" href="#">{{ element }}</a>
        </div>
    </div>

</div>


</template>

<style scoped lang="scss">
@use '../styles/partials/variables';
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

}

</style>
