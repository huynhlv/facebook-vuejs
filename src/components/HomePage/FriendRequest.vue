<template>
  <div class="pt-2 d-flex add-friend">
    <img :src="avatar" class="rounded-circle" width="48" height="48" alt="">
    <div class="ml-2 content">
      <div><a href="#" class="name">{{ name }}</a></div>
      <div class="mutual-friend">{{ mutual }} bạn chung</div>
      <div class="d-flex bt">
        <a class="rounded" href="#">Xác nhận</a>
        <a class="rounded ml-1" href="#">Xóa</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    avatar: String,
    name: String,
    mutual: String
  }
}
</script>
