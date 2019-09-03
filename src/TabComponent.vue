<template>
  <a-tabs defaultActiveKey="2">
    <a-tab-pane key="1">
      <span slot="tab">
        <a-icon type="dashboard" />
        Calificando
      </span>
      <span>Ranking: </span>
      <rate-component />
      <comment-component />
    </a-tab-pane>
    <a-tab-pane key="2">
      <span slot="tab">
        <a-icon type="read" />
        Descripción
      </span>
      <skeleton-component />
    </a-tab-pane>
  </a-tabs>
</template>
<script>
import RateComponent from "./RateComponent.vue"
import CommentComponent from "./CommentComponent.vue"
import SkeletonComponent from "./SkeletonComponent.vue"

export default {
  components : {
    RateComponent,
    CommentComponent,
    SkeletonComponent
  },
  data() {
    return {
    }
  },
  mounted(){
  },
  methods : {
  }
}
</script>