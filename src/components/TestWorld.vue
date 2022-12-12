<template>
    <h2>{{ title }}</h2>
    <button @click="undo">undo</button>
    <button @click="redo">redo</button>
    <div @click="showCircle" class="container">
    <div
      class="circle"
      v-if="circleX && circleY"
      :style="{
        position: 'absolute',
        display: `${display}`,
        top: `${circleY}px`,
        left: `${circleX}px`,
      }"
    >
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  props: {
    title: String,
  },
  data() {
    return {
      score: 0,
      circleX: undefined,
      circleY: undefined,
      display: 'inline',
      timer: undefined,
    };
  },
  methods: {
    showCircle(e) {
      this.circleX = e.pageX;
      this.circleY = e.pageY;
      console.log(this.circleX + " " + this.circleY);
    },
    undo() {
        this.display = 'none'
  },
  redo() {
    this.display = 'inline'
  }
}
}
</script>

<style scoped>
.circle {
  border: 1px solid black;
  width: 60px;
  height: 60px;
  border-radius: 50%;
}

.container {
  height: 100vh;
  margin: 0 auto;
}

button {
    width: 100px;
    padding: 5px;
    margin: 5px;
}
</style>
