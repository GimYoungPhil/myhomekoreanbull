<template lang="html">
  <div class="jumbotron jumbotron-fluid jumbotron-gallry">
    <div class="container">
      <div class="row">
        <div class="col-md-3" v-for="recode in gallry">
          <figure class="figure">
            <img :src="recode.src" class="img-thumbnail img-fluid" :alt="recode.alt">
            <figcaption class="figure-caption text-right">{{ recode.alt }}</figcaption>
          </figure>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['gallry']
}
</script>

<style lang="css">
.jumbotron-gallry {
  background-color: #9fbacb;
}
</style>
