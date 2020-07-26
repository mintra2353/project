<template>
<center>
<div>
    <h1>Welcom!</h1>
    <h2>Below is a list of all the <br>components that support the app</h2>
    <br>
        <div class="box1" style="padding-top: -30px%;">
            <img src="images/mi.jpg" style="width: 260px;height: 320px;margin-top: -10px;" >
        </div>
    <br>
    <nuxt-link to="sing_in">
        <div class="text center" align="center">
            <v-btn width="340px" color="primary dark">SIGN IN</v-btn>
        </div>
    </nuxt-link>
</div>
</center>
</template>
<script>
export default {
    layout: 'default01',
}
</script>
<style>
.box1 {
  background: #757575;
  width: 300px; 
  height: 300px;
}
</style>