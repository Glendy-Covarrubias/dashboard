<template>
  <a-tabs defaultActiveKey="2">
    <a-tab-pane key="1">
      <span slot="tab">
        <a-icon type="apple" />
        Tab 1
      </span>
      <rate-component />
      <comment-component />
    </a-tab-pane>
    <a-tab-pane key="2">
      <span slot="tab">
        <a-icon type="android" />
        Tab 2
      </span>
      Tab 2
    </a-tab-pane>
  </a-tabs>
</template>
<script>
import RateComponent from "./RateComponent.vue"
import CommentComponent from "./CommentComponent.vue"

export default {
  components : {
    RateComponent,
    CommentComponent
  },
  data() {
    return {
    //   collapsed     : false,
    //   titleBar      : "Capacitación",
    //   titleSection  : "Mi Dashboard </>"
    }
  },
  mounted(){
    // invocar los métodos
    // this.getSession();
    // console.log(this.collapsed);
  },
  methods : {
  }
}
</script>