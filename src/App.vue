<template>
  <div id="app">
    <SideMenu />
    <div id="appWrapper">
      <MainSection />

      <UnderLine />
      <InfoSection />
      <UnderLine />
      <CommentSection />
    </div>
  </div>
</template>

<script>
import SideMenu from "@/components/SideMenu/SideMenu";
import MainSection from "@/features/mainSection/MainSection";
import UnderLine from "@/components/UnderLine/UnderLine.vue";
import InfoSection from "@/features/infoSection/InfoSection";
import CommentSection from "@/features/commentSection/CommentSection";
export default {
  name: "App",
  components: {
    SideMenu,
    MainSection,
    UnderLine,
    InfoSection,
    CommentSection,
  },
};
</script>

<style>
#app {
  font-family: "Montserrat", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #2a2e31;
  user-select: none;
}
#appWrapper {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
img {
  -webkit-user-drag: none;
  -khtml-user-drag: none;
  -moz-user-drag: none;
  -o-user-drag: none;
  -user-drag: none;
}
</style>
