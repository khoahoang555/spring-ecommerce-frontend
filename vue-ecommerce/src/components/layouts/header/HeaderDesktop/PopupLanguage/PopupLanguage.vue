<template>
  <BaseDropdown
      custom-transform="transform-popup-language"
      custom-padding="padding-popup-language"
      :is-showing="isShowing"
  >
    <template v-slot:title>
      <div class="language-container" @mouseover="showDropdownContent" @mouseleave="hideDropdownContent">
        <div class="image-item">
          <img src="@/assets/images/header/default.svg" class="custom-img" alt="icon">
<!--          <img src="@/assets/images/header/english.svg" class="custom-img" alt="icon">-->
          <img src="@/assets/images/header/icon_seemore_gray.svg" class="ml-custom" alt="icon">
        </div>
      </div>
    </template>
    <template v-slot:content>
      <div class="content-language-container">
        <div class="item-language active">
          <img src="@/assets/images/header/default.svg" alt="VietNam">
          <span>VN</span>
        </div>
        <div class="item-language">
          <img src="@/assets/images/header/english.svg" alt="English">
          <span>EN</span>
        </div>
      </div>
    </template>
  </BaseDropdown>
</template>

<script lang="ts">
import {defineComponent} from "vue";
import BaseDropdown from "@/components/ui/BaseDropdown.vue";

export default defineComponent({
  components: {BaseDropdown},
  data() {
    return {
      isShowing: false
    }
  },
  methods: {
    showDropdownContent() {
      this.isShowing = true;
    },
    hideDropdownContent() {
      this.isShowing = false;
    }
  }
});
</script>

<style scoped>
.language-container {
  width: 70px;
  height: 40px;
  position: relative;
  border: 1px solid var(--main-border-color);
  border-radius: 10px;
  margin-left: 10px;
}
.image-item {
  display: flex;
  top: 50%;
  left: 50%;
  position: absolute;
  transform: translate(-50%, -50%);
}
.content-language-container {
  padding: 10px;
}
.item-language {
  display: flex;
  justify-content: center;
  padding: 10px;
}
.item-language img {
  width: 32px;
  height: 24px;
  margin-right: 8px;
}
.item-language span {
  font-weight: 500;
  color: #7a7e7f;
}
.custom-img {
  width: 34px !important;
  height: 22px !important;
}
.ml-custom {
  margin-left: 0.25rem !important;
}
.active {
  background-color: var(--main-background-color);
  border-radius: 5px;
}
</style>