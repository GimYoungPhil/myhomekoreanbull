<template lang="html">
  <div class="container my-5" id="menus">
    <h2 class="text-muted">*1인 세팅비 3,000원</h2>
    <div class="row">
      <div class="col-md-6" v-for="menu in menus">
        <div class="menu-item d-flex justify-content-start py-3">
          <div class="p-2">
            <h1 class="display-3">{{ menu.name }}</h1>
          </div>
          <div class="ml-auto text-right p-2">
            <p class="mb-0">{{ menu.origin }}</p>
            <p class="mb-0">{{ menu.weight }}g</p>
            <p class="mb-0">{{ menu.price.toLocaleString('ko-KR', { style: 'currency', currency: 'KRW' }) }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['menus'],
  computed: {
    currency() {
      return menu.price.toLocaleString('ko-KR')
    }
  }
}
</script>

<style lang="css">
.menu-item {
  border-top: solid 1px rgba(0,0,0,.25);
}
</style>
