<template>
    <v-container>
      <SideBar/>
      <SideBarRight/>
      <HeaderBar/>
      <SubHeader/>
      <GraphicInicial/>
    </v-container>
</template>

<script>

import SideBar from '@/components/SideBar.vue';
import SideBarRight from '@/components/SideBarRight.vue';
import HeaderBar from "@/components/HeaderBar.vue";
import SubHeader from '@/components/SubHeader.vue';
import GraphicInicial from '@/components/GraphicInicial.vue';

export default {
  name: 'HomeView',

  components: {
    SideBar,
    SideBarRight,
    HeaderBar,
    SubHeader,
    GraphicInicial
  },
};
</script>
