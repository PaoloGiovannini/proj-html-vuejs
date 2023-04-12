<script>
import ButtonTouch from './ButtonTouch.vue'
export default{
    name: 'SectionCompany',
    components:{
        ButtonTouch
    }
}
</script>

<template>
<section id="about">
    <div>
        <img src="../../assets/bullets.png" alt="trama a pois" class="bullets">
    </div>
    <div class="d-flex justify-between">
        <div class="info-company">
            <div class="about-network">
                <span id="text-about">ABOUT THE NETWORK</span>
                <div class="d-flex align-center">
                    <h2>The</h2>
                    <h2>Company</h2>
                </div>
                <p>For 12 years we have been providing audit and warranty, financial advice risk advice, taxes and related services to select clients.</p>
                <div class="d-flex wrap">
                    <div class="card">
                        <div>
                            <i class="fa-solid fa-medal"></i>
                            <span>Tradition</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisci ng el it. </p>
                        </div>
                    </div>
                    <div class="card">
                        <div>
                            <i class="fa-solid fa-lock"></i>
                            <span>Security</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisci ng el it. </p>
                        </div>
                    </div>
                    <div class="card">
                        <div>
                            <i class="fa-regular fa-clipboard"></i>
                            <span>Certificate</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisci ng el it. </p>
                        </div>
                    </div>
                    <div class="card">
                        <div>
                            <i class="fa-solid fa-graduation-cap"></i>
                            <span>Expertise</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisci ng el it. </p>
                        </div>
                    </div>
                </div>
            <div class="d-flex">
                <ButtonTouch/>
                <div class="button-border">
                    <span>READ MORE</span>
                </div>
            </div>
            </div>
        </div>
        <div class="info-company">
            <img src="../../assets/about-4.jpg" alt="">
        </div>
    </div>

    <div>
        <img src="../../assets/bullets.png" alt="trama a pois" class="bullets">
    </div>
</section>
</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';
#about{
    background-color: variables.$bg-secondary;
    color: white;
    position: relative;
    .bullets{
        width: 60px;
        position: absolute;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    #text-about{
        color: variables.$text-aqua;
        font-weight: bold;
    }
    .info-company:first-child{
        padding-top: 150px;
    }
    .info-company{
        width: 50%;
        .about-network{
            max-width: 50%;
            margin: auto;
            margin-right: 50px;
            h2{
                margin: 20px 0px;
                font-size: 30px;
                font-weight: 900;
            }
            h2:first-child{
                padding: 7px;
                background-color: rgba(3, 132, 132, 0.2);
                margin-right: 7px;
                border-radius: 5px;
            }
        }
        img{
            width: 100%;
            height: 100%;
            display: block;
        }
        p{
            margin-top: 15px;
            margin-bottom: 35px;
            color: variables.$text-grey;
        }
        .card{
            width: calc(100% / 2 - 20px);
            margin: 30px 20px 0px 0px;
            i{
                color: variables.$button-color;
                margin-right: 7px;
            }
            span{
                font-size: 20px;
                font-weight: bold;
            }

        }
        .button-border{
            @include mixins.button-border;
            margin-left: 25px ;
        }
    }

}

</style>
