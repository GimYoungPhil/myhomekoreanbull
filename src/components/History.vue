<template lang="html">
  <div class="container my-5" id="history">
    <h1>연혁</h1>
    <table class="table">
      <tr v-for="record in history">
        <td>{{ record.name }}</td>
        <td>{{ record.location }}</td>
        <td>{{ record.period }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: ['history']
}
</script>

<style lang="css">
</style>
