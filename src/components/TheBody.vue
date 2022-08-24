@<template>
  <div>
    <!-- SECTION SERVICES -->
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
    <div class="divisorio">
      <img src="../assets/svgs/svg-0.svg" alt="">
    </div>
    <!-- SECTION THE COMPANY -->
    <section class="the-company">
      <div class="container-company">
        <div class="company-description">
          <h5>ABOUT THE NETWORK</h5>
          <h2><span class="darkgrey-span">The</span> Company</h2>
          <div class="text-button">
            <p>For 12 years we have been providing audit and warranty, financial <br> advice, risk advice, taxes and
              related
              services to select clients.</p>
          </div>
          <!-- CARDS CONTAINER -->
          <div class="company-container-cards">
            <div v-for="card in companyCards" :key="card.id" class="card">
              <div class="title">
                <i class="fa-solid" :class="card.icon"></i>
                <h4>{{ card.title }}</h4>
              </div>
              <p>{{ card.text }}</p>
            </div>
          </div>
          <div class="buttons">
            <FillButton />
            <EmptyButton class="empty-btn-company" />
          </div>
        </div>
        <img src="../assets/images/about-4.jpg" alt="">
      </div>
    </section>

  </div>
</template>

<script>
import FillButton from './FillButton.vue';
import EmptyButton from './EmptyButton.vue';
export default {
  components: { FillButton, EmptyButton },
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
      ],
      companyCards: [{
        id: 1,
        icon: 'fa-medal',
        title: 'Tradition',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        id: 2,
        icon: 'fa-lock',
        title: 'Security',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        id: 3,
        icon: 'fa-pen-to-square',
        title: 'Certificate',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        id: 4,
        icon: 'fa-graduation-cap',
        title: 'Expertise',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },]
    }
  },
}
</script>

<style lang="scss" scoped>
.services {
  padding-bottom: 70px;
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

.divisorio {
  display: flex;
  position: absolute;
  width: 100%;
  z-index: 1;

  img {
    margin: -28px auto;
  }
}

.the-company {
  display: flex;
  background-color: rgb(17, 17, 23);
  position: relative;

  .container-company {
    display: flex;
    justify-content: space-between;
    width: 1000px;
    height: 715px;
    margin: 0px auto;

    .company-description {
      width: 50%;

      h5 {
        margin-top: 100px;
        color: rgb(0, 166, 170);
      }

      h2 {
        font-size: 50px;
        color: white;
      }

      p {
        color: rgb(127, 138, 144);

      }

      .company-container-cards {
        display: flex;
        flex-wrap: wrap;

        .card {
          color: white;
          width: 50%;
          padding-top: 50px;

          .title {
            display: flex;

            i {
              color: rgb(5, 130, 131);
              font-size: 25px;
              padding-right: 5px;
              display: flex;
              align-items: center;
            }

            h4 {
              margin: 0;
              font-size: 25px;
            }
          }
        }
      }

      .buttons {
        margin-top: 30px;

        .empty-btn-company {
          background-color: rgb(17, 17, 23);
          color: white;
          margin-left: 15px;

        }

        .empty-btn-company:hover {
          background-color: rgb(5, 130, 131);
        }
      }
    }

  }

  img {
    width: 50%;
    position: absolute;
    right: 0;
    height: 100%;
    object-fit: cover;
  }
}
</style>