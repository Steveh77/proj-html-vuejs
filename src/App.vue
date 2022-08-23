<template>
  <div id="app">
    <MyHeader />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
export default {
  name: 'App',
  components: {
    MyHeader
  }
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
