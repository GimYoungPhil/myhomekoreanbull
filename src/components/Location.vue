<template lang="html">
  <div class="container my-5" id="location">
        <iframe width="100%" height="400" frameborder="0" style="border:0"  scrolling="no" v-bind:src="`https://www.google.com/maps/embed/v1/place?q=${urlAddress}&key=AIzaSyA85gqPOz-2I3YDgNiNoVsMQ7ZQQ_a2BLw`" allowfullscreen></iframe>
  </div>
</template>

<script>
export default {
  props: ['location'],

  computed: {
    urlAddress() {
      return encodeURI(this.location.address)
    }
  }
}
</script>

<style lang="css">
</style>




