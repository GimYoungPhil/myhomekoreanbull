<template lang="html">
  <div class="container my-5" id="history">
    <blockquote class="blockquote " v-for="(record, index) in history" key="index">
      <p class="mb-0">{{ record.name }} <small>{{ record.location }}</small></p>
      <footer class="blockquote-footer">
        <cite title="Source Title">{{ record.period }}</cite>
      </footer>
    </blockquote>
  </div>
</template>

<script>
export default {
  props: ['history']
}
</script>

<style lang="css">
</style>
