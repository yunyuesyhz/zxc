<template>
  <div class="backgroundDiv">
      <div class="piContainer glass">
        <div class="nameBlock inputBlock glass">
          <span>姓名</span>
          <input type="text" v-model="name" />
        </div>
        <div class="stdNum inputBlock glass">
          <span>学号</span>
          <input type="text" v-model="stdId" />
        </div>
        <div class="personalImage chooseAPhoto glass">
          <div @click="chooseAPhoto()">选择照片</div>
          <input type="file" name="file" hidden @change="fileChanged()" />
        </div>
        <select class="glass select" name="inOut" id="dep" v-model="dep">
          <option value="计算机学院（国家示范性软件学院）">计算机学院</option>
          <option value="人工智能学院">人工智能学院</option>
          <option value="信息通信工程学院">信息通信工程学院</option>
          <option value="网络空间安全学院">网络空间安全学院</option>
          <option value="经济管理学院">经济管理学院</option>
          <option value="数字媒体与设计艺术学院">数字媒体</option>
          <option value="应急管理学院">应急管理学院</option>
          <option value="电子工程学院">电子工程学院</option>
          <option value="理学院">理学院</option>
          <option value="马克思主义学院">马克思主义学院</option>
          <option value="网络教育学院（继续教育学院）">网络教育学院</option>
          <option value="现代邮政学院（自动化学院）">现代邮政学院</option>
          <option value="人文学院">人文学院</option>
          <option value="国际学院">国际学院</option>
        </select>
        <select class="glass select" name="inOut" id="inOut" v-model="inOut">
          <option value="允许出校">允许出校</option>
          <option value="允许入校">允许入校</option>
        </select>
      </div>
      <div
        class="button glass"
        @click="openGateClicked({ name, stdId, inOut, img, dep })"
      >
        开启自由门
      </div>
  </div>
</template>

<script>
export default {
  name: "personalInfo",
  data() {
    return {
      name: "堕落天使",
      stdId: 2021202121,
      dep: "电子工程学院",
      inOut: "允许出校",
      img: require("@/img/default.jpg"),
    };
  },
  methods: {
    openGateClicked(pi) {
      this.$emit("myClick", pi);
    },
    chooseAPhoto() {
      document.querySelector("input[type=file]").click();
    },
    fileChanged() {
      // this.img = URL.createObjectURL(document.querySelector("input[type=file]").files[0]);
      // localStorage.setItem("img", this.img);
      let fileReader = new FileReader();
      fileReader.onloadend = () => {
        this.img = fileReader.result;
        localStorage.setItem("img", this.img);
      };
      fileReader.readAsDataURL(
        document.querySelector("input[type=file]").files[0]
      );
    },
  },
};
</script>

<style lang="scss" scoped>
$unified_width: 280px;
$outer_border_radius: 30px;
.glass {
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  box-shadow: 4px 4px 30px 0 rgba(27, 0, 37, 0.4);
}
div.backgroundDiv {
  width: 100%;
  height: 100vh;
  color: white;
  background: linear-gradient(
    135deg,
    hsl(170deg, 80%, 70%),
    hsl(190deg, 80%, 70%),
    hsl(250deg, 80%, 70%),
    hsl(320deg, 80%, 70%)
  );
  background-size: 200% 200%;
  animation: gradient-move 10s ease alternate infinite;
  @keyframes gradient-move {
    0% {
      background-position: 0% 0%;
    }
    100% {
      background-position: 100% 100%;
    }
  }
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  div.piContainer {
    width: $unified_width;
    height: 350px;
    border-radius: $outer_border_radius;
    display: flex;
    background-color: rgba(0, 0, 0, 0.4);
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    div.chooseAPhoto {
      width: 80%;
      background-color: rgba(0, 0, 0, 0.2);
      padding: 10px;
      border-radius: 15px;
      align-items: center;
      text-align: center;
      font-weight: bold;
    }
    div.inputBlock {
      width: 80%;
      background-color: rgba(0, 0, 0, 0.2);
      padding: 3px;
      border-radius: 15px;
      display: flex;
      align-items: center;
      span {
        margin-right: 10px;
        border-radius: 15px;
        font-weight: bold;
        letter-spacing: 1px;
        padding: 7px;
        background-color: rgba(0, 0, 0, 0.2);
      }
      input {
        letter-spacing: 1px;
        outline: none;
        border: 0;
        color: white;
        background-color: rgba(0, 0, 0, 0);
      }
    }
    select {
      width: 80%;
      text-align: center;
      background-color: rgba(0, 0, 0, 0.2);
      outline: none;
      border: 0;
      font-size: 16px;
      font-weight: bold;
      color: white;
      padding: 9px 10px;
      border-radius: 15px;
    }
  }
  div.button {
    width: $unified_width;
    margin-top: 20px;
    padding: 20px 0;
    font-size: 25px;
    font-weight: bold;
    text-align: center;
    letter-spacing: 5px;
    border-radius: $outer_border_radius;
    background-color: rgba(0, 0, 0, 0.4);
    transition: background-color 0.5s ease-out;
  }
  div.button:active {
    background-color: rgba(0, 0, 0, 0.7);
  }
}
</style>