<template>
  <div id="app">
    <button type="button" class="btn" @click="showModal">Open Modal!</button>
    <modal v-show="isModalVisible" @close="closeModal"></modal>
  </div>
  
</template>

<script>

import modal from './components/modal';

export default {
  name: 'app',
  components:{
    modal:modal
  },
  data () {
    return {
    isModalVisible:false
    }
  },
  methods:{
    showModal(){
      this.isModalVisible = true;
    },
    closeModal(){
      this.isModalVisible = false;
    }
  }
}
</script>

<style>

</style>
