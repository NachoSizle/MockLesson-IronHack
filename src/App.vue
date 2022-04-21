<template>
  <div class="main-container">
    <h1>VueJS: Props</h1>
    <MyButton name="OK" bgColor="rgb(4, 170, 109)"/>
    <MyButton name="KO" bgColor="rgb(204, 66, 39)"/>
    <MyButton name="WARNING" bgColor="rgb(235, 186, 52)"/>

    <h2>Different props</h2>
    <ShowSquare
      v-bind:bgColors="['green', 'red', 'brown', 'blue', 'black']">
    </ShowSquare>
  </div>
</template>

<script>
import MyButton from './components/MyButton.vue';
import ShowSquare from './components/ShowSquare.vue';

export default {
  name: 'App',
  components: {
    MyButton,
    ShowSquare,
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
