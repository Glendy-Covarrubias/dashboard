<template>
  <a-rate v-model='value' allowHalf/>
</template>
<script>
export default {
  data() {
    return {
      value: 2,
    }
  },
}
</script>