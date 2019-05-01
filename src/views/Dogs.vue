<template>
  <section>
    <h2>Dogs for adoption</h2>
    <b-table striped hover :items="dogs">
      <template slot="name" slot-scope="data">
        <router-link :to="`/pets/dogs/${data.index}`">{{ data.value }}</router-link>
      </template>
    </b-table>
  </section>
</template>

<script>
import { mapState } from 'vuex'

export default {
  data() {
    return {}
  },
  computed: {
    ...mapState(['dogs'])
  }
}
</script>
