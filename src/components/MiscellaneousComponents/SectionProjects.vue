<script>
export default{
    name: 'SectionProjects',
    props: {
        actions: Array
    }

}
</script>

<template>
<section id="projects">
    <div class="container text-center">
        <span id="text-title">WE DO MORE FOR EVERYONE</span>
        <div class="d-flex justify-center align-center">
            <h2>Actions &</h2>
            <h2 >Projects</h2>
        </div>
        <a class="link" v-for="element in actions" href="#">{{ element }}</a>
        <div class="cards d-flex wrap">
            <div class="card">
                <img src="../../assets/project-1.jpg" alt="immagine progetto">
                <div class="text-on-image">
                    <span>Academic professional program in social media</span>
                </div>
            </div>
            <div class="card">
                <img src="../../assets/project-2.jpg" alt="immagine progetto">
                <div class="text-on-image">
                    <span>President's speech at the annual meeting</span>
                </div>
            </div>
            <div class="card">
                <img src="../../assets/project-3.jpg" alt="immagine progetto">
                <div class="text-on-image">
                    <span>International business trip in Shangai</span>
                </div>
            </div>
            <div class="card">
                <img src="../../assets/project-4.jpg" alt="immagine progetto">
                <div class="text-on-image">
                    <span>Technology workshop with education theme</span>
                </div>
            </div>
            <div class="card">
                <img src="../../assets/project-5.jpg" alt="immagine progetto">
                <div class="text-on-image">
                    <span>Donation of clothes and food to the partner NGO</span>
                </div>
            </div>
            <div class="card">
                <img src="../../assets/project-6.jpg" alt="immagine progetto">
                <div class="text-on-image">
                    <span>Confraternization of the procurement team</span>
                </div>
            </div>
        </div>

    </div>
</section>

</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';

.container{
    padding: 100px 0px;
    #text-title{
        color: variables.$text-aqua;
        font-weight: bold;
    }
    h2{
        font-size: 30px;
        font-weight: 900;
        margin: 20px 0px 40px 7px;
    }
    h2:last-child{
        @include mixins.text-bg;
        color: variables.$button-color
    }
    a{
        text-decoration: none;
        color: black;
        padding: 0px 15px;
        display: inline-block;
        margin-bottom: 20px;
        
    }
    a:first-of-type{
        @include mixins.text-bg;
    }
    .cards{
        margin-left: -20px;
        margin-right: -20px;
        .card{
        width: calc(100% / 3 - 40px);
        margin: 20px;
        position: relative;
        
        img{
            width: 100%;
            filter: brightness(0.6);
        }

        .text-on-image{
            width: 220px;
            position: absolute;
            bottom: 20px;
            color: white;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 18px;
            font-weight: bold;
        }
    }
}

}

</style>
