<template>
  <div class="or-button-group">
    <slot></slot>
  </div>
</template>
  <script>
    export default {
      name: "buttonGroup",
      data() {
        return {}
      },
      methods: {}
    }
  </script>

  <style lang="scss" scoped>
  @import "../theme/components/buttonGroup.scss";
  </style>
