<template>
  <div class="message rounded border" id="popup-message">
    <div class="p-2 border-bottom d-flex title">
      <img class="rounded-circle" width="28" height="28" :src="avatar" >
      <span class="name ml-2">{{ name }}</span>
      <i class="fas fa-video"></i>
      <i class="fas fa-phone"></i>
      <i class="fas fa-cog"></i>
      <i class="far fa-window-close" @click="closeMessage"></i>
    </div>
    <div class="content">
      <div class="profile d-flex">
        <img :src="avatar" class="rounded" width="50" height="50">
        <div class="detail">
          <div class="title">Các bạn là bạn bè trên Facebook</div>
          <div class="school">Đã học tại Trường THPT Tây Tiền Hải</div>
        </div>
      </div>
      <div v-for="content in contents" :key="content.id" class="item">
        <span class="text">{{ content.text }}</span>
      </div>
    </div>
    <form v-on:submit.prevent="addNewMessage">
      <input autofocus v-model="newContentText" type="text" class="border-top focus" placeholder="Nhập tin nhắn...">
    </form>
    <div class="d-flex icon">
      <i class="fas fa-images"></i>
      <i class="fas fa-icons"></i>
      <i class="fab fa-git-square"></i>
      <i class="fas fa-smile"></i>
      <i class="fas fa-gamepad"></i>
      <i class="fas fa-copy"></i>
      <i class="fas fa-camera"></i>
      <i class="fas fa-thumbs-up"></i>
    </div>
  </div>
</template>

<script>
import { evenBus } from '../../main.js';
export default {
  data() {
    return {
      name: '',
      avatar: '',
      newContentText: '',
      contents: []
    }
  },
  created() {

    evenBus.$on('name', (name) => {
      this.name = name;
    });
    evenBus.$on('avatar', (avatar) => {
      this.avatar = avatar;
    })
  },
  methods: {
    closeMessage() {
      let closeMessage = document.getElementById('popup-message');
      closeMessage.style.display = "none";
      this.contents = [];
      this.newContentText = '';
    },
    addNewMessage() {
      this.contents.push({
        text: this.newContentText
      })
      this.newContentText = ''
    }
  }
}
</script>
