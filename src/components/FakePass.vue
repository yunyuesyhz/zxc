<template>
  <div class="forms">
    <div style="height: 0px"></div>
    <div class="toptabla">
      <div class="toptabla_con">
        <div class="formsTop_left">
          <span class="iconcolor1 iconfont" style="font-weight: bold"
            >&#xe623;</span
          >
          <p>当前部门：计算机学院（国家示范性软件学院）</p>
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
            >&#xe606;</span
          >
          <p class="">请假外出、返校权限查询</p>
        </div>
      </div>
    </div>
    <div>
      <div element-loading-custom-class="area-vloading" class="m_formList">
        <!---->
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
            <!---->
          </div>
          <!---->
          <div class="plugin-allbox">
            <div
              data-key="User_3"
              class="dplugin-box"
              style="margin-top: 0px; margin-bottom: 0px; text-align: center"
            >
              <div
                class="dplugin-mobile dplugin-doneplugin dplugin-mobile-dinput"
              >
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
                >
                  {{ personalInfo.name }}
                </span>
              </div>
            </div>
            <!---->
          </div>
        </div>
        <!----><!---->
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
            <!---->
          </div>
          <!---->
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
                  <!---->
                  <img
                    :src="personalInfo.img"
                    style="height: 100px; width: 100px"
                    alt="photo"
                  />
                </div>
                <!---->
                <div class="clear"></div>
              </div>
              <!---->
              <!---->
            </div>
            <!---->
          </div>
        </div>
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
            <!---->
          </div>
          <!---->
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
              <!---->
              <!---->
            </div>
            <!---->
          </div>
        </div>
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
            <!---->
          </div>
          <!---->
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
            <!---->
          </div>
        </div>
        <div class="mobile_pluginnames_hide">
          <div
            class="pluginnames"
            style="min-height: 0.1rem; padding: 0 15px"
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
              <span
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
                >{{ personalInfo.inOut }}</span
              >
            </div>
          </div>
        </div>
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
            <!---->
          </div>
          <!---->
          <div class="plugin-allbox">
            <div
              data-key="User_5"
              class="dplugin-box"
              style="margin-top: 0px; margin-bottom: 0px; text-align: center"
            >
              <div
                class="dplugin-mobile dplugin-doneplugin dplugin-mobile-dinput"
              >
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
                >
                  {{ personalInfo.stdId }}
                </span>
              </div>
            </div>
            <!---->
          </div>
        </div>
        <!---->
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
            <!---->
          </div>
          <!---->
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
            <!---->
          </div>
        </div>
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
            <!---->
          </div>
          <!---->
          <div class="plugin-allbox">
            <div
              data-key="User_22"
              class="dplugin-box"
              style="margin-top: 0px; margin-bottom: 0px; text-align: center"
            >
              <div
                class="dplugin-mobile dplugin-doneplugin dplugin-mobile-dinput"
              >
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
                >
                  {{ personalInfo.dep }}
                </span>
              </div>
            </div>
            <!---->
          </div>
        </div>
        <!----><!----><!----><!----><!----><!---->
        <div style="display: none">
          <ul>
            <!----><!----><!----><!----><!----><!----><!----><!----><!----><!----><!----><!----><!---->
            <li>
              <span>动态转化：</span>
              <div
                data-key="Conversion_17"
                class="dplugin-box"
                style="margin-top: 0px; margin-bottom: 0px; text-align: left"
              >
                <!---->
              </div>
            </li>
            <!----><!----><!---->
            <li>
              <span>数据源：</span>
              <div
                data-key="DataSource_23"
                class="dplugin-box"
                plugin="[object Object]"
                style="margin-top: 0px; margin-bottom: 0px; text-align: left"
              >
                <div>
                  <div class="el-dialog__wrapper" style="display: none">
                    <div
                      role="dialog"
                      aria-modal="true"
                      aria-label="选择数据"
                      class="el-dialog el-dialog--center rTbaleDialog"
                      style="margin-top: 15vh; width: 90%"
                    >
                      <div class="el-dialog__header">
                        <span class="el-dialog__title">选择数据</span
                        ><!---->
                      </div>
                      <!---->
                      <div class="el-dialog__footer">
                        <span class="dialog-footer"
                          ><button
                            type="button"
                            class="
                              el-button el-button--default el-button--small
                            "
                          >
                            <!---->
                            <!----><span>取 消</span>
                          </button>
                          <button
                            type="button"
                            class="
                              el-button el-button--primary el-button--small
                            "
                          >
                            <!---->
                            <!----><span>确 定</span>
                          </button></span
                        >
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </li>
            <li>
              <span>验证信息：</span>
              <div
                data-key="Validate_24"
                class="dplugin-box"
                style="margin-top: 0px; margin-bottom: 0px; text-align: left"
              >
                <!---->
              </div>
            </li>
            <li>
              <span>提示：</span>
              <div
                data-key="Alert_25"
                class="dplugin-box"
                plugin="[object Object]"
                style="margin-top: 0px; margin-bottom: 0px; text-align: left"
              >
                <!---->
                <div class="el-dialog__wrapper" style="display: none">
                  <div
                    role="dialog"
                    aria-modal="true"
                    aria-label="禁止扫码"
                    class="el-dialog sele_leave"
                    style="margin-top: 15vh; width: 310px"
                  >
                    <div class="el-dialog__header">
                      <span class="el-dialog__title">禁止扫码</span
                      ><!---->
                    </div>
                    <!----><!---->
                  </div>
                </div>
              </div>
            </li>
            <li>
              <span>提示：</span>
              <div
                data-key="Alert_26"
                class="dplugin-box"
                plugin="[object Object]"
                style="margin-top: 0px; margin-bottom: 0px; text-align: left"
              >
                <!---->
                <div class="el-dialog__wrapper" style="display: none">
                  <div
                    role="dialog"
                    aria-modal="true"
                    aria-label="禁止扫码"
                    class="el-dialog sele_leave"
                    style="margin-top: 15vh; width: 310px"
                  >
                    <div class="el-dialog__header">
                      <span class="el-dialog__title">禁止扫码</span
                      ><!---->
                    </div>
                    <!----><!---->
                  </div>
                </div>
              </div>
            </li>
            <!----><!----><!----><!----><!---->
          </ul>
        </div>
        <div class="el-loading-mask area-vloading" style="display: none">
          <div class="el-loading-spinner">
            <svg viewBox="25 25 50 50" class="circular">
              <circle
                cx="50"
                cy="50"
                r="20"
                fill="none"
                class="path"
              ></circle></svg
            ><!---->
          </div>
        </div>
      </div>
      <!---->
    </div>
    <div class="wxformbtn m_start_btn" @click="changeInOut(this.personalInfo)">
      <button class="draftdiv active">更多</button>
      <div class="wxformbtn_center"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "fakePass",
  props: ["personalInfo"],
  methods: {
    changeInOut(personalInfo) {
      localStorage.setItem("inOut", personalInfo.inOut);
      personalInfo.inOut =
        personalInfo.inOut === "允许出校" ? "允许入校" : "允许出校";
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

<style>
/* @font-face {
  font-family: iconfont;
  src: url(data:font/woff2;base64,d09GMgABAAAAAAOoAAsAAAAACHwAAANcAAEAAAAAAAAAAAAAAAAAAAAAAAAAAAAAHFQGYACDBgqEQIN9ATYCJAMMCwgABCAFhGcHSxtuB8iemjyKBSgLazJBBJjABQ+e/8+r7sv/SSFpmKuRVxJ3nRoAZy+guns5gjbm8hEkqdgHlK9oQAptMS0nvTQjNSFJmCk7ZMItskeW0aP6f46ZLork2xJsitlBZbP5nu8NLPMyCe+dH5CfwvDqoHfqJQjgp1wjRotWd4+F3ugBSoUxjTUokObK6BG+VWiIanRLruBFsNC9GlmGCcZ8IwgsDX9eXlMZLxiYCutW7f/cLfw/s55lKfe/C3UHd7oGOt8ATEABxRvTSt92c3flOFxM4a8TV5hUC41gTOr7/5+QrUutLf/jGSAWVrYDQD6NGPDMcokQeJYVwQCu/xBYQDioBR4w2OgdJrYTHe444vh83nDrs4Z1F24LbPU7Cza7W4aFLgieRrtnqu2whbXnxAycrenjHveHLjiZCk9VmE/QGRLbA9q7s85eIoHYiLjTLEmycTcv2CrSLcJ2MXT176dIIdgbNuAe77lgFbirbXvh2qroGv90/8Y25jL9WU/pJ/RKGFqWVlXoZiZmhviJb04t67cgy7NPVmTFI5NPJXYZ713zX2O3O9s3t/7cZ9iUlh9GCxkNph+6YEZY0+G9zOTM0OFPq5qxgscxpzx9zNXt7qTvSr+TsevBtXBi0DK76l1mF3OXHuIWDdXhK6N3fQhWsyjiuDksWNNM0F25YcTx7PpwrIXBCkOh1q0W+rMWqoBqSuG/2q6Kf/7fMGhfLfv1G3z12hqAu70ObQld/zW4Fu9bMQv8aklvsKvWPaB0HdtdggCKudjvUInf1sC/zQeIdG+4NAoOguDNcQQw8JAECi+ZSI0tBBObSrDw0hD8FGl52CbKeGVE+4BcMwkI4baAQShHQBHuElJjr4NJrOdgEe4v+OmakPNscjOouaCl6IL9AaHD5DkyDce9R/8lsaQq8IySh9QHm9LyYuwSCWWMDfmrv1X1wBNO4YK/HSYJQyYcoaPLQDXbrcqG1n3L0uG0cCKQRSEXGOgDGMHBiOd31/zvu4d8LxIWAZHPRpGzLGZ8UKFUOYC8FBPUciOXTPLKtzWZ8oChhERToJVoRIkWZmB8/awIcqil4QOCmZ0yu9tQVLxcXpq+3CHAj/UgJYYo0XgGjrDYtWjwdJ0HGIVGiuRPpfdQmfzFpg4A)
      format("woff2"),
    url(data:font/woff;base64,d09GRgABAAAAAAVEAAsAAAAACHwAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAADsAAABUIIslek9TLzIAAAFEAAAARAAAAGA8G0jzY21hcAAAAYgAAABUAAABhmTh0NpnbHlmAAAB3AAAAWkAAAJAtXqYDGhlYWQAAANIAAAALwAAADYd1rNlaGhlYQAAA3gAAAAcAAAAJAfeA4RobXR4AAADlAAAAAwAAAAMDAAAAGxvY2EAAAOgAAAACAAAAAgAbAEgbWF4cAAAA6gAAAAfAAAAIAEYAJNuYW1lAAADyAAAAUAAAAJnEKM8sHBvc3QAAAUIAAAAOgAAAEs6ovv2eJxjYGRgYOBiMGCwY2BycfMJYeDLSSzJY5BiYGGAAJA8MpsxJzM9kYEDxgPKsYBpDiBmg4gCACY7BUgAeJxjYGFhYJzAwMrAwNTJdIaBgaEfQjO+ZjBi5ACKMrAyM2AFAWmuKQwHnrE9U2Zu+N/AwMB8hwFIMjCiKGICAGbyDIl4nO2QsRGAMAwD3w644NgiDQUDUTF+1giKA1ugu7fOsisBK1DEKRawG2PoUmqZF7bMl/wJueEtWu0dPpdMt0h3jeDXnvN4Nx9tTUazrU7wB+QODep4nH1Qy07CQBS9l8KwQEjItCVpBDptMm5oDaXURKIpLHTl1rUrw8ql67rxO/wAkv4CezWu/APjStdqIsXbKRLFxMnkzJlzzr3zgArQ0K60MdSgC7swgmMAFEEUSlc4TDdROA00mnoHByI4xGEz9JHrjExJPCLRNKoqOVBV2g+ONkKd8/oyR3xdzN19l2YpVmtbWou5JaVVii15kyV5EnM8yeaKx3lVwi1OE/PaXw0W8XettOIilK3C9KQawPJRm2k94ltgQAckRHAEp3AOl3ANwIf9kG5p9HV6yt7A0JkjD3BNWgUZ7riMdmE0wg62UWeaw2gxRxhEJEsXXR8LPzDbaP7rt4y/9R8C72w7CwWO+TZ/ntDtnybELmbC90Xa9fz7CmOVtFytlrO31PY8O7V76D0oNYdSnYTepopngoY9bXDemCbqb5NE7W4xb+FhTyG1TVcHfL4Ujrc2ygVk70XY624YAF+1emWGAAAAeJxjYGRgYADiYod+13h+m68M3CwMIHA3evtKBP3/KgsDsyOQy8HABBIFACbDCo4AeJxjYGRgYG7438AQw8IAAkCSkQEVMAMARwkCbAQAAAAEAAAABAAAAAAAAAAAbAEgeJxjYGRgYGBmaGfgZgABJiDmAkIGhv9gPgMAFscBrAB4nIWRPW7CQBCFn8GQBJQoSqQ0aVYpKBLJ/JRIqVCgp6AHs+ZHttdaL0jUOU2OkBPkCOloc4pIedhDA0W82tlv3r6ZHckA7rCHh/K75y7ZwyWzkiu4wKNwlfqTsE9+Fq6hiZ5wnfqrcAMveBNusmPGDp5/xayFd2EPt/gQruAGn8JV6l/CPvlbuIYH/AjXqf8KNzDxroWbaHnhwOqp03M126lVaNLIpO54jvViE0/tqTzRNl+ZVHWDzlEa6VTbY5t8u+g5F6nImkQNeavj2KjMmrUOXbB0Luu325HoQWgSDGChMYVjnENhhh3jCiEMUkRFdGf5mO4FNohZaf91T+i2yKkfcoUuAnTOXCO60sJ5Ok2OLV/rUXV0K27LmoQ0lFrNSWKy4g883K2phNQDLIuqDH20uaITf1DMkPwB2JNvV3icY2BigAAuBuyAmZGJkZmRhYE9KTMxPyUxTzzUszgjNSszPjc1LyszryKzJD8vXdfQgoEBANtMC8gAAA==)
      format("woff"),
    url(data:font/ttf;base64,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)
      format("truetype");
} */
.iconfont {
  font-family: iconfont !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.iconcolor1 {
  color: #346df1;
}
* {
  font-family: PingFangSC-Regular, Arial, Microsoft YaHei;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html {
  -webkit-text-size-adjust: 100%;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-size: 111.2px;
}
body,
html {
  width: 100%;
  height: 100%;
}
body {
  text-align: left;
  background-color: #f2f2f2;
  overflow-x: hidden;
  line-height: 0.2rem;
  font-size: 0.14rem;
  color: #333;
}
.forms {
  padding-bottom: 0.7rem;
  border-top: 0.1rem solid #ededed;
}
.forms .toptabla {
  width: 100%;
  height: 100%;
  border-radius: 1px;
  box-sizing: border-box;
  margin-bottom: 0.1rem;
}
.forms .toptabla .toptabla_con {
  height: 100%;
  padding: 10px;
  background: #fff;
  justify-content: space-between;
}
.forms .toptabla .toptabla_con,
.forms .toptabla .toptabla_con .formsTop_left {
  display: flex;
  align-items: center;
}
.forms .toptabla .toptabla_con .formsTop_left > p {
  font-size: 12px;
  font-family: PingFang SC;
  font-weight: 700;
  color: #333;
  margin-left: 5px;
}
.forms .toptabla .toptabla_con .toptabla_img {
  width: 9px;
  height: 5px;
}
.formList {
  background-color: #fff;
}
.pluginnames {
  width: 100%;
  min-height: 42px;
  line-height: 22px;
  padding: 10px 15px;
  font-size: 14px;
  background-color: rgba(47, 99, 164, 0.05);
}
.plugin-allbox {
  width: 100%;
  height: 100%;
  position: relative;
}
.dplugin-box {
  background-color: #fff;
  padding: 13px 15px;
}
.forms .wxformbtn {
  width: 100%;
  height: 0.6rem;
  position: fixed;
  left: 0;
  bottom: 0;
  background: #fff;
  z-index: 2;
  display: flex;
}
.forms .wxformbtn button.active {
  border: 0.01rem solid #4285f4;
  background: #fff;
  color: #4285f4;
}
.forms .wxformbtn button {
  width: calc(33% - 0.15rem);
  height: 0.4rem;
  margin: 0.1rem 0.08rem 0 0.08rem;
  color: #fff;
  background: #4285f4;
  border: 0;
  border-radius: 0.1rem;
  font-size: 0.15rem;
  flex: 1;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.m_start_btn button {
  border-radius: 0.2rem !important;
  margin: 0.1rem 0.05rem 0 0.05rem !important;
}
.m_start_btn .wxformbtn_center {
  display: flex;
  flex: 4;
}
.glass[data-v-fe143b6a] {
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  box-shadow: 4px 4px 30px 0 rgba(27, 0, 37, 0.4);
}
div.backgroundDiv[data-v-fe143b6a] {
  width: 100%;
  height: 100vh;
  color: #fff;
  background: linear-gradient(135deg, #75f0db, #75dbf0, #8a75f0, #f075c7);
  background-size: 200% 200%;
  -webkit-animation: gradient-move-fe143b6a 10s ease infinite alternate;
  animation: gradient-move-fe143b6a 10s ease infinite alternate;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
@-webkit-keyframes gradient-move-fe143b6a {
  0% {
    background-position: 0 0;
  }
  to {
    background-position: 100% 100%;
  }
}
@keyframes gradient-move-fe143b6a {
  0% {
    background-position: 0 0;
  }
  to {
    background-position: 100% 100%;
  }
}
div.backgroundDiv div.piContainer[data-v-fe143b6a] {
  width: 280px;
  height: 350px;
  border-radius: 30px;
  display: flex;
  background-color: rgba(0, 0, 0, 0.4);
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}
div.backgroundDiv div.piContainer div.chooseAPhoto[data-v-fe143b6a] {
  width: 80%;
  background-color: rgba(0, 0, 0, 0.2);
  padding: 10px;
  border-radius: 15px;
  align-items: center;
  text-align: center;
  font-weight: 700;
}
div.backgroundDiv div.piContainer div.inputBlock[data-v-fe143b6a] {
  width: 80%;
  background-color: rgba(0, 0, 0, 0.2);
  padding: 3px;
  border-radius: 15px;
  display: flex;
  align-items: center;
}
div.backgroundDiv div.piContainer div.inputBlock span[data-v-fe143b6a] {
  margin-right: 10px;
  border-radius: 15px;
  font-weight: 700;
  letter-spacing: 1px;
  padding: 7px;
  background-color: rgba(0, 0, 0, 0.2);
}
div.backgroundDiv div.piContainer div.inputBlock input[data-v-fe143b6a] {
  letter-spacing: 1px;
  outline: none;
  border: 0;
  color: #fff;
  background-color: transparent;
}
div.backgroundDiv div.piContainer select[data-v-fe143b6a] {
  width: 80%;
  text-align: center;
  background-color: rgba(0, 0, 0, 0.2);
  outline: none;
  border: 0;
  font-size: 16px;
  font-weight: 700;
  color: #fff;
  padding: 9px 10px;
  border-radius: 15px;
}
div.backgroundDiv div.button[data-v-fe143b6a] {
  width: 280px;
  margin-top: 20px;
  padding: 20px 0;
  font-size: 25px;
  font-weight: 700;
  text-align: center;
  letter-spacing: 5px;
  border-radius: 30px;
  background-color: rgba(0, 0, 0, 0.4);
  transition: background-color 0.5s ease-out;
}
div.backgroundDiv div.button[data-v-fe143b6a]:active {
  background-color: rgba(0, 0, 0, 0.7);
}
</style>
