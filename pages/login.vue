<template>
    <center>
   <v-card width="400" color="#FF6347">
     <v-card-title>
       <h1>Login</h1>
     </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field label="Username"
          prepend-icon="mdi-account-circle"
          />
          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            label="Password"
            prepend-icon="mdi-lock" 
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
            />
       </v-form>
     </v-card-text>
     <v-card-actions>
         <nuxt-link to="/register">
       <v-btn color="green">REGISTER</v-btn>
         </nuxt-link>
        <v-spacer></v-spacer>
       <v-btn color="info">LOGIN</v-btn>
    </v-card-actions>  
     <nuxt-link to="/">
        <v-btn rounded color="teal">กลับหน้าหลัก</v-btn>
    </nuxt-link>
   </v-card>
   </center>
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      showPassword: false
    }
  }
}
</script>