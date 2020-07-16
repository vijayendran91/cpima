<template>
  <div id="app" style="background-color:'#ffffcc';">
    <title>{{msg}}</title>
    <div>
      <b-navbar toggleable="lg" type="dark" variant="warning">
        <b-container style="margin-left: 0px;margin-right: 0px;">
            <b-navbar-brand href="/" style="font-size:30px;">
                <img src="src/assets/State_of_Hawaii.svg.png"  style="width:10%;">
                State Of Hawaii
            </b-navbar-brand>
            <b-nav-item-dropdown class="navbar-dropdown" toggle-class="text-white" text="Lang" right>
                <b-dropdown-item href="#">Account</b-dropdown-item>
                <b-dropdown-item href="#">Settings</b-dropdown-item>
            </b-nav-item-dropdown>
        </b-container>
      </b-navbar>
        
    </div>
    <div class="home-jumbotron" toggle-class="text-lightyellow">
        <b-jumbotron header="Unemployment Claims" lead="How to submit a perfect clain ?" style="background-color:'black' !important">
            <p>This site provides in-detail and step-by-step procedure to submit your unemplayment claim</p>
            <b-button size="lg" style="background-color:#C7FF0D;">Basic Info</b-button>
        </b-jumbotron>
    </div>
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
//   created() {
    
//     let ckeditor = document.createElement("script");
//     ckeditor.setAttribute("src", "//documentcloud.adobe.com/view-sdk/main.js");
//     document.head.appendChild(ckeditor);
//     document.addEventListener("adobe_dc_view_sdk.ready", function() {
//       var adobeDCView = new AdobeDC.View({
//         clientId: "790af3f947c1460881d99bf4110ab2e2",
//         divId: "adobe-dc-view"
//       });
//       adobeDCView.previewFile(
//         {
//           content: {
//             location: {
//               url:
//                 "src/assets/State of Hawaii Guide.pdf"
//             }
//           },
//           metaData: { fileName: "State of Hawaii Guide.pdf" }
//         },
//         {embedMode: "IN_LINE"}
//       );
//     });
//   }
};
</script>

<style>
    .navbar-brand{
        padding-right: 0px;
    }
    body{
        background-color: lightyellow;
    }

    .navbar-dropdown{
        list-style-type: none;
        color: black;
    }

    .jumbotron{
        background-color: lightyellow;
    }


</style>