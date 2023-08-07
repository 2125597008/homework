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
          name: "明朝那些事儿（全集）",
          author: "当年明月",
          recommend: "92.4%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/61/YueWen_822995/t6_YueWen_822995.jpg",
          numb: 3146,
        },
        {
          name: "长安的荔枝",
          author: "马伯庸",
          recommend: "95.4%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/75/cpPlatform_dbb14284a55f1e733b60202b0777255d/t6_cpPlatform_dbb14284a55f1e733b60202b0777255d.jpg",
          numb: 3022,
        },
        {
          name: "翦商：殷周之变与华夏新生",
          author: "李硕",
          recommend: "95.2%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/31/cpplatform_qgm8mx4we5qpr3jsaspa9n/t6_cpplatform_qgm8mx4we5qpr3jsaspa9n1679558201.jpg",
          numb: 9487,
        },
        {
          name: "让人拍案叫绝的中国史",
          author: "渤海小吏",
          recommend: "94.0%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/67/YueWen_36235932/t6_YueWen_36235932.jpg",
          numb: 6275,
        },
        {
          name: "一读就上瘾的中国史",
          author: "温伯陵",
          recommend: "79.0%",
          imgs: "https://wfqqreader-1252317822.image.myqcloud.com/cover/844/34560844/t6_34560844.jpg",
          numb: 4795,
        },
        {
          name: "大明王朝1566 (全集)",
          author: "刘和平",
          recommend: "91.3%",
          imgs: "https://wfqqreader-1252317822.image.myqcloud.com/cover/310/847310/t6_847310.jpg",
          numb: 3489,
        },
        {
          name: "弃长安",
          author: "张名扬",
          recommend: "94.1%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/50/cpplatform_2gsdqbnn8ehtt9wkwjztqj/t6_cpplatform_2gsdqbnn8ehtt9wkwjztqj1689577123.jpg",
          numb: 3347,
        },
        {
          name: "三国争霸",
          author: "渤海小吏",
          recommend: "90.1%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/20/cpplatform_n2g8fnd9eu4fj5fssec8sy/t6_cpplatform_n2g8fnd9eu4fj5fssec8sy1680848708.jpg",
          numb: 2874,
        },
        {
          name: "半小时漫画史记 (全5册)",
          author: "陈磊·半小时漫画团队",
          recommend: "94.2%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/75/cpplatform_7eqrreg97tkvjleahhzspm/t6_cpplatform_7eqrreg97tkvjleahhzspm1683690681.jpg",
          numb: 2703,
        },
        {
          name: "人类简史：从动物到上帝",
          author: "尤瓦尔·赫拉利",
          recommend: "87.8%",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/37/YueWen_855812/t6_YueWen_855812.jpg",
          numb: 2369,
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
