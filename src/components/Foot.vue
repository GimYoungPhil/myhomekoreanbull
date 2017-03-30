<template lang="html">
  <div class="jumbotron jumbotron-fluid mb-0">
    <div class="container">
      <div class="content text-left">
        <p class="lead mb-0">{{ location.address }}</p>
        <p class="lead"><a href="tel:02-385-3293">{{ location.tel }}</a></p>
        <p class="mb-0">
          <em>Copyright © 2017</em>
          내고향 한우방 정육식당
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['location']
}
</script>

<style lang="css">

</style>
