<template>
  <div>
    <h2>Hello: {{ name }}</h2>
    <h2>age: {{ age }}</h2>
    <input type="text" :value="name">
    <input type="text" v-model="name">
    <div><button @click="doSave">SAVE</button></div>
    <div><button @click="doMENU">MAIN MENU</button></div>
    <div><button @click="doHome">HOME</button></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "Mintra Jitkote",
      age: 33,
    }
  },
  methods:{
    doSave(){
    console.log("DO SAVE");
    },
    doMENU(){
    this.$router.push('menu_act')
   },
   doHome(){
    this.$router.push('/')
   } 
  },
}
</script>