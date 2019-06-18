<template>
  <div class="home d-flex">
    <Sidebar />
    <ListPost />
    <News />
    <Online />
    <PopupMessage />
  </div>
</template>
<script>
  import Sidebar from './Sidebar.vue'
  import ListPost from './ListPost.vue'
  import News from './News.vue'
  import Online from './Online.vue'
  import PopupMessage from './PopupMessage.vue'
  export default {
    components: {
      Sidebar,
      ListPost,
      News,
      Online,
      PopupMessage
    }
  }
</script>
