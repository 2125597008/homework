<template>
  <div class="ranking">
    <ul>
      <li v-for="(item, index) in arr" :key="index">
        <div class="cont">
          <div class="icon">
            <img :src="item.icon" alt="" />
          </div>
          <div class="list">
            <div class="book">
              <img :src="item.img1" alt="" />
              <p>1 {{ item.name1 }}</p>
              <span>{{ item.author1 }}</span>
            </div>
            <div class="book">
              <img :src="item.img2" alt="" />
              <p>2 {{ item.name2 }}</p>
              <span>{{ item.author2 }}</span>
            </div>
            <div class="book">
              <img :src="item.img3" alt="" />
              <p>3 {{ item.name3 }}</p>
              <span>{{ item.author3 }}</span>
            </div>
            <div class="book">
              <img :src="item.img4" alt="" />
              <p>4 {{ item.name4 }}</p>
              <span>{{ item.author4 }}</span>
            </div>
          </div>
          <div class="bun">
            <button>查看全部</button>
          </div>
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
          icon: "https://weread-1258476243.file.myqcloud.com/assets/ranklist.rising.chart_title.YqPFOS9Gin.png",
          name1: "让人拍案叫绝的中国史（套装共2册）",
          author1: "渤海小史",
          img1: "https://weread-1258476243.file.myqcloud.com/weread/cover/67/YueWen_36235932/t6_YueWen_36235932.jpg",
          name2: "生活即禅，笑看平凡",
          author2: "林帝浣",
          img2: "https://weread-1258476243.file.myqcloud.com/weread/cover/98/cpPlatform_3300025251/t6_cpPlatform_3300025251.jpg",
          name3: "资本的秘密",
          author3: "赫尔南多",
          img3: "https://weread-1258476243.file.myqcloud.com/weread/cover/25/cpplatform_8numzl8erzinxvfsk3p9jv/t6_cpplatform_8numzl8erzinxvfsk3p9jv1685508354.jpg",
          name4: "大汉帝国全史",
          author4: "上医治国",
          img4: "https://weread-1258476243.file.myqcloud.com/weread/cover/79/cpplatform_2rqinjd9n9aycpp7emxrg1/t6_cpplatform_2rqinjd9n9aycpp7emxrg11691045643.jpg",
        },
        {
          icon: "https://weread-1258476243.file.myqcloud.com/assets/ranklist.newbook.chart_title.GWZVW5nl3Z.png",
          name1: "法医秦明：白卷",
          author1: "法医秦明",
          img1: "https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_2thuj2jlv1odkiylmdlcjr/t6_cpplatform_2thuj2jlv1odkiylmdlcjr1689825647.jpg",
          name2: "宋慈洗冤笔记（独家首发｜1-3册）",
          author2: "巫童",
          img2: "https://weread-1258476243.file.myqcloud.com/weread/cover/95/cpplatform_bxra3sweeea8uuujb6jghh/t6_cpplatform_bxra3sweeea8uuujb6jghh1689755652.jpg",
          name3: "挣脱（独家首发｜一个律师的女性辩护记录）",
          author3: "刘任侠",
          img3: "https://weread-1258476243.file.myqcloud.com/weread/cover/9/cpplatform_ffxxfh9zishrhh1gdece8z/t6_cpplatform_ffxxfh9zishrhh1gdece8z1690196853.jpg",
          name4: "饮鸩（独家首发）",
          author4: "一枚铜钱",
          img4: "https://weread-1258476243.file.myqcloud.com/weread/cover/39/cpplatform_uavwwbmcljz28lruduqj72/t6_cpplatform_uavwwbmcljz28lruduqj721690363640.jpg",
        },
        {
          icon: "https://weread-1258476243.file.myqcloud.com/assets/ranklist.all.chart_title.JPnYFfuPbm.png",
          name1: "长安的荔枝",
          author1: "马伯庸",
          img1: "https://weread-1258476243.file.myqcloud.com/weread/cover/75/cpPlatform_dbb14284a55f1e733b60202b0777255d/t6_cpPlatform_dbb14284a55f1e733b60202b0777255d.jpg",
          name2: "三体",
          author2: "刘慈欣",
          img2: "https://weread-1258476243.file.myqcloud.com/weread/cover/80/yuewen_695233/t6_yuewen_6952331677562148.jpg",
          name3: "明朝那些事儿",
          author3: "当年明月",
          img3: "https://weread-1258476243.file.myqcloud.com/weread/cover/61/YueWen_822995/t6_YueWen_822995.jpg",
          name4: "活着",
          author4: "余华",
          img4: "https://wfqqreader-1252317822.image.myqcloud.com/cover/464/834464/t6_834464.jpg",
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
.ranking ul li {
  margin-top: 20px;
}
.ranking ul li img {
  width: 50px;
}
.ranking ul li .cont {
  width: 100%;
}
.ranking ul li .cont .icon {
  height: 50px;
}
.ranking ul li .cont .icon img {
  width: 250px;
  height: 30px;
}
.ranking ul li .cont .list {
  display: flex;
  flex-wrap: wrap;
}
.ranking ul li .cont .list .book {
  width: 50%;
  height: 100px;
  margin-top: 10px;
  font-size: 14px;
}
.ranking ul li .cont .list .book img {
  height: 100%;
  width: 40%;
  float: left;
  margin-right: 10px;
}
.ranking ul li .cont .list .book p {
  margin-top: 20px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.ranking ul li .cont .list .book span {
  display: inline-block;
  color: gray;
  margin-top: 10px;
}
.ranking ul li .cont .bun {
  height: 50px;
  text-align: center;
  line-height: 50px;
  margin-top: 30px;
}
.ranking ul li .cont .bun button {
  height: 40px;
  width: 90%;
  border-radius: 10px;
  border: none;
  color: gray;
  font-size: 15px;
}
</style>
