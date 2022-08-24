<template>
  <div id="app">
    <MyHeader :empty-buttons="emptyButtons" :fill-buttons="fillButtons" />
    <TheBody :empty-buttons="emptyButtons" :fill-buttons="fillButtons" />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import TheBody from './components/TheBody.vue';
export default {
  name: 'App',
  components: {
    MyHeader,
    TheBody
  },
  data() {
    return {
      emptyButtons: ['VIEW MAP', 'READ MORE'],
      fillButtons: ['GET IN TOUCH', 'SEND', 'SEE ALL',]
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
  color: rgb(5, 130, 131);
  background-color: rgb(213, 231, 232);
  border-radius: 3px;
}

.darkgrey-span {
  padding: 0 5px 0 5px;
  color: white;
  background-color: rgb(14, 39, 45);
  border-radius: 3px;
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
