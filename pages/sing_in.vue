<template>
    <center>
    <div style="padding-top: 20px;">
        <img src="images/mi.jpg" style="width: 80px; height: 100px;border-radius: 50%">
    </div>

    <v-card color="#BEBEBE" height="300px">
       <v-form>
           <br><br>
         <v-text-field label="Username"outlined dense
          />
         <v-text-field label="Password"outlined dense
          />
    <v-checkbox
      v-model="checkbox"
      label="Remember me"
      required
    ></v-checkbox>
       </v-form> 
       
        <nuxt-link to="des">
        <div class="text center" align="center">
            <v-btn width="340px" color="primary dark">SIGN IN</v-btn>
        </div>
    </nuxt-link>
    </v-card>

</center>
</template>
<script>
export default {
    layout: 'default02',
}
</script>
