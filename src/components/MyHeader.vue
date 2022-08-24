<template>
    <div>
        <!--SECTION HEADER CONTACTS -->
        <section class="contacts">
            <div class="container">
                <div>
                    <i class="fa-solid fa-clock"></i>
                    <span> Open Hours: Mon-Sat - 9:00 - 18:00 </span>
                </div>
                <div>
                    <i class="fa-solid fa-phone p-5px"></i>
                    <span class="p-10px">+1(305)1234-5678 </span>
                    <i class="fa-solid fa-envelope p-5px"></i>
                    <span class="p-10px">hello@example.com</span>
                    <i class="fa-brands fa-facebook-f p-10px"></i>
                    <i class="fa-brands fa-twitter p-10px"></i>
                    <i class="fa-brands fa-linkedin-in p-10px"></i>
                </div>

            </div>
        </section>
        <!-- SECTION HERO -->
        <section class="hero">
            <div class="bg-hero">
                <div class="container">
                    <nav>
                        <div>
                            <img class="nav-logo" src="../assets/logo.png" alt="">
                        </div>
                        <div>
                            <ul>
                                <li v-for="link in links" :key="link"><a href="#">{{ link }}</a></li>
                                <li>
                                    <FillButton />
                                </li>
                            </ul>
                        </div>
                    </nav>
                    <div class="central-text">
                        <h1>Ready <span class="acquagreen-span">Team</span></h1>
                        <p>No matters what your company needs,we will be <br> ready to assist you in the best possible
                            way
                        </p>
                        <FillButton class="m-10px" />
                        <EmptyButton class="m-10px" />
                    </div>
                </div>
            </div>
        </section>
    </div>


</template>

<script>
import FillButton from './FillButton.vue';
import EmptyButton from './EmptyButton.vue';
export default {
    props: {
        emptyButtons: Array,
        fillButtons: Array
    },
    data() {
        return {
            links: ["HOME", "SERVICES", "ABOUT", "PROJECT", "RESULT"]
        };
    },
    components: { FillButton, EmptyButton },
}
</script>

<style lang="scss" scoped>
.m-10px {
    margin: 10px
}

/* SECTION HEADER CONTACTS */
.contacts {
    height: 50px;
    background-color: #21333E;
    display: flex;
    align-items: center;
    color: rgb(192, 195, 208);

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}

/* SECTION HERO */
.hero {
    height: 700px;

    .bg-hero {
        height: 100%;
        background-image: url(../assets/images/bg-parallax.png);
        background-position: center;
        padding-bottom: 60px;

        nav {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;

            .nav-logo {
                height: 50px;
            }

            ul {
                display: flex;
                list-style-type: none;

                li {
                    padding-left: 35px;

                    a {
                        text-decoration: none;
                        color: rgb(65, 80, 90);
                        box-shadow: inset 0 0 0 0 rgb(213, 231, 232);
                        margin: 0 -.25rem;
                        padding: 6px .25rem;
                        transition: color .3s ease-in-out, box-shadow .3s ease-in-out;
                        border-radius: 3px;
                    }

                    a:hover {
                        box-shadow: inset 100px 0 0 0 rgb(213, 231, 232);
                        color: rgb(65, 80, 90);
                    }
                }

            }

        }

        .central-text {
            width: 440px;
            text-align: center;
            margin: 0 auto;
            padding-top: 140px;

            h1 {
                font-size: 70px;
                color: rgb(33, 51, 62);
                font-family: 'Ruda', sans-serif;
                margin-bottom: 30px;
            }

            p {
                color: rgb(127, 138, 144);
                font-size: 20px;
                font-family: system-ui;
            }
        }


    }

}
</style>