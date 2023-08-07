<template>
  <div class="literature">
    <ol>
      <li v-for="(item, index) in arr" :key="index" @click="browse(item)">
        <div class="icon">
          <img :src="item.imgs" alt="" />
        </div>
        <div class="text">
          <p style="font-size: 17px">{{ item.name }}</p>
          <p style="font-size: 14px; color: gray">{{ item.author }}</p>
          <p style="font-size: 14px; color: gray">推荐值{{ item.recommend }}</p>
          <span>
            <img
              src="https://weread-1258476243.file.myqcloud.com/miniprogram/common/book_readers.svg"
              alt=""
            />
            {{ item.numb }}
          </span>
        </div>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [
        {
          name: "我与地坛",
          author: "史铁生",
          recommend: "91.1%",
          imgs: "https://wfqqreader-1252317822.image.myqcloud.com/cover/44/674044/t6_674044.jpg",
          numb: 3146,
        },
        {
          name: "红楼梦",
          author: "曹雪芹",
          recommend: "93.2%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/45/YueWen_34615967/t6_YueWen_34615967.jpg",
          numb: 3022,
        },
        {
          name: "封神演义（中国古典文学名著）",
          author: "许仲林",
          recommend: "70.6%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/59/YueWen_823352/t6_YueWen_823352.jpg",
          numb: 1796,
        },
        {
          name: "平凡的世界 (全三册)",
          author: "路遥",
          recommend: "93.1%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/61/yuewen_24965201/t6_yuewen_249652011682413401.jpg",
          numb: 1634,
        },
        {
          name: "生死疲劳",
          author: "诺言",
          recommend: "92.5%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/55/YueWen_26435427/t6_YueWen_26435427.jpg",
          numb: 1572,
        },
        {
          name: "杀死一只知更鸟",
          author: "哈伯·李",
          recommend: "91.9%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/32/YueWen_853116/t6_YueWen_853116.jpg",
          numb: 1460,
        },
        {
          name: "白鹿原",
          author: "陈忠实",
          recommend: "91.1%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/78/YueWen_812443/t6_YueWen_812443.jpg",
          numb: 1306,
        },
        {
          name: "西游记",
          author: "吴承恩",
          recommend: "93.2%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/22/yuewen_34631845/t6_yuewen_346318451676961764.jpg",
          numb: 1030,
        },
        {
          name: "你当像鸟飞往你的山",
          author: "塔拉·韦斯特弗",
          recommend: "86.3%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/22/YueWen_26713355/t6_YueWen_26713355.jpg",
          numb: 1017,
        },
        {
          name: "一地鸡毛（典藏版）",
          author: "刘震云",
          recommend: "92.3%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/85/3300010685/t6_3300010685.jpg",
          numb: 745,
        },
      ],
    };
  },

  mounted() {},

  methods: {
    browse(item) {
      item.numb += 1;
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
a {
  text-decoration: none;
}
.literature ol li {
  margin-top: 5%;
  display: flex;
  z-index: 0;
}
.literature ol li .icon {
  width: 20%;
  height: 110px;
}
.literature ol li .icon img {
  width: 100%;
  height: 100%;
}
.literature ol li .text {
  width: 80%;
  height: 100px;
  /* background-color: pink; */
  position: relative;
}
.literature ol li .text p {
  margin-left: 20px;
  line-height: 40px;
}
.literature ol li .text p:first-child {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  width: 65%;
}
.literature ol li .text span {
  position: absolute;
  display: inline-block;
  text-align: center;
  width: 18%;
  font-size: 10px;
  right: 5px;
  top: 10px;
  background-color: #f1f1f1;
  color: gray;
  border-radius: 10px;
}
</style>
