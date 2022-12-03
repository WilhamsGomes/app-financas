<template>
    <v-app>
      <SideBar/>
      <SideBarRight/>
      <HeaderBar/>
    </v-app>
</template>

<script>

import SideBar from '@/components/SideBar.vue';
import SideBarRight from '@/components/SideBarRight.vue';
import HeaderBar from "@/components/HeaderBar.vue";

export default {
  name: 'HomeView',

  components: {
    SideBar,
    SideBarRight,
    HeaderBar
  },
};
</script>
