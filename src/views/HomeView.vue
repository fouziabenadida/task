<template>
<v-app :style="{background: $vuetify.theme.themes.dark.background}">
<side-bar/>
<right-side-bar/>
</v-app>
</template>

<script>
import SideBar from '@/components/SideBar.vue'
import RightSideBar from '@/components/RightSideBar.vue'


  export default {
    name: 'HomeView',
  components:{
    SideBar,
    RightSideBar,
  }
    
    
  }
</script>
