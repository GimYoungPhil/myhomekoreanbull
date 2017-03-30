<template lang="html">
  <div class="container my-5" id="menus">
    <h1>메뉴</h1>
    <table class="table">
      <tr v-for="menu in menus">
        <td>{{ menu.name }}</td>
        <td>{{ menu.weight }}</td>
        <td>{{ menu.price }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: ['menus']
}
</script>

<style lang="css">
</style>
