<template>
    <div>
      <PersonInfo v-show="!showFakePass" @myClick="onClick"></PersonInfo>
      <fake v-show="showFakePass" @clickToReturn="back" :personalInfo="personalInfo"/>
    </div>
</template>

<script>
import PersonInfo from './components/PersonInfo.vue'
import fake from './components/fake.vue'

export default {
  components: { fake, PersonInfo },
  data() {
    return {
      showFakePass: false,
      personalInfo: {
        name: "易玛㷩",
        stdId: 2020202020,
        dep: "计算机学院（国家示范性软件学院）",
        inOut: "允许出校",
        img: require("@/img/default.jpg"),
      },
    };
  },
  mounted() {
    document.body.addEventListener("touchstart", () => {});
  },
  methods: {
    onClick(pi) {
      this.personalInfo = pi;
      this.showFakePass = true;
    },
    back() {
      this.showFakePass = false;
    },
  },
};
</script>

<style>

</style>
