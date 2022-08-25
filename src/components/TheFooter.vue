@<template>
    <section class="form-section">
        <div class="container">
            <div class="form-container">
                <div class="title">
                    <h5>SEND A MESSAGE</h5>
                    <h2>Get in <span class="acquagreen-span">Touch</span></h2>
                    <p>We will responde to your message as soon as possible </p>

                </div>
                <div class="form">
                    <input type="text" placeholder="Name">
                    <input type="text" placeholder="Email">
                    <input type="text" placeholder="Phone">
                    <input type="text" placeholder="More Info">
                    <textarea rows="10" cols="89" placeholder="Message"></textarea>
                </div>
                <SendButton />
            </div>
            <div class="contacts">
                <h3>Example.inc</h3>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                <p>Dolorum alias distinctio deleniti laboriosam itaque, non ipsam.</p>
                <div class="telephone">
                    <i class="fa-solid fa-phone"></i>
                    <span> +1(305)1234-5678</span>
                </div>
                <div class="email">
                    <i class="fa-solid fa-envelope"></i>
                    <span> hello@example.com</span>
                </div>
                <div class="addresse">
                    <i class="fa-solid fa-location-dot"></i>
                    <span> Main Avenue,987</span>
                </div>
                <ViewMapButton />
            </div>
        </div>
    </section>
</template>

<script>
import SendButton from './SendButton.vue';
import ViewMapButton from './ViewMapButton.vue';

export default {
    components: { SendButton, ViewMapButton }
}
</script>

<style lang="scss" scoped>
.form-section {
    padding-top: 100px;


    .container {
        display: flex;
        height: 100%;
    }

    .form-container {
        width: 70%;
        height: 100%;

        .title {
            h5 {
                color: #41C457;
            }

            h2 {
                margin: 0;
            }

            p {
                color: rgb(127, 138, 144)
            }
        }

        .form {
            margin-top: 50px;
            margin-bottom: 50px;

            input {
                width: 45%;
                margin-bottom: 20px;
                margin-right: 20px;
                height: 35px;
                border: 5px solid rgb(236, 236, 236);
                background-color: rgb(236, 236, 236);
                border-radius: 5px;

            }

            textarea {
                width: 95%;
                height: 100px;
                margin-right: 20px;
                border: 5px solid rgb(236, 236, 236);
                background-color: rgb(236, 236, 236);
                border-radius: 5px;
                resize: none;

            }
        }

    }

    .contacts {
        width: 30%;
        height: 100%;

        h3 {
            margin-bottom: 50px;
            font-size: 30px;
        }

        p {
            color: rgb(127, 138, 144);
        }

        i {
            padding: 7px;
            border: 1px solid rgb(218, 236, 237);
            border-radius: 50%;
            color: #41C457;
            background-color: rgb(218, 236, 237);
            margin-bottom: 10px;
            margin-right: 8px;
        }

        span {
            color: #41C457;
        }

        .telephone {
            margin-top: 50px;
        }

        .addresse {
            i {
                padding: 7px;
                padding-left: 9px;
                padding-right: 9px;
                margin-bottom: 50px;
            }
        }



    }
}
</style>