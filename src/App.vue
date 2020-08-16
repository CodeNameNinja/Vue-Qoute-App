<template>
  <div class="container">
    <app-header :maxQoutes="maxQoutes" :qouteCount="qoutes.length"></app-header>
    <app-new-qoute @qouteAdded="newQoute"></app-new-qoute>
    <app-qoute-grid :qoutes="qoutes" @qouteDeleted="deleteQoute"></app-qoute-grid>
    <div class="r">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Infor: Click on a Qoute to delete it.</div>
      </div>
    </div>
  </div>
</template>

<script>
import QouteGrid from './components/QouteGrid';
import NewQoute from './components/NewQoute';
import Header from './components/Header';
export default {
  data: function(){
    return{
      qoutes:[
        'Just a Qoute'
      ],
      maxQoutes: 10
    }
  },
  components:{
    'appQouteGrid':QouteGrid,
    'appNewQoute':NewQoute,
    'appHeader':Header
  },
  methods:{
    newQoute(qoute){
      if(this.qoutes.length >= this.maxQoutes){
        return alert('Max Qoute Limit reached, delete some qoutes to free up space!')
      }
      this.qoutes.push(qoute);
    },
    deleteQoute(index){
      this.qoutes.splice(index,1);
    }
  }
};
</script>

<style>
</style>
