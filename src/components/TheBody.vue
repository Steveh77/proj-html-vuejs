@<template>
  <div>
    <section class="services">
      <div class="container">
        <h5>OUR BUSINESS AREA </h5>
        <h2>Excellence in <span class="acquagreen-span">Services</span></h2>
        <div class="text-button">
          <p>We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of <br>
            experienced and renowned professionals. These are some options that you can hire</p>
          <FillButton />
        </div>
        <!-- SERVICES CARD -->
        <div class="services-cards">
          <div v-for="card in servicesCards" :key="card.id" class="services-card">
            <div class="container-card">
              <div class="icons">
                <img :src='"../assets/svgs/svg-" + card.id + ".svg"' alt="">
                <i class="fa-solid fa-arrow-right"></i>
              </div>
              <h4>{{ card.title }}</h4>
              <p>{{ card.text }}</p>
            </div>
          </div>

        </div>
      </div>
    </section>
  </div>
</template>

<script>
import FillButton from './FillButton.vue';
export default {
  components: { FillButton },
  data() {
    return {
      servicesCards: [
        {
          id: 1,
          title: 'Audit e Assurance',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
        },
        {
          id: 2,
          title: 'financial Advisory',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
        },
        {
          id: 3,
          title: 'Analitytics and M&a',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
        },
        {
          id: 4,
          title: 'Middle Marketing',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
        },
        {
          id: 5,
          title: 'Legal Consulting',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
        },
        {
          id: 6,
          title: 'Regulatory Risk',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
        },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.services {

  background-color: rgb(238, 244, 237);

  .container {
    h5 {
      padding-top: 150px;
      color: rgb(0, 166, 170);
    }

    h2 {
      font-size: 50px;
      color: rgb(33, 51, 62);
    }

    .text-button {
      display: flex;
      justify-content: space-between;
      align-items: center;

      p {
        color: rgb(127, 138, 144);
      }

    }

    .services-cards {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      margin-top: 40px;

      .services-card {
        display: flex;
        flex-direction: column;
        width: 32%;
        height: 260px;
        background-color: white;
        border-radius: 20px;
        margin-bottom: 18px;

        .container-card {
          width: 80%;
          height: 80%;
          margin: auto;

          .icons {
            display: flex;
            justify-content: space-between;

            img {
              height: 50px;
            }

            i {
              font-size: 30px;
              color: rgb(130, 193, 193);
            }
          }

          h4 {
            font-size: 25px;
          }

          p {
            color: rgb(127, 138, 144);
          }
        }


      }
    }
  }
}
</style>