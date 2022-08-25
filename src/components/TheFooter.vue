@<template>
    <section class="form-section">
        <div class="container">
            <div class="form">
                <div class="title">
                    <h5>SEND A MESSAGE</h5>
                    <h2>Get in <span class="acquagreen-span">Touch</span></h2>
                    <p>We will responde to your message as soon as possible </p>
                </div>
            </div>
            <div class="contacts">
                <h3>Example.inc</h3>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                <p>Dolorum alias distinctio deleniti laboriosam itaque, non ipsam.</p>
                <div class="telephone">prova</div>
                <div class="email">prova</div>
                <div class="addresse">prova</div>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.form-section {
    padding-top: 100px;
    height: 500px;

    .container {
        display: flex;
        height: 100%;
    }

    .form {
        width: 70%;
        height: 100%;

        .title {
            h5 {
                color: #41C457;
            }

            p {
                color: rgb(127, 138, 144)
            }
        }

    }

    .contacts {
        width: 30%;
        height: 100%;

        p {
            color: rgb(127, 138, 144);
        }

    }
}
</style>