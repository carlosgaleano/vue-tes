<template>
  <div id="app">
    <input id="input-text" type="text" v-model="msg">
    <div v-show="!msg" class="red" id="warning">Complete el mensaje </div>
    <span id="message" >{{ msg }}</span>
    <span id="full-name">{{ fullName }}</span>
    <button @click="toUppercase"  >Change firstName</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      msg: '',
      firstName: '',
      lastName: ''
    };
  },computed:{
    fullName(){
      return this.firstName+' '+this.lastName;
    }

  },
  methods:{
    toUppercase(){
      return this.firstName= this.firstName.toUpperCase();
    }


  }
};
</script>
<style>
.red {
  color: red;
}
</style>