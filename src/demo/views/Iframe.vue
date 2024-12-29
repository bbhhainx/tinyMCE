<template>
  <div>
    <h2>IFrame Editor</h2>
    <editor
      :api-key="apiKey"
      :initialValue="content"
      :plugins="'code preview quickbars table image link lists media autoresize help advlist emoticons searchreplace visualchars visualblocks fullscreen accordion anchor advtemplate codesample charmap tableofcontents insertdatetime wordcount'"
      :toolbar="'undo redo | blocks | fontsize | fontfamily |bold italic strikethrough forecolor backcolor | image | alignleft aligncenter alignright alignjustify | bullist numlist indent outdent | removeformat | code emoticons preview'"
    />
  </div>
</template>

<script lang="ts" setup>
import Editor from "/@/main/ts/index.ts";
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
</script>
