<template>
  <div class="post rounded mt-2">
    <div class="content">
      <div class="d-flex">
        <img :title="name" :src="avatar" class="rounded-circle" width="40" height="40">
        <div class="ml-2 profile">
          <a href="#" class="name" :title="name">{{ name }}</a>
          <div class="time">{{ time }} - <i class="fas fa-globe-africa"></i></div>
        </div>
        <span class="dots">
          <a href="#"><i class="fas fa-ellipsis-h"></i></a>
        </span>
      </div>
      <div class="mt-2 description">
        <div>{{ stt }}</div>
      </div>
    </div>
    <div class="image">
      <img :src="image">
    </div>
    <div class="interactive">
      <div class="d-flex title pb-2 border-bottom">
        <i class="fab fa-gratipay"></i>
        <span class="ml-1" :title="like"><a href="#">{{ likes }}</a></span>
        <span class="title-comment">
          <a href="#">{{ comments }} bình luận</a>
        </span>
      </div>
      <div class="d-flex button border-bottom">
        <button><i class="far fa-thumbs-up mr-1"></i>Thích</button>
        <button><i class="far fa-comment-alt mr-1"></i>Bình luận</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    avatar: String,
    name: String,
    time: String,
    stt: String,
    image: String,
    likes: String,
    comments: String
  },
  data() {
    return {
      like: 'Nguyễn Hạnh'
    }
  }
}
</script>
