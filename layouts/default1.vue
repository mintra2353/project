<template>
    <!-- ส่วนบนสุด -->
    <v-app>
      <v-card> 
       <v-app-bar
      color="#838B8B"
      dense
      dark
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Page title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <nuxt-link to="/login">
        <v-icon color="white">mdi-heart</v-icon>
        </nuxt-link>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
        <v-content>
          <nuxt/>
        </v-content>
    <!-- ส่วนเนื้อหา -->
  </v-card>
    </v-app>
</template>
