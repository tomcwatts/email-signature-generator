<template>
  <table
    width="auto"
    cellspacing="0"
    cellpadding="0"
    border="0"
    style="
      margin: 0px;
      border-collapse: collapse
      font-family: Arial, sans-serif;
      font-size: 13px;
      line-height: 14px;
    "
  >
    <tbody>
      <tr>
        <td
          width="100"
          height="100"
          style="width: 100px; max-width: 100px; vertical-align: top"
        >
          <a href="https://tomwatts.dev/" style="display: block; width: 100px">
            <img
              width="100"
              height="100"
              style="
                width: 100px;
                min-width: 100px;
                max-width: 100px;
                height: 100px;
                min-height: 100px;
                border: none;
              "
              src="https://tomwatts.s3.ap-southeast-2.amazonaws.com/logo.png"
          /></a>
        </td>
        <td
          width="18"
          style="
            width: 18px;
            min-width: 18px;
            max-width: 18px;
            border: none;
          "
        ></td>
        <td
          style="
            vertical-align: top;
            text-align: left;
            text-align: left;
          "
        >
          <table
            cellpadding="0"
            cellspacing="0"
            style="
              vertical-align: -webkit-baseline-middle;
              text-decoration: none;
              color: #8c8c8c !important;
              font-size: 12px;
            "
            color="#8C8C8C"
          >
            <tbody>
              <tr style="vertical-align: middle" height="22">
                <td style="padding: 0px">
                  <span
                    style="
                      font-family: Arial, sans-serif;
                      color: #212121;
                      font-size: 15px;
                      line-height: 22px;
                      font-weight: bold;
                    "
                    >{{ props.state.name || "Tom Watts" }}</span
                  >
                </td>
              </tr>

              <tr style="vertical-align: middle" height="19">
                <td style="padding: 0px">
                  <span
                    style="
                      font-family: Arial, sans-serif;
                      color: #767676;
                      font-weight: 500;
                      font-size: 13px;
                      line-height: 18px;
                    "
                    >{{ props.state.jobTitle || "Assistant to the Regional Manager" }}</span
                  >
                </td>
              </tr>

              <tr style="vertical-align: middle" height="19">
                <td style="padding: 0px">
                  <span
                    style="
                      font-family: Arial, sans-serif;
                      color: #545454;
                      font-size: 13px;
                      line-height: 19px;
                      font-weight: 400;
                    "
                    >{{ props.state.location || "Perth, Australia" }}</span
                  >
                </td>
              </tr>

              <table
                cellpadding="0"
                cellspacing="0"
                style="vertical-align: -webkit-baseline-middle; width: 100%"
              >
                <tbody>
                  <tr>
                    <td
                      height="6"
                      style="font-size: 6px; height: 6px; line-height: 6px"
                    >
                      &nbsp;
                    </td>
                  </tr>
                </tbody>
              </table>

              <table
                cellpadding="0"
                cellspacing="0"
                style="vertical-align: -webkit-baseline-middle; width: 100%"
              >
                <tbody>
                  <tr height="10" style="vertical-align: middle; height: 10px">
                    <td
                      color="#00AEEF"
                      direction="horizontal"
                      height="2"
                      style="
                        width: 300px;
                        border-bottom-width: 2px;
                        border-bottom-style: solid;
                        border-bottom-color: #17e9d9;
                        font-size: 10px;
                        line-height: 10px;
                        border-left-style: none;
                        display: block;
                      "
                    ></td>
                  </tr>
                </tbody>
              </table>

              <table
                cellpadding="0"
                cellspacing="0"
                style="
                  vertical-align: -webkit-baseline-middle;
                  text-decoration: none;
                  font-size: 14px;
                  line-height: 14px;
                "
              >
                <tbody>
                  <tr
                    v-if="props.state.phone"
                    style="vertical-align: middle"
                    height="22"
                  >
                    <td style="padding: 0px" width="300">
                      <a
                        :href="`tel:${formattedPhone}`"
                        color="#545454"
                        style="
                          font-family: Arial, sans-serif;
                          color: #545454 !important;
                          font-size: 13px;
                          line-height: 14px;
                          font-weight: 500 !important;
                        "
                        >{{ props.state.phone || "0412 345 678" }}</a
                      >
                    </td>
                  </tr>

                  <tr
                    v-if="props.state.email"
                    style="vertical-align: middle"
                    height="22"
                  >
                    <td style="padding: 0px" width="300">
                      <a
                        :href="`mailto:${props.state.email}`"
                        color="#545454"
                        style="
                          font-family: Arial, sans-serif;
                          color: #545454 !important;
                          font-size: 13px;
                          line-height: 14px;
                          font-weight: 400 !important;
                        "
                        >{{ props.state.email }}</a
                      >
                    </td>
                  </tr>

                  <tr style="vertical-align: middle" height="22">
                    <td style="padding: 0px" width="300">
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
                          style="color: #8e8e8e !important; font-weight: 300"
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
                            line-height: 14px;
                          "
                        >
                          Facebook </a
                        ><span
                          style="color: #8e8e8e !important; font-weight: 300"
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
                            line-height: 14px;
                          "
                        >
                          LinkedIn </a
                        ><span
                          style="color: #8e8e8e !important; font-weight: 300"
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
                            line-height: 14px;
                          "
                          >Instagram</a
                        >
                      </span>
                    </td>
                  </tr>
                </tbody>
              </table>
            </tbody>
          </table>
        </td>
      </tr>

      <tr v-if="props.state.note" style="vertical-align: middle" height="48">
        <td colspan="3">
          <table
            cellpadding="0"
            cellspacing="0"
            style="vertical-align: -webkit-baseline-middle; width: 100%"
          >
            <tbody>
              <tr>
                <td height="4px" style="font-size: 4px; line-height: 4px">
                  &nbsp;
                </td>
              </tr>
            </tbody>
          </table>

          <table
            cellpadding="0"
            cellspacing="0"
            border="0"
            style="max-width: 400px; margin: 0px; border-collapse: collapse"
          >
            <tr>
              <td
                style="
                  padding: 4px 1px 0px 0px;
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
    </tbody>
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
