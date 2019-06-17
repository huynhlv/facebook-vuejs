<template>
  <div class="online">
    <div v-for="item in items" :key="item.id" class="pl-2 py-1 d-flex item">
      <img class="rounded-circle" :src="item.avatar" width="32" height="32">
      <span class="ml-2 name">{{ item.name }}</span>
      <span class="icon-online"><i class="fas fa-circle"></i></span>
    </div>
    <div class="search">
      <i class="fas fa-search ml-2"></i>
      <input type="text" placeholder="Tìm kiếm">
      <i :title="'Tùy chọn'" class="fas fa-cog mr-1"></i>
      <i :title="'Tin nhắn mới'" class="fas fa-calendar-plus mr-1"></i>
      <i :title="'Tạo nhóm mới'" class="fas fa-user-plus mr-1"></i>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          avatar: 'https://scontent.fdad3-1.fna.fbcdn.net/v/t1.0-1/p32x32/53080015_1249086161906298_3767192497667702784_n.jpg?_nc_cat=110&_nc_oc=AQlItcJgY9dTER1tp05xnALANnyQXbDRa7W2cpDO9RK9raQHB9c0FY4ZtjXTGLCepMw&_nc_ht=scontent.fdad3-1.fna&oh=21575b396a00f02de2c3409bbf9c762a&oe=5D83BF14',
          name: 'Hoai Koy'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/p80x80/61953165_1025195297678176_3598365841592156160_n.jpg?_nc_cat=108&_nc_oc=AQkQjgkYIWsPZzNpKXznEgwqqLOVBkI6xV3zgyjd0jX2oQEZOczwY8bLluxmIYe603M&_nc_ht=scontent.fdad2-1.fna&oh=888172f23fb527d179bd30daf1aafc46&oe=5D90926E',
          name: 'Thùy Nhi'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/c0.0.80.80a/p80x80/61773087_924292944629787_7234156774071205888_n.jpg?_nc_cat=105&_nc_oc=AQnQeCYCtjSuD2jm3epUZvsi_VfKNAm4szUoLnq0yapj8EhY6KEjz8g1Js8yyk-r7vE&_nc_ht=scontent.fdad1-1.fna&oh=623949d2bf018da7fe5569ec3254c285&oe=5D95E1B3',
          name: 'Mỹ Vân'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/p80x80/64524284_2111038539195247_139379140523458560_n.jpg?_nc_cat=105&_nc_oc=AQnbX5XRyvSJ4LAqTrBM5bFgdrEYvs0WABFPWeXct-MmTHr04VcjIOxbO14LTA2khcE&_nc_ht=scontent.fdad1-1.fna&oh=35923e64c2db09c436660affa036e100&oe=5D866244',
          name: 'Ngọc Trâm'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/c0.10.80.80a/p80x80/60722277_1321359514678837_6717087276213469184_n.jpg?_nc_cat=102&_nc_oc=AQmhjRuIAK8J3S4azOyhXYlLXmL5cgBqNj8eD6GlIRGzvnRRN3p9TdIvUN42MGCVht0&_nc_ht=scontent.fdad1-1.fna&oh=c910a762141437432a517034d43d0b51&oe=5D7FB6CB',
          name: 'Lệ Hằng'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/c0.14.80.80a/p80x80/62303858_1358344867650107_4338797291226791936_n.jpg?_nc_cat=105&_nc_oc=AQlr03vctDhY6uKSE1geY2Xj_Rh-1znxKu4SZSfKD0C4NNS077eJaquq0oMgEDK5Vqk&_nc_ht=scontent.fdad1-1.fna&oh=5406635c602567894c96d516034889a7&oe=5D81CC84',
          name: 'Thanh Hạ'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/p80x80/64378516_1268424093317358_929346986308534272_n.jpg?_nc_cat=104&_nc_oc=AQmifIW4q8E29fcOjRZX0ZiIP3Xm-dzdRHRa1Y6KuwomGdVwL-4z7iRbt4VaK6XdWIg&_nc_ht=scontent.fdad1-1.fna&oh=405b8cb92e7aa4e32a1870645b15afa4&oe=5D8EC00F',
          name: 'Quỳnh Sambi'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/p80x80/62120236_1316077648547735_6314944892673982464_n.jpg?_nc_cat=102&_nc_oc=AQkNKXg0qDmRcDl0x5Lk37IXKI7vIs5Cu6ZpvUuyw_HQVXcEbzf5e7kyIE6oP4dyG5U&_nc_ht=scontent.fdad1-1.fna&oh=85284884995f8e007d773e7c41add29c&oe=5D8F63AA',
          name: 'Nga Hoang'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.20.80.80a/p80x80/62517516_3034633853428575_4270531040914702336_n.jpg?_nc_cat=107&_nc_oc=AQl82FiIzZ67HikrJzdKGj0a26FPGM9507GdXeDCUeQKjezOSp3QtfUPJd06X75bHaQ&_nc_ht=scontent.fdad2-1.fna&oh=47a03e12a68b5662cfc15efcf151cf72&oe=5D790BB3',
          name: 'Nguyen Linh'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.10.80.80a/p80x80/61314276_2351249841760751_6886126043543896064_n.jpg?_nc_cat=111&_nc_oc=AQmBVyKsJOfBXUYzYhUiDLASyWCTczKK9SAecSYr9UnSjGG2esrPSmcN-OfGFlWoLtI&_nc_ht=scontent.fdad2-1.fna&oh=ae53094f747bba18ba5c77e77efbe412&oe=5D8A5AF9',
          name: 'Hà Trần'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/c1.0.80.80a/p80x80/60178389_2334116703537985_5035951817163276288_n.jpg?_nc_cat=100&_nc_oc=AQmguOsRJHqGhvf3ebVcT7D-R0czIQ3hQxscXYWbzQ8FlAc5R0BrY5m-JGJQDDuGJlk&_nc_ht=scontent.fdad1-1.fna&oh=803b92526bb11f00110462820a01d11d&oe=5D82869C',
          name: 'Phượng Ruby'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/p80x80/55622707_2295752284083960_7610520901339054080_n.jpg?_nc_cat=104&_nc_oc=AQlNzHu3S5evg2154un13k7DD5n_wYTOth_kSdkFxatfLYUXiYQZlQClf3P2ABqMYr8&_nc_ht=scontent.fdad1-1.fna&oh=8efa1b99f077fd305985104c1b233540&oe=5D96B878',
          name: 'Trang Lê'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.0.80.80a/p80x80/61836822_2934641780093636_2283943881504456704_n.jpg?_nc_cat=107&_nc_oc=AQm725XW-Nvy8IMEgJhPF27urN7aT5L91us-FMQSagbv82QuHd4XjxyTpdZ2-fnn2qQ&_nc_ht=scontent.fdad2-1.fna&oh=a8364b5249c4be4f21fd2cbd4a478e16&oe=5D8774F8',
          name: 'Út Nhỏ'
        }
      ]
    }
  }
}
</script>
