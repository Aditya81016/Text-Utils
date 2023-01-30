<template>
  <button type="button" class="btn btn-outline-primary" v-html="text"></button>
  <div class="container popover">
    <div class="title">{{ title }}</div>
    <div class="content">{{ content }}</div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Butt",
  props: {
    text: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    content: {
      type: String,
    },
    type: {
      type: String,
      default: "primary",
    },
  },
};
</script>

<style scoped>
button {
  border-width: 3px;
  transform: scale(0.7);
}

button:hover + .popover {
  display: block;
}

.popover {
  position: absolute;
  z-index: 1000;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 5px;
  padding: 10px;
  display: none;
  transform: translate(0px, -120px);
}

.title {
  font-size: 16px;
  font-weight: bold;
}

.content {
  font-size: 14px;
  color: rgba(255, 255, 255, 0.7);
}
</style>
