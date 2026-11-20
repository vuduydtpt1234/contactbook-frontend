<script>
export default {
  props: {
    contact: { type: Object, required: true },
  },
};
</script>

<template>
  <div class="card">
    <div class="card-header">
      <i class="fas fa-address-card"></i>
      {{ contact.name }}
    </div>

    <ul class="list-group list-group-flush">
      <li class="list-group-item">
        <i class="fas fa-envelope"></i>
        Email: {{ contact.email }}
      </li>

      <li class="list-group-item">
        <i class="fas fa-address-book"></i>
        Địa chỉ: {{ contact.address }}
      </li>

      <li class="list-group-item">
        <i class="fas fa-phone"></i>
        Điện thoại: {{ contact.phone }}
      </li>

      <li class="list-group-item">
        <i class="fas fa-star" v-if="contact.favorite"></i>
        {{ contact.favorite ? "Liên hệ yêu thích" : "" }}
      </li>
    </ul>
  </div>
</template>
