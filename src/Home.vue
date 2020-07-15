<template>
  <div id="app">
    <h1>{{msg}}</h1>
    <div id="adobe-dc-view"></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      msg: "CPIMA"
    };
  },
  created() {
    
    let ckeditor = document.createElement("script");
    ckeditor.setAttribute("src", "//documentcloud.adobe.com/view-sdk/main.js");
    document.head.appendChild(ckeditor);
    document.addEventListener("adobe_dc_view_sdk.ready", function() {
      var adobeDCView = new AdobeDC.View({
        clientId: "790af3f947c1460881d99bf4110ab2e2",
        divId: "adobe-dc-view"
      });
      adobeDCView.previewFile(
        {
          content: {
            location: {
              url:
                "src/assets/State of Hawaii Guide.pdf"
            }
          },
          metaData: { fileName: "State of Hawaii Guide.pdf" }
        },
        {}
      );
    });
  }
};
</script>

<style>
</style>