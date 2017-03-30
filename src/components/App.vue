<template lang="html">
  <div>
    <jumbotron v-if="sign" :sign="sign"></jumbotron>
    <menus v-if="menus" :menus="menus"></menus>
    <gallry v-if="gallry" :gallry="gallry"></gallry>
    <history v-if="history" :history="history"></history>
    <location v-if="location" :location="location"></location>
    <foot v-if="location" :location="location"></foot>
  </div>
</template>

<script>
import axios from 'axios'
import _ from 'underscore'

import Jumbotron from './Jumbotron.vue'
import Menus from './Menus.vue'
import Gallry from './Gallry.vue'
import History from './History.vue'
import Location from './Location.vue'
import Foot from './Foot.vue'

export default {
  components: { Jumbotron, Menus, Gallry, History, Location, Foot },

  data() {
    return {
      sign: null,
      menus: null,
      gallry: null,
      history: null,
      location: null
    }
  },

  created() {
    this.fetchData()
  },

  methods: {
    fetchData() {
      var vm = this
      axios.get('/api/data.json')
           .then(response => {
             _.extend(vm, _.pick(response.data, ['sign', 'menus', 'gallry', 'history', 'location']))
           })
           .catch(error => error)
    }
  }
}
</script>

<style lang="css" src="./app.css">
</style>
