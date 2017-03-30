<template lang="html">
  <div class="container my-5" id="location">
    <div class="row">
      <div class="col-md-8">
        <iframe width="100%" height="400" frameborder="0" style="border:0" src="https://www.google.com/maps/embed/v1/place?q=%EC%84%9C%EC%9A%B8%20%EC%9D%80%ED%8F%89%EA%B5%AC%20%EC%8B%A0%EC%82%AC1%EB%8F%99%2018-44&key=AIzaSyA85gqPOz-2I3YDgNiNoVsMQ7ZQQ_a2BLw" allowfullscreen></iframe>
      </div>
      <div class="col-md-4">
        주소:
        <p>{{ location.address }}</p>
        <p>{{ location.tel }}</p>
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




