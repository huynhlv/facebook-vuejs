<template>
  <div class="pt-2 d-flex new">
    <a href="#">
      <img :src="avatar" class="rounded-circle img-border" width="50" height="50" alt="">
    </a>
    <div class="ml-2">
      <div class="name"><a href="#">{{ name }}</a></div>
      <span>{{ time }}</span>
    </div>

  </div>
</template>
<script>
export default {
  props: {
    avatar: String,
    name: String,
    time: String
  }
}
</script>
