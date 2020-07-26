<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app clipped>
      <lang-selector />
      <template v-slot:prepend>
        <v-list-item two-line>
          <v-list-item-avatar>
            <img src="../static/images/m.jpg" />
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>มินตรา จิตโคตร</v-list-item-title>
            <v-list-item-subtitle>เข้าสู่ระบบ</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item v-for="item in items" :key="item.title" @click>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <div>
      <v-app-bar color="deep-purple accent-4" dense dark>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

        <v-toolbar-title>Page title</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-menu left bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn icon v-bind="attrs" v-on="on">
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </template>

          <v-list>
            <v-list-item v-for="n in 5" :key="n" @click="() => {}">
              <v-list-item-title>Option {{ n }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-app-bar>
    </div>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <v-content>
          <nuxt/>
      </v-content>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>
<script>
import LangSelector from "~/components/lang-selector.vue";

export default {
  components: {
    LangSelector,
  },

  computed: {
    drawer: {
      get() {
        return this.$store.state.drawer;
      },
      set(v) {
        this.$store.commit("setDrawer", v);
      },
    },
  }, // computed
  data () {
      return {
        items: [
          { title: 'Home', icon: 'mdi-home-city' },
          { title: 'ประวัติ', icon: 'assignment_ind' },
          { title: 'สมาชิก', icon: 'mdi-account-group-outline' },
          { title: 'สินค้าแนะนำ', icon: 'local_grocery_store' },
          { title: 'สินค้าขายดี', icon: 'star_outline' },
          { title: 'บทความ', icon: 'format_align_left' },
          { title: 'ถาม-ตอบ', icon: 'comment' },
        ],
      }
    },

  watch: {
    "$store.state.lang"() {
      this.$i18n.locale = this.$store.state.lang;
    },
  }, // watch
};
</script>