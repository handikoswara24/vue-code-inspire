<template>
  <div>
    <div class="alert" :class="mode" role="alert">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: ["mode"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.primary {
  color: #004085;
  background-color: #cce5ff;
  border-color: #b8daff;
}
.success {
  color: #fff;
  background-color: #4caf50;
  border-color: #4caf50;
}
.danger {
  color: #fff;
  background-color: #f44336;
  border-color: #f44336;
}
.alert {
  position: relative;
  padding: 0.75rem 1.25rem;
  margin-bottom: 1rem;
  border: 1px solid transparent;
  border-radius: 0.25rem;
}
</style>
