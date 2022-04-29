<template>
  <div class="main-container">
    <h1>VueJS: Props</h1>
    <MyButton name="OK" bgColor="#67f080"></MyButton>
    <MyButton name="KO" bgColor="#f25041"></MyButton>

    <!-- <h1>Different props</h1>
    <ShowSquare
      v-bind:bgColors="['green', 'red', 'brown', 'blue', 'black']"
      v-bind:isHidden="false">
    </ShowSquare> -->
  </div>
</template>

<script>
// import ShowSquare from './components/ShowSquare.vue';
import MyButton from './components/MyButton.vue';

export default {
  name: 'App',
  components: {
    MyButton,
    // ShowSquare,
  },
};
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  div {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
