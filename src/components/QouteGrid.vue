<template>
  <div class="row">
      <app-qoute v-for="(qoute, index) in qoutes" :key="index" @click.native="deleteQoute(index)">
          {{qoute}}
      </app-qoute>
  </div>
</template>

<script>
import Qoute  from "./Qoute";
export default {
  props: ['qoutes'],
  components: {
    "app-qoute": Qoute,
  },
  methods:{
      deleteQoute(index){
          this.$emit('qouteDeleted', index)
      }
  }
};
</script>

<style scoped>
</style>