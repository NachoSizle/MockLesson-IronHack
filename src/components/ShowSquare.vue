<template>
  <div>
    <h3>Now, render {{ numOfSquares }} squares!</h3>
     <div class="container--squares">
      <div class="square"
        v-for="(color, index) in bgColors"
        :key="color"
        :style="{ backgroundColor: color }">
        {{ index + 1 }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ShowSquare',
  props: {
    bgColors: {
      type: Array,
      required: true,
      default() {
        return ['green', 'blue'];
      },
    },
  },
  computed: {
    numOfSquares() {
      return this.bgColors.length;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 0;
  }
  .container--squares {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .square {
    width: 4rem;
    height: 4rem;

    border-radius: 0.5rem;
    text-decoration: none;
    border: none;
    color: white;

    margin: 0.5rem;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }
</style>
