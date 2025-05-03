<script>
export default {
  name: "App",
};
</script>

<template>
  <div>
    <!-- App Header -->
    <div class="app-header">
  Ứng dụng Quản lý danh bạ <i class="fas fa-address-book"></i>
</div>



    <!-- Main content: 2 cột ContactList và ContactCard -->
    <div class="main-content">
      <!-- Vue Router sẽ hiển thị component theo route -->
      <router-view />
    </div>
  </div>
</template>

<style>
/* CSS riêng cho App.vue */
.app-header {
  background-color: #343a40;
  color: white;
  padding: 15px;
  font-size: 20px;

}

.input-search {
  display: flex;
  justify-content: center;
  margin-top: 10px;
}

.input-search input {
  width: 300px;
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 3px;
}

.input-search button {
  margin-left: 5px;
  padding: 5px 10px;
  cursor: pointer;
}

.main-content {
  display: flex;
  justify-content: center;
  gap: 40px;
  margin-top: 20px;
}
</style>
