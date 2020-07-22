<template>
  <div>
    <h1>HELLO {{ name }}age:{{std}} </h1>
<v-text-field
        v-model="first"
        label="กรุณากรอกชื่อ"
        placeholder="กรุณากรอกชือของท่าน"
        outlined
        shaped
     
     ></v-text-field>
 <v-text-field
            outlined
            label="Append"
            append-icon="mdi-map-marker"
          ></v-text-field>
<v-text-field
            v-model="message"
            solo
            label="Solo"
            clearable
          ></v-text-field>
<v-text-field
            label="Filled"
            placeholder="Dense & Rounded"
            filled
            rounded
            dense
          ></v-text-field>          
  </div>
</template>
<script>
export default {
  data:function(){
    return{
     name:"alongkorn",
     age:45,
     dep:"information  technology"

    }
  }
}
</script>
<script>
  export default {
    data () {
      return {
        message: 'HELLO!',
      }
    },
  }
</script>