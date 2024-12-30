<template>
  <div class="bg-cleangray h-dvh w-full flex overflow-hidden">
    <sideBar  />
    <div class="text-white w-full">
      <MainContent />
    </div>
    <RightSideBar />
    <footerConfig />  
  </div>
</template>

<script>
import sideBar from "@/components/sideBar/sideBar.vue"
import MainContent from "@/components/main/MainContent.vue"
import footerConfig from "@/components/footer/footerConfig.vue"
import RightSideBar from "@/components/sideBar/rightSideBar.vue";

export default {
  name: 'MainView',
  components: { 
    sideBar,
    MainContent,
    footerConfig,
    RightSideBar
  }
  
}
</script>
