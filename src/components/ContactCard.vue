<template>
  <div>
    <div class="p-1"><strong>Tên:</strong> {{ contact.name }}</div>
    <div class="p-1"><strong>Email:</strong> {{ contact.email }}</div>
    <div class="p-1"><strong>Địa chỉ:</strong> {{ contact.address }}</div>
    <div class="p-1"><strong>Điện thoại:</strong> {{ contact.phone }}</div>

    <!-- Cải tiến phần "Yêu thích" -->
    <div class="p-1">
      <strong>Yêu thích:</strong>
      <i 
        :class="{'fas fa-check text-success': contact.favorite, 'fas fa-times text-danger': !contact.favorite}"
        class="favorite-icon"
        :title="contact.favorite ? 'Đang yêu thích' : 'Không yêu thích'"
      ></i>
    </div>

    <!-- Chỉ hiển thị một dòng hiệu chỉnh -->
    <div class="mt-2">
      <router-link :to="{ name: 'contact.edit', params: { id: contact._id } }">
        <span class="badge badge-warning">
          <i class="fas fa-edit"></i> Hiệu chỉnh
        </span>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  props: { contact: Object },
};
</script>

<style scoped>
.favorite-icon {
  font-size: 1.5rem;
  transition: all 0.3s ease;
}

.favorite-icon:hover {
  transform: scale(1.2);
  cursor: pointer;
}

/* Đảm bảo khoảng cách đúng */
.mt-2 {
  margin-top: 10px;
  display: inline-block; /* Đảm bảo chỉ hiển thị một dòng */
}
</style>
