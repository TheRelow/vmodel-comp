<template>
  <label>
    sync input
    <br>
    <input type="text" v-model="input">
  </label>
</template>

<script>
export default {
  name: "CustomInput",
  components: {},
  data: ()=>({
    input: ''
  }),
  props: [ 'value' ],
  created() {
    this.input = this.value
  },
  watch: {
    input: function (val) {
      this.$emit('update:value', val)
    },
    value: function (val) {
      this.input = val
    }
  }
}
</script>