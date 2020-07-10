<template>
   <v-card>
     <v-card-title>
       <h1>Login</h1>
     </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field label="Username"
          prepend-icon="mdi-account-circle"
          />
          <v-text-field
            type="Password"
            label="Password"
            prepend-icon="lock" append-icon="visibility_off"
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
   </v-card>
</template>