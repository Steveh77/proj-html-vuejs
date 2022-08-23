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

        </section>
    </div>


</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container {
    width: 900px;
    margin: 0 auto;
}

/* -------UTILS------- */
.p-5px {
    padding: 5px;
}

.p-10px {
    padding: 10px;
}

/* ----------------------- */

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
.hero {}
</style>