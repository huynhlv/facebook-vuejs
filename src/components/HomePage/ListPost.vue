<template>
  <div class="list-post">
    <div class="new-post rounded">
      <div class="title rounded-top border-bottom text-gray">Tạo bài viết</div>
      <div class="d-flex content border-bottom">
        <img :title="'Lê Huỳnh'" class="rounded-circle" src="https://scontent.fdad3-2.fna.fbcdn.net/v/t1.0-1/c141.115.755.755a/s40x40/59410777_1000376926827965_5249272818301927424_n.jpg?_nc_cat=101&_nc_oc=AQmbYTWi2Hag9HS3nUhPrKYcOre9CKOVp4HdSk716MHtfniWYFhR9hlcNeO_Nzzbpc8&_nc_ht=scontent.fdad3-2.fna&oh=250f5a9f23d2e78efe2ba028e1949582&oe=5D89C961">
        <input type="text" placeholder="Huỳnh ơi, bạn đang nghĩ gì?">
      </div>
      <div class="utilities d-flex">
        <div class="image-video">
          <a href="#">
            <i class="fas fa-images"></i>
            <span>Ảnh/Video</span>
          </a>
        </div>
        <div class="image-video">
          <a href="#">
            <i class="fas fa-user-tag"></i>
            <span>Gắn thẻ bạn bè</span>
          </a>
        </div>
        <div class="image-video">
          <a href="#">
            <i class="fas fa-grin"></i>
            <span>Cảm xúc/Hoạt động</span>
          </a>
        </div>
      </div>
    </div>
    <div>
      <Post
        v-for="item in items" :key="item.id"
        :avatar="item.avatar"
        :name="item.name"
        :time="item.time"
        :stt="item.stt"
        :image="item.image"
        :likes="item.likes"
        :comments="item.comments"
      />
    </div>
  </div>
</template>

<script>
import Post from './Post.vue'
export default {
  data(){
    return {
      items: [
        {
          avatar: 'https://scontent.fdad3-1.fna.fbcdn.net/v/t1.0-1/p50x50/42438095_2350901638260291_1266491374899822592_n.jpg?_nc_cat=106&_nc_oc=AQkgVA3goOS4rPPIBmkxlFPrraCZFmhXmx7QaV3xKvaRaLjMBu4ecvpVcc0Du6A-fEM&_nc_ht=scontent.fdad3-1.fna&oh=5787ee4ab73273edcea31689eeac8745&oe=5D8FC064',
          name: 'Nguyen Ngoc',
          time: '1 giờ',
          stt: 'Có bác nào như em không. Rất thích dùng đồ của apple nhưng riêng điện thoại lại khoái android.',
          image:'https://scontent.fdad3-1.fna.fbcdn.net/v/t1.0-0/p526x296/64417014_2791382357545548_9005784243405586432_n.jpg?_nc_cat=102&_nc_oc=AQkOnMi-E0kNaebFLnSl2HG6vN47ZgLBnaLK040ykN2S2_CzTR3mejFDHqwn_E11tSg&_nc_ht=scontent.fdad3-1.fna&oh=1558bfb9807a1b9c2932f5816990296d&oe=5D78C345',
          likes: '123',
          comments: '241'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.0.50.50a/p50x50/61731499_368919750421237_7381845499491385344_n.jpg?_nc_cat=109&_nc_oc=AQmDDm8E15QSPZ1z8RzgJiFJ7QLIvvq1meUH6GB8nOizpaEOy5X8U1WFqNKd4gTz8lw&_nc_ht=scontent.fdad2-1.fna&oh=6c5c96140c69043e35f62b594e250b02&oe=5D9392C2',
          name: 'Nguyen Nhan',
          time: '3 giờ',
          stt: '- Nếu nỗi buồn hóa thành mưa, thế gian này có nơi nào mà không ướt -',
          image:'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-0/p526x296/64313771_375503523096193_855926736586539008_n.jpg?_nc_cat=107&_nc_oc=AQmoFbnx3KBfQcZb9SYw1wrW4cQNRnO-tVJbGSJvbFVPlIfG0p86oyTSXd1ZJpUcOTw&_nc_ht=scontent.fdad2-1.fna&oh=a467d7fa112d9d1fede5e9ce5d8c826c&oe=5D8DE2D8',
          likes: '123',
          comments: '241'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/c0.11.50.50a/p50x50/46334313_1925273274435285_5850594804114653184_n.jpg?_nc_cat=1&_nc_oc=AQksl8k9m5-bEi4GYNcUj3fCkxaR1w0O5YYg7mTpVIPcGezmDMHBs2lJKOM1qcbDyNY&_nc_ht=scontent.fdad1-1.fna&oh=d531494281fe0f76bbe980673ecde1bf&oe=5D82E0A8',
          name: 'Lee Dzung',
          time: '5 giờ',
          stt: 'Ae nào có đổi gió cho vui E có bù trừ hợp lý ạ',
          image:'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-0/p526x296/64442756_2232909146744872_2714276428920127488_n.jpg?_nc_cat=108&_nc_oc=AQndGYzlHTR1CC9rBBq8Uujl9we0VgNLnUwYll8mgUU-S5xQwwaeib-dEvKq15KHOCs&_nc_ht=scontent.fdad2-1.fna&oh=7112ce15b55834f0a8c49fb5b690d6f6&oe=5D92455B',
          likes: '123',
          comments: '241'
        }
      ]
    }
  },
  components: {
    Post
  }
}
</script>
