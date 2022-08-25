<template>
  <div id="app">
    <MyHeader :empty-buttons="emptyButtons" :fill-buttons="fillButtons" />
    <TheBody :empty-buttons="emptyButtons" :fill-buttons="fillButtons" :results="results"
      :collaboration="collaboration" />
    <TheFooter />
    <TheFooterPart2 />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import TheBody from './components/TheBody.vue';
import TheFooter from './components/TheFooter.vue';
import TheFooterPart2 from './components/TheFooterPart2.vue';
export default {
  name: 'App',
  components: {
    MyHeader,
    TheBody,
    TheFooter,
    TheFooterPart2
  },
  data() {
    return {
      emptyButtons: ['VIEW MAP', 'READ MORE'],
      fillButtons: ['GET IN TOUCH', 'SEND', 'SEE ALL',],
      results: [
        {
          result: 1,
          number: 128,
          name: "Certification"
        },
        {
          result: 1,
          number: 230,
          name: "Employees"
        },
        {
          result: 1,
          number: 517,
          name: "Customers"
        },
        {
          result: 1,
          number: 94,
          name: "Countries Served"
        },

      ],
      collaboration: [
        {
          id: 1,
          logo: 'logo-4.png',
          name: "jquery"
        },
        {
          id: 2,
          logo: 'logo-5.png',
          name: "less"
        },
        {
          id: 3,
          logo: 'logo-1.png',
          name: "wooCommerce"
        },
        {
          id: 4,
          logo: 'logo-2.png',
          name: "wordpress"
        },
        {
          id: 5,
          logo: 'logo-3.png',
          name: "pingdom"
        },
        {
          id: 6,
          logo: 'logo-4.png',
          name: "jquery"
        }
      ]
    }
  },
}
</script>

<style lang="scss">
body {
  margin: 0;
  font-family: system-ui;
}

/* GENERICS */
.acquagreen-span {
  padding: 0 5px 0 5px;
  color: #41C457;
  background-color: rgb(213, 231, 232);
  border-radius: 3px;
}

.darkgrey-span {
  padding: 0 5px 0 5px;
  color: white;
  background-color: rgb(14, 39, 45, 0.7);
  border-radius: 3px;
}

h2 {
  font-size: 50px;
}

/* -------UTILS------- */
.container {
  width: 1000px;
  margin: 0 auto;
}

.p-5px {
  padding: 5px;
}

.p-10px {
  padding: 10px;
}

.m-right-5px {
  margin-right: 5px;
}

/* ----------------------- */
</style>
