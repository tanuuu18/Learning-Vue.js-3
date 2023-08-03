<template>
  <h2>Hello {{ name }}, {{ profile }}!!</h2>
</template>
<script>
export default {
  name: "Greet",
  props: ["name"],
};
</script>
