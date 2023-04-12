<script>
export default{
    name: 'SectionForm',

}
</script>

<template>
    <section id="info-company">
        <div class="container">
            <div class="d-flex">
                <div id="form">
                    <span id="send">SEND A MESSAGE</span>
                    <div class="d-flex align-center">
                        <h2>Get in</h2>
                        <h2>Touch</h2>
                    </div>
                    <span>We will respond to your message as soon as possible.</span>
                    <div class="d-flex wrap cards-input">
                        <div class="input-form pos-rel">
                            <input type="text" placeholder="Name">
                            <img src="../../assets/image (1).png" alt="#" class="pos-abs">
                        </div>
                        <div class="input-form">
                            <input type="text" placeholder="Email">
                        </div>
                        <div class="input-form">
                            <input type="text" placeholder="Phone">
                        </div>
                        <div class="input-form pos-rel">
                            <input type="text" placeholder="More Info">
                            <img src="../../assets/image (2).png" alt="#" class="pos-abs">
                        </div>
                    </div>
                    <input type="text" placeholder="Message" id="big-input">
                    <span class="button">SEND</span>
                </div>
                <div id="contact">

                    <h3>Example Inc.</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, ullam?</p>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea, sed.</p>
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
                    <span class="button-border">VIEW MAP</span>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';
.container{
    padding: 80px 0px;
    #form{
    width: 60%;
    #send{
        color: variables.$text-aqua;
        font-weight: bold;
    }
    h2{
        font-size: 30px;
        font-weight: 900;
        margin: 20px 0px;
    }
    h2:last-child{
        @include mixins.text-bg;
        color: variables.$button-color;
    }
    input{
        width: 100%;
        padding: 8px 0px;
        background-color: #ececec;
        border: none;
        border-radius: 3px;
    }
    #big-input{
        line-height: 150px;
        margin-top: 5px;
    }
    .button{
        @include mixins.button;
        display: inline-block;
        margin-top: 30px;
    }
    
    .cards-input{
        margin-left: -5px;
        margin-right: -5px;
        margin-top: 20px;
        .pos-rel{
            position: relative;
        }

        .input-form{
            width: calc(100% / 2 - 10px);
            margin: 5px;
            .pos-abs{
                position: absolute;
                top: 50%;
                right: 0;
                transform: translate(-50%, -50%);
            }
        }
    }

}
#contact{
    width: 40%;
    margin: 0px 30px;
    p{
        padding: 10px 0px;
    }
    .info{
        color: variables.$button-color;
        padding: 8px 0px;
        i{
            background-color: #d5e7e8;
            padding: 10px;
            border-radius: 50%;
            margin-right: 7px;
        }

    }
    .button-border{
        @include mixins.button-border;
        display: inline-block;
        color: variables.$button-color;
        margin-top: 20px;
    }
}
}


</style>
