<template>
  <button class="btn" :style="{ backgroundColor: bgColor}"> {{ name }} </button>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    name: String,
    bgColor: {
      type: String,
      required: true,
      default() {
        return '#ffffff';
      },
      validator(value) {
        return value.includes('#');
      },
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .btn {
    width: 8rem;
    height: 2rem;
    display: inline-block;

    border-radius: 0.5rem;
    text-decoration: none;
    border: none;
    color: white;

    margin: 0.5rem;
  }
</style>
