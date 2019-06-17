<template>
  <div>
    <div class="sidebar">
      <ItemNav v-for="item in items" :icon="item.icon" :name="item.name" :active="item.active" :key="item.id"/>
      <div class="shortcuts">Lối tắt</div>
      <ItemNav v-for="shortcut in shortcuts" :key="shortcut.id"
        :icon="shortcut.icon"
        :name="shortcut.name"
      />
    </div>
  </div>
</template>

<script>
import ItemNav from './ItemNav.vue'
export default {
  data () {
    return {
      shortcuts: [
        {
          icon: 'fab fa-adversal text-info',
          name: 'Rub City',
        },
        { 
          icon: 'fas fa-users',
          name: 'Nhóm'
        },
        {
          icon: 'fas fa-scroll text-danger',
          name: 'Trang'
        },
        {
          icon: 'fas fa-calendar-alt text-warning',
          name: 'Sự kiện'
        },
        {
          icon: 'fas fa-gamepad text-primary',
          name: 'Trò chơi'
        }
      ],
      items: [
        { 
          icon: 'fas fa-newspaper active',
          name: 'Bản tin',
          active: 'active'
        },
        { 
          icon: 'fab fa-facebook-messenger',
          name: 'Messenger'
        },
        {
          icon: 'fas fa-camera-retro',
          name: 'Watch'
        }
      ]
    }
  },
  components: {
    ItemNav
  }
}
</script>
