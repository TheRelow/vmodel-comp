<template>
  <div class="home">
    <sync-input v-bind:value.sync="inputData"></sync-input>
    {{ inputData }}
    <button @click="testEditVariable">check editing variable in parent component</button>
  </div>
</template>

<script>
import SyncInput from "../components/SyncInput";
export default {
  name: 'Home',
  components: { SyncInput },
  data: ()=>({
    inputData: '123',
  }),
  methods: {
    testEditVariable() {
      this.inputData = 'test text'
    },
  },
}
</script>