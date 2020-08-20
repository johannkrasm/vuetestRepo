<template>
  
  <div class="about">
    



   <!-- <DocCrud :pShowSearch=false pProcesshref="/cm/00000000-0000-01/la/00000000-0000-03/pr/da8e9461-c578-49"> </DocCrud>  -->
   <!-- <TypCrud  pSenderName="0610663309" :pShowSearch=false > </TypCrud> -->
   <h3>-----------------</h3>
   <!-- <SchedCrud pSchedId = "GVE" :pShowSearch=false > </SchedCrud> -->
   <div>
     <div>
       <div>
      <div>

      </div>
       </div>
     </div>
   <!-- <link rel="icon" href="/favicon.ico"/> -->
   </div>
   <!-- <SingleDocView></SingleDocView> -->
    <h1></h1>


  <!-- <v-btn color="primary" v-on:click="theDocFunction()"> Opna Doc</v-btn> -->

    
    <h2>This is the about page</h2>
    <h2>Version: {{theVersion}}</h2>
    <h2>baseUrl: {{ baseUrl }}</h2>
    <h2>environment: {{ theEnv }}</h2>
    <br/>

    <!-- her er daemi um href medhondlun
    <a
    v-for="link in mylinks"
    :key="link.name"
    :href="link.href"
    :target="link.target"
    rel="noopener noreferrer">
    {{ link.name }}
    </a>
    -->
  
  
  </div>


</template>

<script lang="ts">
import Vue from "vue";
//import MyAppConfig from "../utils/myApp.config";
//import DocumentView from "../views/DocumentView.vue";
//import TypeView from "../views/TypeView.vue";

//import SingleDocView from "../components/SingleDocView.vue";

//import { Component, Prop } from "vue-property-decorator";
/*
@Component({
  components: {  TypeView, SingleDocView }
})
*/
export default class About extends Vue {
  baseUrl: string = "mylocalhost"; //MyAppConfig.getGvBaseUrl();
  theEnv: string = "test"; //process.env.NODE_ENV;

  theVersion: string = "2.0";

  docUrl: string = "http://localhost:8085/v1/birta/doc/cm/a98f8631-cd4d-44/sa/e3d0d470-9ccc-4a/doc/cac7e11b-1e43-46/xmlContent/6808003240-15.3.2019.xml";
  mylinks = [
    { name: "Home", href: "/dashboard", target: "_self" },
    { name: "Google", href: "https://www.google.com/", target: "_blank" },
    { name: "Xml Doc", href: this.docUrl, target: "_blank" }
  ];

  constructor() {
    super();
    try {
      // let baseUrl = MyAppConfig2.getGvBaseUrl();
    } catch (error) {
      console.log("error:" + error);
    }
  }

  theDocFunction() {
    window.open(this.docUrl, "_blank");
  }
}
</script>
