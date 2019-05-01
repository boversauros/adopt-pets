<template>
  <section>
    <h2>Cats for adoption</h2>
    <b-table striped hover :items="cats">
      <template slot="name" slot-scope="data">
        <router-link :to="`/pets/cats/${data.index}`">{{ data.value }}</router-link>
      </template>
    </b-table>
  </section>
</template>

<script>
import { mapState } from "vuex"

export default {
  data() {
    return {}
  },
  computed: {
      ...mapState(['cats'])
  }
};
</script>
