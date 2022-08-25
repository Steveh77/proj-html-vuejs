@<template>
    <section class="footer-menu">
        <div class="container">
            <div class="nextgen">
                <ul>
                    <li>
                        <h1><span>NEXT</span>GEN</h1>
                    </li>
                    <li>
                        <p>A functional HTML template for Corporate &amp; Business</p>
                    </li>
                    <li>
                        <div class="telephone">
                            <i class="fa-solid fa-phone"></i>
                            <span> +1(305)1234-5678</span>
                        </div>

                    </li>
                    <li>
                        <div class="email">
                            <i class="fa-solid fa-envelope"></i>
                            <span> hello@example.com</span>
                        </div>
                    </li>
                    <li>
                        <div class="addresse">
                            <i class="fa-solid fa-location-dot"></i>
                            <span> Main Avenue,987</span>
                        </div>
                    </li>
                    <FillButton class="footerButton" />
                </ul>
            </div>
            <div class="footer-cards">
                <div v-for="card in footerCards" :key="card" class="card">
                    <ul>
                        <li>
                            <h1>{{ card.section }}</h1>
                        </li>
                        <ul>
                            <li v-for="link in card.links" :key="link">
                                <p><i class="fa-solid fa-angle-right"></i> {{ link }}</p>
                            </li>

                        </ul>
                    </ul>

                </div>
            </div>
        </div>

    </section>
</template>

<script>
import FillButton from './FillButton.vue';

export default {
    data() {
        return {
            footerCards: [
                {
                    section: "About",
                    links: ["The Company", "institutional", "Social & Event", "Innovation", "Environment", "Technology"]
                },
                {
                    section: "Services",
                    links: ["The Company", "institutional", "Social & Event", "Innovation", "Environment", "Technology"]
                },
                {
                    section: "Support",
                    links: ["The Company", "institutional", "Social & Event", "Innovation", "Environment", "Technology"]
                }
            ]
        };
    },
    components: { FillButton }
}
</script>

<style lang="scss" scoped>
.footer-menu {
    margin-top: 50px;
    height: 500px;
    background-color: rgb(17, 17, 23);

    .container {
        display: flex;
        padding-top: 50px;

        .nextgen {
            width: 25%;

            ul {
                color: rgb(188, 190, 188);
                list-style-type: none;

                li {
                    h1 {
                        color: white;

                        span {
                            background-color: rgb(14, 39, 45);
                            color: rgb(0, 166, 166);
                            padding: 5px 4px 5px 25px;
                            border-radius: 20px 0px 0 20px;
                        }
                    }

                    i {
                        padding: 5px;
                    }
                }
            }

            .footerButton {
                margin-top: 20px;
                background-color: rgb(17, 17, 23);
            }

            .footerButton:hover {
                background-color: #41C457;
                transition: 0.5s;
            }
        }

        .footer-cards {
            display: flex;
            width: 75%;
            color: white;
            justify-content: space-evenly;

            .card {
                width: 30%;
                background-color: rgb(25, 25, 31);
                border-radius: 10px;

                ul {
                    list-style-type: none;

                    ul {
                        padding-left: 5px;
                        font-size: 15px;

                        li {
                            p {
                                color: rgb(188, 190, 188);
                                margin: 5px;
                            }
                        }
                    }
                }

            }
        }
    }

}
</style>