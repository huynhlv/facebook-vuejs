<template>
  <div class="w-25">
    <div class="news ml-2 rounded p-2">
      <div class="title d-flex">
        <span :title="'Tin là ảnh và video hiểu thị trong 24h giờ. Khi ai đó thêm vào tin, tin đó sẽ hiển thị ở đây'"
          class="name">Tin</span>
        <span class="utilities">
          <a href="#">Lưu trữ</a> -
          <a href="#">Cài đặt</a>
        </span>
      </div>
      <New 
        v-for="item in items" :key="item.id"
        :avatar="item.avatar"
        :name="item.name"
        :time="item.time"
      />
    </div>
    <div class="birthday ml-2 rounded p-2 mt-2 d-flex">
      <a href="#">
        <i class="fas fa-gift"></i>
        <span class="ml-1">Lê Văn Huỳnh</span>
      </a>
    </div>
    <div class="friend-request ml-2 rounded p-2 mt-2">
      <div class="title d-flex">
        <span>Lời mời kết bạn</span>
        <a href="#">Xem tất cả</a>
      </div>
      <FriendRequest
        v-for="friend in friends" :key="friend.id"
        :avatar="friend.avatar"
        :name="friend.name"
        :mutual="friend.mutual"
      />
    </div>
  </div>
</template>
<script>
import New from './New.vue'
import FriendRequest from './FriendRequest.vue'
export default {
  components: {
    New,
    FriendRequest
  },
  data() {
    return {
      friends: [
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.0.80.80a/p80x80/49211072_590983364680934_3957939794943672320_n.jpg?_nc_cat=110&_nc_oc=AQl1CZsCCIrONYnjqmZwGiuveTumzC0B0oDpZkZX9C_WHC2CXaWks6EVeAAk-cxXl7U&_nc_ht=scontent.fdad2-1.fna&oh=12c4e7275fd351515a7d0d452176341f&oe=5D79ED59',
          name: 'Hải Yến',
          mutual: '67'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/p80x80/64204410_2362300047387592_912144289373356032_n.jpg?_nc_cat=106&_nc_oc=AQlUAGRdbGTS4Ri8ZrkWKvocLw0fKkL9XPCLS0QC8QxrUkl-6xwtkpii4HuSn63xg2Y&_nc_ht=scontent.fdad1-1.fna&oh=28ec35760f4c057e2cc3728e64a3afe9&oe=5D983FFA',
          name: 'Huyền Ngô',
          mutual: '52'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.13.80.80a/p80x80/61552963_1156771247835317_8939247116862095360_n.jpg?_nc_cat=111&_nc_oc=AQk5Zhkuir0U4vvzcE21cqRPsK-aXBDXle065IAYWjgjo8Z5uSz4N4hgycF63eDmPUo&_nc_ht=scontent.fdad2-1.fna&oh=b6966549d42bd3cd6350e5b4b7360975&oe=5D82B3C0',
          name: 'Trần Nhung',
          mutual: '12'
        }
      ],
      items: [
        {
          avatar: 'https://scontent.fdad3-1.fna.fbcdn.net/v/t1.0-1/p80x80/54257758_1100894286737730_5848651593406218240_n.jpg?_nc_cat=103&_nc_oc=AQl3orduiTSO2HxWHIvOIogBkY6M2dki0Ot5MGY9X-qAQ03E2aISCV-uG8ZV3z_Cd0Q&_nc_ht=scontent.fdad3-1.fna&oh=096c2527963e07667397d8c054d1665c&oe=5D9239FC',
          name: 'Hồng Thắm',
          time: 'khoảng 1 giờ trước'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/c0.10.80.80a/p80x80/61314276_2351249841760751_6886126043543896064_n.jpg?_nc_cat=111&_nc_oc=AQnj4yoCJYbVfmFxvpoNjNkv_NDx1jxDVXN_49Z-aKKrwaLibQfzIabaF2q62V57IV4&_nc_ht=scontent.fdad2-1.fna&oh=bb639db557c903f2f6273b041e2dfccc&oe=5D8A5AF9',
          name: 'Mai Hồng',
          time: 'khoảng 2 giờ trước'
        },
        {
          avatar: 'https://scontent.fdad1-1.fna.fbcdn.net/v/t1.0-1/c0.0.80.80a/p80x80/51699172_1280212128792735_3191024640659030016_n.jpg?_nc_cat=103&_nc_oc=AQkATyAAwcOsu10Np3iWpkOAqb92j6L4a1JB6M8Ke8cTuOrmLr3Ttkvx7q3t0NSw8tE&_nc_ht=scontent.fdad1-1.fna&oh=5f61d4010bf86ca918c2afb2edae51da&oe=5D78E330',
          name: 'Thần Nuy',
          time: 'khoảng 3 giờ trước'
        },
        {
          avatar: 'https://scontent.fdad2-1.fna.fbcdn.net/v/t1.0-1/p80x80/62583543_1201451780035490_8042627867248427008_n.jpg?_nc_cat=107&_nc_oc=AQn12aSRzR4wxgp4IyCsYbw-CORAskyvdWvot9YyLtsXVUL6KVUWahde8g9Wik_hxGM&_nc_ht=scontent.fdad2-1.fna&oh=21b14888ece4e8f077b648265406d937&oe=5D916D17',
          name: 'Ngọc Ánh',
          time: 'khoảng 4 giờ trước'
        }
      ]
    }
  }
}
</script>
