<template>
  <div class="forms">
    <div style="height: 0px"></div>
    <div class="toptabla">
      <div class="toptabla_con">
        <div class="formsTop_left">
          <span class="iconcolor1 iconfont" style="font-weight: bold"
            >&#xe98e;</span
          >
          <p>当前部门：{{personalInfo.dep}}</p>
        </div>
        <img
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACoAAAAYCAYAAACMcW/9AAAB4ElEQVRYR83VO0sDQRAA4Nm9LfMbBBEsBC1EEFGUJblcOEihP8Je8YnYiPhErf0Rlja729j4C6wUE1+o+AAtlMiaHTmJcsYkbi6R3FVX7Mx+Nzs7RwAAhBCCEOIG73F8KKU+UUqNI+JuHIEh03UAPUDE4ZhD34mUcg8AxmIPVUoNIOJhzKH7JABKKScAYDuOWES8SiQSnZ/QEnYaADZihj1mjI1wzm+/oaUxtUQIWYwJNo+IQ+l0+jrw/ICWKrsAAMstxt5prdt833/7cvyCthpLCDlzHGcgOO5wsSpCW4g9oZS6yWTyvPxEq0JbgL0wxnR5nvdSqe1qQoMApdQMIq7/c8/eaK3bwz1ZV0W/Fiul5hFx5Z+wuWKxOJTJZG5q5f+zoqE5OwcAq03G5hhjg+UXJ9LRh4Oa3Aa3hUKhI5vNvtp8vHVFm9wGl4yxXs75gw2y4sC3CWywsnmtdb/v+/c2e9Uc+DYJlFKTiLhlsza05hIAul3Xfa4z7vcvtJ4EQohZQsiaTUzwxwGAvlQq9WizPtJ4qpXYEpsv9eRTFGTkHi3fTEo5BQCbVRAXANAT5bjD+eq+9dUqUgV7ZIxJep53F7WSDV+mShsLIUYppSPGmASl9NRxnB3OeaFRZBD/ATVSvUcGtzefAAAAAElFTkSuQmCC"
          alt=""
          class="toptabla_img"
          @click="$emit('clickToReturn')"
        />
      </div>
    </div>
    <div class="toptabla">
      <div class="toptabla_con">
        <div class="formsTop_left">
          <span class="iconcolor1 iconfont" style="font-weight: bold"
            >&#xe715;</span
          >
          <p class="">请假外出、返校权限查询</p>
        </div>
      </div>
    </div>
    <!-- 姓名 -->
    <div class="">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >姓名</span
        >
      </div>
      <div class="plugin-allbox">
        <div
          data-key="User_3"
          class="dplugin-box"
          style="margin-top: 0px; margin-bottom: 0px; text-align: center"
        >
          <div class="dplugin-mobile dplugin-doneplugin dplugin-mobile-dinput">
            <span
              class="doneplugin-value doneplugin-value-userview"
              style="
                font-size: 14px;
                font-family: 微软雅黑;
                font-weight: normal;
                font-style: normal;
                color: rgb(96, 98, 102);
                text-decoration: none;
                text-align: center;
                line-height: 15px;
                letter-spacing: 0px;
              "
              >{{ personalInfo.name }}</span
            >
          </div>
        </div>
      </div>
    </div>
    <!-- 照片 -->
    <div class="">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >照片</span
        >
      </div>
      <div class="plugin-allbox">
        <div
          data-key="Avatar_41"
          class="dplugin-box"
          style="margin-top: 0px; margin-bottom: 0px; text-align: center"
        >
          <div class="dplugin-mobile dplugin-mobile-dAvatar">
            <div
              class="dplugin-mobile-addfileed-box"
              style="height: 100px; width: 100px; margin: auto"
            >
              <img
                :src="personalInfo.img"
                alt="photo"
                style="height: 100px; width: 100px"
              />
            </div>
            <div class="clear"></div>
          </div>
        </div>
      </div>
    </div>
    <!-- 动态图 -->
    <div class="mobile_pluginnames_hide">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >动态图</span
        >
      </div>
      <div class="plugin-allbox">
        <div
          data-key="Image_36"
          class="dplugin-box"
          style="margin-top: 0px; margin-bottom: 0px; text-align: left"
        >
          <div class="dplugin-mobile dplugin-mobile-dImage dImageview">
            <img
              src="../img/colorful.gif"
              style="width: 100%; height: 100%"
            />
          </div>
        </div>
      </div>
    </div>
    <!-- 状态码 -->
    <div class="">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >状态码</span
        >
      </div>
      <div class="plugin-allbox" plugin="[object Object]">
        <div
          data-key="Qrcode_11"
          class="dplugin-box"
          style="
            margin-top: 0px;
            margin-bottom: 0px;
            width: 100%;
            text-align: center;
            height: 100%;
            overflow-x: auto;
          "
        >
          <div class="dplugin-mobile">
            <img
              src="../img/pass.png"
              id="Qrcode_11_qrcodecanvas"
              height="150"
              width="150"
              style="height: 150px; width: 150px"
            />
          </div>
        </div>
      </div>
    </div>
    <!-- 允许入校 -->
    <div class="mobile_pluginnames_hide">
      <div
        class="pluginnames"
        style="min-height: 0.1rem; padding: 0px 15px"
      ></div>
      <div
        data-key="Input_12"
        class="dplugin-box"
        style="margin-top: 0px; margin-bottom: 0px; text-align: center"
      >
        <div
          class="
            dplugin-mobile dplugin-mobile-dinput
            dinput-vie
            dplugin-mobile-dinput-focusalert
          "
          style="
            font-size: 18px;
            font-family: 微软雅黑;
            font-weight: bold;
            font-style: normal;
            color: green;
            text-decoration: none;
            text-align: center;
            line-height: 20px;
            letter-spacing: 0px;
          "
        >
          <span id="yunxu"
            style="
              font-size: 18px;
              font-family: 微软雅黑;
              font-weight: bold;
              font-style: normal;
              color: green;
              text-decoration: none;
              text-align: center;
              line-height: 20px;
              letter-spacing: 0px;
            "
            >{{personalInfo.inOut}}</span
          >
        </div>
      </div>
    </div>
    <!-- 学工号 -->
    <div class="">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >学工号</span
        >
      </div>
      <div class="plugin-allbox">
        <div
          data-key="User_5"
          class="dplugin-box"
          style="margin-top: 0px; margin-bottom: 0px; text-align: center"
        >
          <div class="dplugin-mobile dplugin-doneplugin dplugin-mobile-dinput">
            <span
              class="doneplugin-value doneplugin-value-userview"
              style="
                font-size: 14px;
                font-family: 微软雅黑;
                font-weight: normal;
                font-style: normal;
                color: rgb(96, 98, 102);
                text-decoration: none;
                text-align: center;
                line-height: 15px;
                letter-spacing: 0px;
              "
              >{{personalInfo.stdId}}</span
            >
          </div>
        </div>
      </div>
    </div>
    <!-- 出入校时间 -->
    <div class="">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >出入校时间</span
        >
      </div>
      <div class="plugin-allbox">
        <div
          data-key="Calendar_15"
          class="dplugin-box"
          style="margin-top: 0px; margin-bottom: 0px; text-align: center"
        >
          <div
            class="dplugin-mobile dplugin-mobile-dCalendar dCalendar-vie"
            style="
              font-size: 14px;
              font-family: 微软雅黑;
              font-weight: normal;
              font-style: normal;
              color: rgb(96, 98, 102);
              text-decoration: none;
              text-align: center;
              line-height: 20px;
              letter-spacing: 0px;
            "
          >
            <span
              style="
                font-size: 14px;
                font-family: 微软雅黑;
                font-weight: normal;
                font-style: normal;
                color: rgb(96, 98, 102);
                text-decoration: none;
                text-align: center;
                line-height: 20px;
                letter-spacing: 0px;
              "
              >{{ timeNow }}</span
            >
          </div>
        </div>
      </div>
    </div>
    <!-- 学院 -->
    <div class="">
      <div class="pluginnames">
        <span
          style="
            color: rgb(135, 135, 135);
            font-size: 14px;
            font-family: 微软雅黑;
            line-height: 22px;
          "
          >学院</span
        >
      </div>
      <div class="plugin-allbox">
        <div
          data-key="User_22"
          class="dplugin-box"
          style="margin-top: 0px; margin-bottom: 0px; text-align: center"
        >
          <div class="dplugin-mobile dplugin-doneplugin dplugin-mobile-dinput">
            <span
              class="doneplugin-value doneplugin-value-userview"
              style="
                font-size: 14px;
                font-family: 微软雅黑;
                font-weight: normal;
                font-style: normal;
                color: rgb(96, 98, 102);
                text-decoration: none;
                text-align: center;
                line-height: 15px;
                letter-spacing: 0px;
              "
              >{{personalInfo.dep}}</span
            >
          </div>
        </div>
      </div>
    </div>
    <!-- 更多 -->
    <div class="wxformbtn m_start_btn" @click="changeInOut">
      <button class="draftdiv active">更多</button>
      <div class="wxformbtn_center"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "fake",
  props: ["personalInfo"],
  methods: {
    changeInOut() {
        this.personalInfo.inOut =
        this.personalInfo.inOut === "允许出校" ? "允许入校" : "允许出校";
    },
  },
  computed: {
    timeNow() {
      let moment = require("moment");
      return moment().format("YYYY-MM-DD HH:mm:ss");
    },
  },
};
</script>

<style src="../css/iconfont.css"></style>
<style src="../css/style.css"></style>