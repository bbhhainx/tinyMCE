<template>
  <div>
    <editor v-model="content" api-key="apiKey"></editor>
  </div>
</template>

<script>
import Editor from "/@/main/ts/index";

const apiKey = "qagffr3pkuv17a8on1afax661irst1hbr4e6tbv888sz91jc";
const content = `
<table class="table table-bprintLabeled" style="width: 100%;" border="1" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td>{PAGE_NAME}<br />http://facebook.com/{PAGE_USERNAME}</td>
<td>Đơn h&agrave;ng <strong>#{ORDER_ID}</strong><br />Ng&agrave;y tạo:&nbsp;{ORDER_CREATED_DAY}</td>
</tr>
<tr>
<td colspan="2">Người nhận: <strong>{SHIPPING_NAME}</strong><br />
<div style="width: 100%;">
<div style="margin-left: 80px;">
<p style="margin: 0px 0px 0px 0px;">{SHIPPING_ADDRESS}</p>
</div>
</div>
<div style="margin-left: 80px;">{SHIPPING_PHONE}</div>
</td>
</tr>
<tr>
<td colspan="2">{FULL_PRODUCTS}</td>
</tr>
<tr>
<td>{NOTE}</td>
<td>Thu hộ (COD): {TOTAL_COD}</td>
</tr>
</tbody>
</table>`;

export default {
  name: "EditorTab",
  components: {
    editor: Editor
  },
  data() {
    return {
      apiKey,
      content
    };
  }
};
</script>
