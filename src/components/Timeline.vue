<template>
  <div class="timeline">
    <h1>Timeline</h1>
    <ul>
      <twit v-for="(key, twit) in timeline" v-bind:key="key" />
    </ul>
  </div>
</template>

<script>
import Twit from '@/components/Twit.vue'

export default {
  name: 'Timeline',
  components: {
    Twit
  },
  computed: {
    timeline () {
      return Array(10)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>
