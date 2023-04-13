<script>
export default{
    name: 'PageFooter',
    props: {
        voices: Array
    },
    data() {
      return {
        scTimer: 0,
        scY: 0,
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    methods: {
      handleScroll() {
        this.scY = window.scrollY;
      },
      toTop() {
        window.scrollTo({
          top: 0,
          behavior: "smooth"
        });
    }}

}
</script>

<template>
    <!-- sezione superiore del footer -->
    <section id="footer-up">
        <div class="container">
            <!-- inizio elenco carte -->
            <div class="d-flex cards">
                <div class="card">
                    <img src="../assets/logo.PNG" alt="logo nexgen">
                    <p>A Functional HTML Template for Corporate & Business.</p>
                    <div class="info">
                        <span>
                            <i class="fa-solid fa-phone"></i>
                        </span>
                        <span>+1 (305) 1234-5678</span>
                    </div>
                    <div class="info">
                        <span>
                            <i class="fa-solid fa-envelope"></i>
                        </span>
                        <span>hello@example.com</span>
                    </div>
                    <div class="info">
                        <span>
                            <i class="fa-solid fa-globe"></i>
                        </span>
                        <span>Main Avenue, 987</span>
                    </div>
                    <span class="button-border">GET IN TOUCH</span>
                </div>
                <!-- carte generate automaticamente dai valori passati attraverso le props -->
                <div v-for="voice in voices" class="card bg">
                    <h3>{{ voice.titolo }}</h3>
                    <ul>
                        <li v-for="element in voice.voci">
                            <i class="fa-solid fa-chevron-right"></i>
                            <span>{{ element }}</span>
                        </li>
                    </ul>    
                </div>
                <!--fine carte generate automaticamente dai valori passati attraverso le props -->
            </div>
            <!-- fine elenco carte -->
        </div>
    </section>
    <!-- fine sezione superiore del footer -->

    <!-- sezione inferiore del footer -->
    <section id="footer-down">
        <div class="container">
            <div class="d-flex justify-between">
                <span>Enjoy the low price. We are tracking any intention of piracy.</span>
                <div>
                    <span>© {{ new Date().getFullYear() }} NEXGEN is Proudly Powered by </span>
                    <a href="#">Codings</a>
                </div>
            </div>
        </div>
        <!-- freccia scrollToTop -->
        <div>
            <i class="fa-solid fa-chevron-up" v-show="scY > 300" @click="toTop"></i>
        </div>
        <!-- fine freccia scrollToTop -->
    </section>
    <!-- fine sezione inferiore del footer -->
</template>

<style scoped lang="scss">
@use '../styles/partials/variables';
@use '../styles/partials/mixins';
#footer-up{
    background-color: variables.$bg-secondary;
    .container{
        padding: 60px 0px;
        .cards{
            margin-left: -20px;
            margin-right: -20px;
        .bg{
                background-color: #19191f;
                padding: 30px 30px;
                border-radius: 8px;
            }
        .card{
            width: calc(100% / 4 - 40px);
            margin: 0px 20px;
            p{
                margin: 15px 0px;
            }
            .info{
                padding: 7px 0px;
            }
            .button-border{
                @include mixins.button-border;
                display: inline-block;
                margin-top: 30px;
            }
            .button-border:hover{
                color: white;
            }
            p,span,i{
                color: variables.$text-grey;
            }
            h3{
                color: white;
                margin-bottom: 10px;
            }
            img{
                width: 130px;
            }
            ul li{
                list-style: none;
                padding: 7px 0px;
                cursor: pointer;
                i{
                    margin-right: 8px;
                }
            }
        }
        }

    }
}
#footer-down{
    background-color: #0d0d11;
    position: relative;
    .container{
        padding: 30px 0px;
        span{
            color: variables.$text-grey;
        }
        a{
            text-decoration: none;
            color: variables.$text-aqua;
        }
    }
    i{
        color: white;
        position: fixed;
        bottom: 10px;
        right: 20px;
        z-index: 213123;
        background-color:rgba(82, 187, 186, 0.8);
        padding: 20px;
        border-radius: 50%;
        cursor: pointer;
    }
}

</style>
