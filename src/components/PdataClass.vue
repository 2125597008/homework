<template>
  <div class="fenlei">
    <ul>
      <li v-for="(item, index) in arr" :key="index">
        <div class="left">
          <p class="title">{{ item.title }}</p>
          <p>1.{{ item.name1 }}</p>
          <p>2.{{ item.name2 }}</p>
          <p>3.{{ item.name3 }}</p>
        </div>
        <div class="right">
          <img :src="item.imgs" alt="" />
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [
        {
          title: "精品小说",
          name1: "长相思",
          name2: "剑来",
          name3: "三体（全集）",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/17/yuewen_23484983/t6_yuewen_234849831690286968.jpg",
        },
        {
          title: "历史",
          name1: "明朝那些事儿",
          name2: "长安的荔枝",
          name3: "翦商：殷周之变与华夏新生",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/61/YueWen_822995/t6_YueWen_822995.jpg",
        },
        {
          title: "文学",
          name1: "我与地坛",
          name2: "红楼梦",
          name3: "封神演义（中国古典文学名著）",
          imgs: "https://wfqqreader-1252317822.image.myqcloud.com/cover/44/674044/t6_674044.jpg",
        },
        {
          title: "艺术",
          name1: "生活蒙太奇",
          name2: "新摄影笔记",
          name3: "梵高手稿",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/84/YueWen_33514727/t6_YueWen_33514727.jpg",
        },
        {
          title: "人物传记",
          name1: "邓小平时代",
          name2: "苏东坡新传",
          name3: "毛泽东传（全6卷）",
          imgs: "https://wfqqreader-1252317822.image.myqcloud.com/cover/48/674048/t6_674048.jpg",
        },
        {
          title: "宗教哲学",
          name1: "道德经",
          name2: "图解易经",
          name3: "次第花开",
          imgs: "https://weread-1258476243.file.myqcloud.com/weread/cover/50/YueWen_832038/t6_YueWen_832038.jpg",
        },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
li {
  list-style: none;
}
a {
  text-decoration: none;
}
.fenlei {
  width: 92%;
  margin: auto;
}
.fenlei ul li {
  width: 100%;
  height: 170px;
  margin-top: 10%;
  display: flex;
  border-radius: 20px;
}
.fenlei ul li .left {
  width: 66%;
  height: 100%;
  background-color: #f1f1f1;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
  text-align: left;
  line-height: 30px;
}
.fenlei ul li .left .title {
  color: black;
  font-size: 20px;
  margin-left: 20px;
  margin-top: 20px;
}
.fenlei ul li .left p {
  margin-left: 20px;
  font-size: 14px;
  color: gray;
}
.fenlei ul li .right {
  width: 35%;
  height: 100%;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
}
.fenlei ul li img {
  width: 100%;
  height: 100%;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
}
</style>
