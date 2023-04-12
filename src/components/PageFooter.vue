<script>
export default{
    name: 'PageFooter',
    props: {
        voices: Array
    }

}
</script>

<template>
    <section id="footer-up">
        <div class="container">
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
                <div v-for="voice in voices" class="card bg">
                    <h3>{{ voice.titolo }}</h3>
                    <ul>
                        <li v-for="element in voice.voci">
                            <i class="fa-solid fa-chevron-right"></i>
                            <span>{{ element }}</span>
                        </li>
                    </ul>    
                </div>
            </div>
        </div>
    </section>
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
    </section>
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
            }
        }
        }

    }
}
#footer-down{
    background-color: #0d0d11;
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
}

</style>
