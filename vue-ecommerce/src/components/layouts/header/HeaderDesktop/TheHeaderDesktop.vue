<template>
  <div class="header-container-desktop">
    <div class="container no-padding">
      <div class="header-item">
        <div class="header-logo">
          <img src="@/assets/images/header/fahasa_logo.png" />
        </div>
        <div class="header-category">
          <img src="@/assets/images/header/ico_menu.svg" />
          <img src="@/assets/images/header/icon_seemore_gray.svg" />
        </div>
        <div class="header-search">
          <form action="">
            <div class="form-search">
              <input type="text" placeholder="Tìm kiếm sản phẩm mong muốn..."/>
              <button type="submit"><i class="fa-solid fa-magnifying-glass"></i></button>
            </div>
          </form>
        </div>
        <div class="header-functions">
          <div class="function-item">
            <img src="@/assets/images/header/ico_noti_gray.svg">
            <span>Thông báo</span>
          </div>
          <div class="function-item">
            <img src="@/assets/images/header/ico_cart_gray.svg">
            <span>Giỏ hàng</span>
          </div>
          <div class="function-item">
            <img src="@/assets/images/header/ico_account_gray.svg">
            <span>Tài khoản</span>
          </div>
          <div class="function-item">
            <div class="language-container">
              <div class="image-item">
                <img src="@/assets/images/header/default.svg" alt="icon" width="34px" height="22px">
                <img src="@/assets/images/header/icon_seemore_gray.svg" class="ml-1" alt="icon">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({

});
</script>

<style scoped>
.header-container-desktop {
  background-color: var(--white);
}

.header-item {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 68px;
}

.header-category {
  display: flex;
  width: 90px;
  margin-right: 5px;
  justify-content: end;
}

.header-functions {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 40px;
  margin-left: 20px;
}

.header-functions .function-item {
  display: flex;
  flex-direction: column;
  margin-left: 10px;
  align-items: center;
  width: 72px;
  font-size: 15px;
}

.language-container {
  position: relative;
  height: 40px;
  border: 1px solid var(--main-border-color);
  border-radius: 10px;
  width: 70px;
}

.language-container .image-item {
  display: flex;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.form-search {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 566px;
  height: 40px;
  border: 1px solid var(--main-border-color);
  border-radius: 10px;
}

.form-search input {
  height: 20px;
  margin-left: 15px;
  width: 472px;
  border: none !important;
  outline: none;
  font-size: 15px;
  padding: 0px !important;
}

.header-search button {
  width: 72px;
  height: 32px;
  background-color: var(--red);
  border: none;
  border-radius: 10px;
  color: var(--white);
  font-size: 15px;
}
</style>