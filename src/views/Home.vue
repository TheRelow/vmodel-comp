<template>
  <div class="home">
    <sync-input v-bind:value.sync="inputData"></sync-input>
    {{ inputData }}
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
}
</script>