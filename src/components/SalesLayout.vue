<template>
  <table
    cellpadding="0"
    cellspacing="0"
    border="0"
    style="
      margin: 0px;
      border-collapse: collapse;
      font-family: Arial, sans-serif;
      font-size: 13px;
      line-height: 14px;
    "
  >
    <tr>
      <td style="padding: 0px 1px 0px 0px">
        <table
          cellpadding="0"
          cellspacing="0"
          border="0"
          style="margin: 0px; border-collapse: collapse"
        >
          <tr>
            <td
              align="center"
              style="padding: 0px 12px 0px 0px; vertical-align: top"
            >
              <table
                cellpadding="0"
                cellspacing="0"
                border="0"
                style="margin: 0px; border-collapse: collapse"
              >
                <tr>
                  <td style="padding: 0px 1px 10px 0px">
                    <p style="margin: 1px">
                      <img
                        :src="
                          props.state.profileUrl ||
                          'https://tomwatts.s3.ap-southeast-2.amazonaws.com/profile+1.png'
                        "
                        alt=""
                        :title="props.state.name || 'Tom Watts'"
                        width="100"
                        height="100"
                        class=""
                        style="display: block; border: 0px; max-width: 100px"
                      />
                    </p>
                  </td>
                </tr>
              </table>
              <table
                cellpadding="0"
                cellspacing="0"
                border="0"
                style="margin: 0px; border-collapse: collapse"
              >
                <tr>
                  <td style="padding: 0px 1px 0px 0px">
                    <p style="margin: 1px">
                      <a href="https://tomwatts.dev/" target="_blank"
                        ><img
                          src="https://tomwatts.s3.ap-southeast-2.amazonaws.com/logotype.png"
                          alt=""
                          title="Tom Watts"
                          width="150"
                          height="37"
                          style="display: block; border: 0px; max-width: 150px"
                      /></a>
                    </p>
                  </td>
                </tr>
              </table>
            </td>
            <td width="5" style="padding: 1px 0px 0px"></td>
            <td style="padding: 0px 1px 0px 0px; vertical-align: top">
              <table
                cellpadding="0"
                cellspacing="0"
                border="0"
                style="margin: 0px; border-collapse: collapse; font-size: 12px"
              >
                <tr style="vertical-align: middle" height="21">
                  <td style="padding: 0px">
                    <span
                      style="
                        font-family: Arial, sans-serif;
                        color: #212121;
                        font-size: 15px;
                        font-weight: bold;
                        line-height: 21px;
                        white-space: nowrap;
                        margin: 0;
                      "
                      >{{ props.state.name || "Tom Watts" }}</span
                    >
                  </td>
                </tr>

                <tr style="vertical-align: middle" height="20">
                  <td style="padding: 0px">
                    <span
                      style="
                        font-family: Arial, sans-serif;
                        color: #767676;
                        font-size: 13px;
                        font-weight: 400;
                        line-height: 20px;
                        white-space: nowrap;
                        margin: 0;
                      "
                      >{{
                        props.state.jobTitle ||
                        "Assistant to the Regional Manager"
                      }}</span
                    >
                  </td>
                </tr>

                <tr style="vertical-align: middle" height="18">
                  <td style="padding: 0px">
                    <span
                      style="
                        font-family: Arial, sans-serif;
                        color: #545454;
                        font-size: 13px;
                        font-weight: 400;
                        line-height: 18px;
                        white-space: nowrap;
                        margin: 0;
                      "
                      >{{ props.state.location || "Perth Australia" }}</span
                    >
                  </td>
                </tr>

                <tr>
                  <td>
                    <table
                      cellpadding="0"
                      cellspacing="0"
                      style="
                        vertical-align: -webkit-baseline-middle;
                        width: 100%;
                      "
                    >
                      <tbody>
                        <tr>
                          <td
                            height="8"
                            style="
                              font-size: 8px;
                              height: 8px;
                              line-height: 8px;
                            "
                          >
                            &nbsp;
                          </td>
                        </tr>
                      </tbody>
                    </table>
                    <table
                      cellpadding="0"
                      cellspacing="0"
                      style="
                        vertical-align: -webkit-baseline-middle;
                        width: 100%;
                      "
                    >
                      <tbody>
                        <tr
                          height="12"
                          style="vertical-align: middle; height: 12px"
                        >
                          <td
                            color="#00AEEF"
                            direction="horizontal"
                            height="2"
                            style="
                              width: 320px;
                              border-bottom-width: 2px;
                              border-bottom-style: solid;
                              border-bottom-color: #17e9d9;
                              font-size: 12px;
                              border-left-style: none;
                              display: block;
                            "
                          ></td>
                        </tr>
                      </tbody>
                    </table>
                  </td>
                </tr>

                <tr>
                  <td>
                    <table
                      cellpadding="0"
                      cellspacing="0"
                      border="0"
                      style="margin: 0px; border-collapse: collapse"
                    >
                      <tr>
                        <td
                          style="
                            font-family: Arial, sans-serif;
                            font-size: 13px;
                            font-weight: 400;
                            line-height: 18px;
                            white-space: nowrap;
                            color: #545454 !important;
                            padding: 0px 1px 0px 0px;
                          "
                        >
                          <p style="margin: 1px">
                            <a
                              :href="`tel:${formattedPhone}`"
                              target="_blank"
                              style="
                                font-family: Arial, sans-serif;
                                font-size: 13px;
                                font-weight: 400;
                                line-height: 18px;
                                white-space: nowrap;
                                color: #545454;
                              "
                              ><span
                                style="
                                  font-family: Arial, sans-serif;
                                  font-size: 13px;
                                  font-weight: 400;
                                  line-height: 18px;
                                  white-space: nowrap;
                                  color: #545454;
                                "
                                >{{
                                  props.state.phone || "+61 412 345 678"
                                }}</span
                              ></a
                            >
                          </p>
                        </td>
                      </tr>

                      <tr>
                        <td
                          style="
                            font-family: Arial, sans-serif;
                            font-size: 13px;
                            font-weight: 400;
                            line-height: 18px;
                            white-space: nowrap;
                            color: #545454 !important;
                            padding: 0px 1px 0px 0px;
                          "
                        >
                          <p style="margin: 1px">
                            <a
                              :href="`mailto:${props.state.email}`"
                              target="_blank"
                              style="
                                font-family: Arial, sans-serif;
                                font-size: 13px;
                                font-weight: 400;
                                line-height: 18px;
                                white-space: nowrap;
                                color: #545454;
                              "
                              ><span
                                style="
                                  font-family: Arial, sans-serif;
                                  font-size: 13px;
                                  font-weight: 400;
                                  line-height: 18px;
                                  white-space: nowrap;
                                  color: #545454;
                                "
                                >{{
                                  props.state.email || "hello@companyemail.com"
                                }}</span
                              ></a
                            >
                          </p>
                        </td>
                      </tr>
                    </table>
                  </td>
                </tr>
                <tr>
                  <td style="padding: 0px 1px 0px 0px">
                    <table
                      cellpadding="0"
                      cellspacing="0"
                      border="0"
                      style="margin: 0px; border-collapse: collapse"
                    >
                      <tr style="vertical-align: middle" height="24">
                        <td style="padding: 0px" width="320">
                          <span
                            color="#767676"
                            style="font-family: Arial, sans-serif"
                          >
                            <a
                              href="https://tomwatts.dev/"
                              target="_blank"
                              color="#767676"
                              style="
                                font-family: Arial, sans-serif;
                                text-decoration: none !important;
                                color: #767676 !important;
                                font-weight: 700;
                                font-size: 13px;
                                line-height: 14px;
                              "
                            >
                              tomwatts.dev </a
                            ><span
                              style="
                                color: #8e8e8e !important;
                                font-weight: 300;
                              "
                              >&nbsp;|&nbsp;</span
                            >
                          </span>
                          <span
                            color="#767676"
                            style="font-family: Arial, sans-serif"
                          >
                            <a
                              href="https://www.facebook.com/"
                              target="_blank"
                              color="#767676"
                              style="
                                font-family: Arial, sans-serif;
                                text-decoration: none !important;
                                color: #767676 !important;
                                font-weight: 400;
                                font-size: 13px;
                                line-height: 24px;
                              "
                            >
                              Facebook </a
                            ><span
                              style="
                                color: #8e8e8e !important;
                                font-weight: 300;
                              "
                              >&nbsp;|&nbsp;</span
                            >
                          </span>
                          <span
                            color="#767676"
                            style="font-family: Arial, sans-serif"
                          >
                            <a
                              href="https://www.linkedin.com/in/tom-watts-perth/"
                              target="_blank"
                              color="#767676"
                              style="
                                font-family: Arial, sans-serif;
                                text-decoration: none !important;
                                color: #767676 !important;
                                font-weight: 400;
                                font-size: 13px;
                                line-height: 24px;
                              "
                            >
                              LinkedIn </a
                            ><span
                              style="
                                color: #8e8e8e !important;
                                font-weight: 300;
                              "
                              >&nbsp;|&nbsp;</span
                            >
                          </span>
                          <span
                            color="#767676"
                            style="font-family: Arial, sans-serif"
                          >
                            <a
                              href="https://www.instagram.com/"
                              target="_blank"
                              color="#767676"
                              style="
                                font-family: Arial, sans-serif;
                                text-decoration: none !important;
                                color: #767676 !important;
                                font-weight: 400;
                                font-size: 13px;
                                line-height: 24px;
                              "
                              >Instagram</a
                            >
                          </span>
                        </td>
                      </tr>
                    </table>
                  </td>
                </tr>
              </table>
            </td>
          </tr>
        </table>
      </td>
    </tr>

    <tr v-if="!!props.state.infoLink">
      <td style="padding: 4px 1px 0px 0px">
        <table
          cellpadding="0"
          cellspacing="0"
          border="0"
          style="max-width: 400px; margin: 0px; border-collapse: collapse"
        >
          <tr>
            <td
              style="
                font-family: Arial, sans-serif;
                font-size: 12px;
                line-height: 13px;
                color: #0064b3 !important;
              "
            >
              <p
                style="
                  font-family: Arial, sans-serif;
                  font-size: 12px;
                  line-height: 13px;
                  color: #0064b3 !important;
                  margin: 1px;
                "
              >
                <a
                  :href="props.state.infoLink"
                  target="_blank"
                  color="#0064b3"
                  style="
                    font-family: Arial, sans-serif;
                    text-decoration: none !important;
                    color: #0064b3 !important;
                    font-weight: 500;
                    font-size: 13px;
                    line-height: 24px;
                  "
                >
                  {{ props.state.infoLink }}
                </a>
              </p>
            </td>
          </tr>
        </table>
      </td>
    </tr>

    <tr v-if="!!props.state.note">
      <td style="padding: 4px 1px 0px 0px">
        <table
          cellpadding="0"
          cellspacing="0"
          border="0"
          style="max-width: 400px; margin: 0px; border-collapse: collapse"
        >
          <tr>
            <td
              style="
                font-family: Arial, sans-serif;
                font-size: 12px;
                line-height: 13px;
                color: #747474 !important;
              "
            >
              <p
                style="
                  font-family: Arial, sans-serif;
                  font-size: 12px;
                  line-height: 13px;
                  color: #747474 !important;
                  margin: 1px;
                "
              >
                {{ props.state.note }}
              </p>
            </td>
          </tr>
        </table>
      </td>
    </tr>
  </table>
</template>

<script setup>
import { defineProps, computed } from "vue";

const props = defineProps({
  state: Object,
});

const formattedPhone = computed(() => {
  if (!props.state.phone) return "";
  return props.state.phone.replace(/\s/g, "");
});
</script>
