<template>
  <div>
    <p>{{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: {
    content: {
      type: String,
      required: true
    }
  },
};
</script>

<style scoped>
</style>