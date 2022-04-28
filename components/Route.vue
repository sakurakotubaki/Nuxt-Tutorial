<template>
  <div class="box">
    <div class="one"><NuxtLink to="/about">About Page</NuxtLink></div>
    <div class="two"><NuxtLink to="/info">Info Page</NuxtLink></div>
    <div class="three"><NuxtLink to="/http">HTTP Page</NuxtLink></div>
  </div>
</template>

<script>
export default {
  name: 'RouteComponent',
}
</script>

<style scoped>
.box {
  display: flex;
}

.one {
  flex: 1 1 auto;
}

.two {
  flex: 1 1 auto;
}

.three {
  flex: 1 1 auto;
}
</style>
