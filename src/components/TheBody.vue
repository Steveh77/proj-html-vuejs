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
    <div class="divisorio">
      <img src="../assets/svgs/svg-0.svg" alt="">
    </div>
    <!-- SECTION PROJECTS -->
    <section class="projects">
      <div class="container">
        <h5>WE NEED MORE FOR EVERYONE</h5>
        <h2>Action &amp; <span class="acquagreen-span">Projects</span></h2>
        <div class="links">
          <ul>
            <li v-for="link in projectLinks" :key="link"><a href="aa">{{ link }}</a></li>
          </ul>
        </div>
        <div class="project-container-card">
          <div v-for="card in projectCard" :key="card" class="project-card">
            <img :src='"../assets/images/project-" + card.photo + ".jpg"' alt="">
            <div>
              <i class="fa-solid fa-arrow-right"></i>
              <h4>{{ card.description }}</h4>
              <p class="hover-text">{{ card.text }}</p>
            </div>
          </div>
        </div>

      </div>
    </section>
    <!-- SECTION RESULTS -->
    <section class="result">
      <div class="container">
        <h5>WHAT ARE WE DOING</h5>
        <h2><span class="darkgrey-span">Results</span> in Number</h2>
        <div class="container-results">
          <ul>
            <li v-for="result in results" :key="result">
              <span>{{ result.number }}</span>
              <h5>{{ result.name }}</h5>
            </li>
          </ul>
        </div>
      </div>
    </section>
    <!-- SECTION COLLABORATION -->
    <section class="collaboration">
      <div class="container">
        <img v-for="collab in collaboration" :key="collab.id" src="../assets/images/logo-1.png" alt="">

      </div>
    </section>
  </div>
</template>

<script>
import FillButton from './FillButton.vue';
import EmptyButton from './EmptyButton.vue';
export default {
  props: {
    results: Array,
    collaboration: Array
  },
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
      },],
      projectLinks: [
        'ALL', 'INSTITUTIONALS', 'SOCIAL', 'EVENTS', 'INNOVATIONS', 'ENVIRONMENT', 'TECHNOLOGY'
      ],
      projectCard: [{
        photo: '1',
        description: 'Academic professional program in social media',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'

      },
      {
        photo: '2',
        description: "President's speech at the annual meetings",
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        photo: '3',
        description: 'international business trip in Shanghai',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        photo: '4',
        description: 'Technology workshop with education theme',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        photo: '5',
        description: 'Donation of clothes and food to the partner NGO',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },
      {
        photo: '6',
        description: 'Confraternization of the procurement team',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit'
      },

      ]
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
      color: #41C457;
    }

    h2 {
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
              filter: invert(59%) sepia(61%) saturate(494%) hue-rotate(78deg) brightness(96%) contrast(88%);
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
    filter: invert(59%) sepia(61%) saturate(494%) hue-rotate(78deg) brightness(96%) contrast(88%);
    opacity: 0.5;
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
        color: #41C457;
      }

      h2 {
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
              color: #41C457;
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
          background-color: #41C457;
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

.projects {
  .container {
    text-align: center;

    h5 {
      padding-top: 70px;
      color: #41C457;
    }

    .links {

      ul {
        display: flex;
        justify-content: space-evenly;
        list-style-type: none;

        li {
          a {
            text-decoration: none;
            color: rgb(96, 109, 117);
            box-shadow: inset 0 0 0 0 rgb(213, 231, 232);
            margin: 0 -.25rem;
            padding: 6px .25rem;
            transition: color .3s ease-in-out, box-shadow .3s ease-in-out;
            border-radius: 3px;
          }

          a:hover {
            border-radius: 5px;
            box-shadow: inset 160px 0 0 0 rgb(218, 236, 237);
            color: rgb(65, 80, 90);
          }
        }
      }
    }

    .project-container-card {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-evenly;
      margin-top: 50px;

      .project-card {
        position: relative;
        width: 30%;
        margin-bottom: 20px;


        img {
          width: 100%;
          border-radius: 10px;
          filter: brightness(0.6);
        }

        i {
          position: absolute;
          top: 35px;
          right: 30px;
          color: white;
          font-size: 31px;
          opacity: 0;
        }

        h4 {
          position: absolute;
          bottom: 30px;
          margin: 19px;
          font-size: 23px;
          color: white;

        }

        p {
          opacity: 0;
          position: absolute;
          bottom: 24px;
          color: white;
          margin: 10px;
        }
      }

      .project-card:hover {
        cursor: pointer;

        img {
          filter: brightness(0.3);
          transition: 0.5s;

        }

        i {
          opacity: 1;
          transition: 1s;
        }

        h4 {
          bottom: 70px;
          transition: 0.5s;
        }

        p {
          opacity: 1;
          transition: 2s;

        }
      }
    }
  }
}

.result {
  height: 500px;
  text-align: center;
  background-image: url(../assets/images/bg-7.jpg);
  background-position: center;

  h5 {
    color: #41C457;
    padding-top: 100px;
  }

  h2 {
    color: white;
  }

  .container-results {
    ul {
      display: flex;
      justify-content: space-between;
      list-style-type: none;

      li {
        color: white;
        font-size: 30px;
        color: #41C457;
        font-weight: bold;
        margin-top: 25px;

        h5 {
          padding-top: 0;
          margin-top: 20px;
          color: white;
        }
      }
    }
  }
}

.collaboration {
  height: 200px;
  background-color: black;

  .container {
    display: flex;
    justify-content: space-between;

    img {
      height: 30px;
    }
  }
}
</style>