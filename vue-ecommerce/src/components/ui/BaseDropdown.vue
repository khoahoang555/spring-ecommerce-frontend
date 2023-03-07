<template>
<div class="dropdown-container" :class="customPadding">
  <div class="dropdown-title">
    <slot name="title"></slot>
  </div>
  <div class="dropdown-content" :class="customTransform" v-if="isShowing">
    <slot name="content"></slot>
  </div>
</div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({
  props: {
    customPadding: {
      required: true,
      type: String
    },
    customTransform: {
      required: true,
      type: String
    },
    isShowing: {
      required: true,
      type: Boolean
    }
  }
});
</script>

<style scoped>
.dropdown-container {
  position: relative;
  z-index: 4;
  cursor: pointer;
}
.dropdown-title {
  display: flex;
}
.dropdown-content {
  position: absolute;
  right: 0;
  bottom: 0;
  background-color: var(--white);
  border-radius: 10px;
  z-index: 999;
}
.padding-popup-language {
  padding: 18px 0px;
}
.transform-popup-language {
  transform: translate(0, 100%);
}
</style>