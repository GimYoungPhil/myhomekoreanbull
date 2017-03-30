<template lang="html">
  <div class="jumbotron jumbotron-fluid">
    <div class="container">
      <h1 class="display-2 wf-jeju">{{ sign.title }}</h1>
      <p class="lead">{{ sign.subTitle }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['sign']
}
</script>

<style lang="css">
</style>
