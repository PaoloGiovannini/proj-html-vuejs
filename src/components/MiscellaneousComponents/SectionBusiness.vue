<script>
export default{
    name: 'SectionBusiness',

}
</script>

<template>
<!-- inizio sezione services -->
<section id="services">
    <div class="container">
        <span id="subtitle">OUR BUSINESS AREAS</span>
        <div class="d-flex align-center">
            <h2>Excellence in</h2>
            <h2>Services</h2>
        </div>
        <div class="d-flex justify-between align-center">
            <span id="info">We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.</span>
            <div class="button">
                <span>SEE ALL</span>
            </div>
        </div>
        <div class="d-flex" id="container-card">
            <div class="card">
                <div class="d-flex justify-between">
                    <i class="fa-solid fa-network-wired"></i>
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
                <h4>Audit & Assurance</h4>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos ratione.</p>

            </div>
            <div class="card">
                <div class="d-flex justify-between">
                    <i class="fa-solid fa-briefcase"></i>
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
                <h4>Financial Advisory</h4>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos ratione.</p>

            </div>
            <div class="card">
                <div class="d-flex justify-between">
                    <i class="fa-solid fa-chart-line"></i>
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
                <h4>Analytics and M&A</h4>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos ratione.</p>

            </div>
            <div class="card">
                <div class="d-flex justify-between">
                    <i class="fa-solid fa-plane-up"></i>
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
                <h4>Middle Marketing</h4>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos ratione.</p>

            </div>
            <div class="card">
                <div class="d-flex justify-between">
                    <i class="fa-solid fa-globe"></i>
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
                <h4>Legal Consulting</h4>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos ratione.</p>

            </div>
            <div class="card">
                <div class="d-flex justify-between">
                    <i class="fa-regular fa-folder-open"></i>
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
                <h4>Regulatory Risk</h4>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos ratione.</p>

            </div>
        </div>
    </div>
</section>
<!-- fine sezione services -->
</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';

 #services{
    background-color: variables.$bg-primary;
    padding: 90px 0px;
    #subtitle{
        color: variables.$text-aqua;
        font-weight: bold;
    }
    h2{
        font-size: 30px;
        font-weight: 900;
        padding: 20px 0px;
    }
    h2:first-child{
        color: variables.$bg-info ;
        margin-right: 10px;
    }
    h2:last-child{
        color: variables.$button-color;
        @include mixins.text-bg
    }
    .button:hover{
    background-color: #00a6a6;
    }
    .button{
        @include mixins.button
    }
    #info{
        flex-basis: 900px;
    }
    #container-card{
        flex-wrap: wrap;
        padding-top: 30px;
        margin-left: -20px;
        margin-right: -20px;
        .card:hover .fa-arrow-right{
               background-color: #d5e7e8;
               padding: 10px;
               border-radius: 50%;
               cursor: pointer;
            }
        .card{
            width: calc(100% / 3 - 40px);
            background-color: white;
            margin: 10px 20px;
            padding: 40px;
            border-radius: 10px;
            i:first-child{
                color: variables.$button-color;
                font-size: 30px;
            }
            i:last-child{
                color: variables.$button-color;
            }
            h4{
                margin: 20px 0px;
            }
        }
    }
 }

</style>
