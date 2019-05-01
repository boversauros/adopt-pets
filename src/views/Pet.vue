<template>
  <section>{{animal.name}}</section>
</template>

<script>
import { mapState } from "vuex"

export default {
  data() {
    return {
      animal: {}
    }
  },
  computed: {
    ...mapState(["cats", "dogs"])
  },
  mounted() {
    const animal = this[this.$route.params.species][this.$route.params.id]
    this.animal = animal
  }
}
</script>
