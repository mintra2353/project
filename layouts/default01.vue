<template>
    <!-- App.vue -->

<v-app>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container fluid>

      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

</v-app>
</template>
<style>
#app {
  background: white; /* For browsers that do not support gradients */
}
h1{
    color: black;
    text-align: center;
}
h2{
    color: gray;
    font-size: 12px;
    text-align: center;
}
</style>