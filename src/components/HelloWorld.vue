<template>
  <p>
    fromComponent: {{ fromComponent }}
  </p>
  <p>
    fromMixin: {{ fromMixin }}
  </p>
  <p>
    length (this.fromMixin.length accessed in component data() func): {{ length }}
  </p>
</template>

<script>
import testMixin from './test-mixin'

export default {
  mixins: [testMixin],
  data() {
    return {
      fromComponent: "COMP_DATA",
      length: this.fromMixin.length,
    }
  }
}
</script>
