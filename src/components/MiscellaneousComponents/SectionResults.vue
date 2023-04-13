<script>
export default{
    name: 'SectionResults',

}
</script>

<template>
<section id="results">
    <div id="number-results">
        <div class="container text-center">
            <span class="results-text">WHAT ARE WE DOING</span>
            <div class="d-flex justify-center align-center">
                <h2>Results</h2>
                <h2>In Numbers</h2>
            </div>
            <div class="cards d-flex">
                <div class="card">
                    <h3>128</h3>
                    <span class="description">Certifications</span>
                </div>
                <div class="card">
                    <h3>230</h3>
                    <span class="description">Employees</span>
                </div>
                <div class="card">
                    <h3>517</h3>
                    <span class="description">Customers</span>
                </div>
                <div class="card">
                    <h3>94</h3>
                    <span class="description">Countries Served</span>
                </div>
            </div>

        </div>
    </div>
    <div id="logos">
        <div class="container">
            <div class="d-flex">
                <div class="logo">
                    <img src="../../assets/logo-4.png" alt="">
                </div>
                <div class="logo">
                    <img src="../../assets/logo-5.png" alt="">
                </div>
                <div class="logo">
                    <img src="../../assets/logo-1.png" alt="">
                </div>
                <div class="logo">
                    <img src="../../assets/logo-2.png" alt="">
                </div>
                <div class="logo">
                    <img src="../../assets/logo-3.png" alt="">
                </div>
                <div class="logo">
                    <img src="../../assets/logo-4.png" alt="">
                </div>
            </div>
        </div>
    </div>
</section>

</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';

#number-results{
    padding: 150px 0px;
    background-image: url('../../assets/bg-7.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 700px;
    background-position: center;
    h2, .description {
        color: white;
    }
    .description{
        font-weight: bold;
    }
    h2:first-child{
        padding: 7px;
        background-color: rgba(3, 132, 132, 0.2);
        margin-right: 7px;
        border-radius: 5px;
    }
    h2{
        margin-top: 18px;
        margin-bottom: 80px;
        font-weight: 900;
        font-size: 30px;
    }
    h3, .results-text{
        color: variables.$text-aqua;
        font-weight: bold;
    }
    h3{
        margin-bottom: 15px;
        font-size: 30px;
    }
    .card{
        width: calc(100% / 4);
    }
}
#logos{
    padding: 80px 0px;
    background-color: variables.$bg-secondary;
    .logo{
        width: calc(100% / 6);
        img{
            width: 70px;
            height: 70px;
            object-fit: contain;
            filter: brightness(4);
        }
        img:hover{
            filter: invert(1);
        }
    }
}


</style>
