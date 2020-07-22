<template>
<div>
    <v-container>
        <v-card
            color="#AB82FF"
            dark
            height="400"
          ><center>
            <v-card-title class="headline">ประวัติของฉัน</v-card-title>
            <v-img
             src="https://scontent.fbkk22-6.fna.fbcdn.net/v/t1.0-9/25158246_1948790398706809_1054861765606753251_n.jpg?_nc_cat=102&_nc_sid=7aed08&_nc_eui2=AeH8K4Au42nBC5-zbn0LpapsMrqeo6cnSAkyup6jpydICeR34LX2DwW5_zh656XGVf4dcMpOzrbWjjQD7KCgmqx3&_nc_ohc=n5zewXt0tvkAX9xNX49&_nc_ht=scontent.fbkk22-6.fna&oh=4525ad92b50661521241bb652e7b54e4&oe=5F3C372D"
             height="200px"
             width="200px"
            ></v-img>
            <br>
            <v-card-subtitle>ชื่อ นางสาวมินตรา จิตโคตร <br> ที่อยู่ 34 ม.8 ต.กุดชุมแสง อ.หนองบัวแดง จ.ชัยภูมิ <br> 
            ศึกษาที่ วิทยาลัยเทคนิคชัยภูมิ แผนกเทคโนโลยีสารสนเทศ ชั้น ปวส.2
            </v-card-subtitle>
            </center>
          </v-card>
          <br>
          <center>
           <nuxt-link to="/home">
              <v-btn rounded color="#ECAB53">Black</v-btn>
            </nuxt-link>
            </center>
    </v-container>
</div>
</template>
<script>
export default {
    layout:"public",
}
</script>