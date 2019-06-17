<template>
  <div class="item" :class="active">
    <a href="#">
      <div class="d-flex">
        <i :class="icon" class="icon"></i>
        <span class="name">{{ name }}</span>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
    name: String,
    active: String
  }
}
</script>
