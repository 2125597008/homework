<template>
  <div>
    <div id="header">
      <h5>微信读书</h5>
      <input type="text" name="" id="" placeholder="搜索" />
      <a
        ><svg
          t="1691067147570"
          class="icon"
          viewBox="0 0 1059 1024"
          version="1.1"
          xmlns="http://www.w3.org/2000/svg"
          p-id="1566"
          width="19"
          height="20"
        >
          <path
            d="M463.65500237 773.18500475a352.19666903 352.19666903 0 1 1 352.19666903-352.19666904 352.57094797 352.57094797 0 0 1-352.19666904 352.19666904z m0-641.95110188a289.81681265 289.81681265 0 1 0 289.81681265 289.81681266A290.12871176 290.12871176 0 0 0 463.65500237 131.23390287z"
            p-id="1567"
            fill="#515151"
          ></path>
          <path
            d="M952.6506972 912.47922422a31.18992819 31.18992819 0 0 1-21.77057017-8.85793963L679.61406566 657.96941048a31.18992819 31.18992819 0 0 1 43.66589914-44.60159729l251.26606138 245.65187411a31.18992819 31.18992819 0 0 1-21.83294917 53.52191674z"
            p-id="1568"
            fill="#515151"
          ></path></svg
      ></a>
    </div>
    <div id="main">
      <div id="bookshelf">
        <div id="bookshelf-title">
          <img
            src="https://dogefs.s3.ladydaily.com/~/source/wallhaven/small/gp/gp9god.jpg?w=400&h=200&fmt=webp"
            alt=""
          />
          <span>微信用户</span>
          <a>体验卡今日到期</a>
        </div>
        <div id="bookshelf-main">
          <img
            src="https://weread-1258476243.file.myqcloud.com/weread/cover/25/cpplatform_8numzl8erzinxvfsk3p9jv/t6_cpplatform_8numzl8erzinxvfsk3p9jv1685508354.jpg"
            alt=""
          />
          <span>
            <a>书架></a>
          </span>
        </div>
      </div>
      <div id="nav">
        <div id="app">
          <ul>
            <li
              v-for="(tab, index) in tabs"
              :key="index"
              @click="selectTab(index)"
              :class="{ active: selectedIndex === index }"
            >
              {{ tab.name }}
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div id="booklist">
      <ul>
        <li v-for="(item, index) in list" :key="index">
          <img :src="item.img" />
          <span id="ming">{{ item.title }}</span>
          <span id="zuo">{{ item.zuozhe }}</span>
          <span id="tui">{{ item.tuijian }}</span>
          <span id="du">{{ item.du }}</span>
        </li>
      </ul>
    </div>
    <fldata></fldata>
  </div>
</template>

<script>
import fldata from "../components/FdataView.vue";
export default {
  components: {
    fldata,
  },
  data() {
    return {
      tabs: [
        {
          name: "推荐",
        },
        {
          name: "分类",
        },
        {
          name: "排行",
        },
        {
          name: "文学艺术",
        },
        {
          name: "哲学社科",
        },
      ],
      list: [
        {
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/75/cpplatform_vkins1c9mzkmfbt3kjlrn9/t6_cpplatform_vkins1c9mzkmfbt3kjlrn91677476708.jpg",
          title: "长相思 (杨紫 张晚意 邓为 檀健...",
          zuozhe: "桐华 | 推荐值89.5%",
          du: "大家都在读",
        },
        {
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/43/cpplatform_uksuobynut7k8guvdp7jpb/t6_cpplatform_uksuobynut7k8guvdp7jpb1690794764.jpg",
          title: "长安的荔枝",
          zuozhe: "马伯谦 | 推荐值95.5%",
          du: "大家都在读",
        },
        {
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/39/cpplatform_uavwwbmcljz28lruduqj72/t6_cpplatform_uavwwbmcljz28lruduqj721690363640.jpg",
          title: "剑来(1-42)册 出版精校版",
          zuozhe: "烽火戏诸侯 | 推荐值80.8%",
          du: "大家都在读",
        },
        {
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/9/cpplatform_qdvo1xbxvdelziahxm5zem/t6_cpplatform_qdvo1xbxvdelziahxm5zem1690195117.jpg",
          title: "认知觉醒：开启自我的改变的原动力",
          zuozhe: "周玲 | 推荐值91.3%",
          du: "大家都在读",
        },
        {
          img: "https://wfqqreader-1252317822.image.myqcloud.com/cover/464/834464/t6_834464.jpg",
          title: "活着",
          zuozhe: "余华 | 推荐值91.9%",
          du: "大家都在读",
        },
        {
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/80/yuewen_695233/t6_yuewen_6952331677562148.jpg",
          title: "三体(全集）",
          zuozhe: "刘慈欣 | 推荐值93.4%",
          du: "大家都在读",
        },
        {
          img: "https://wfqqreader-1252317822.image.myqcloud.com/cover/385/25615385/t6_25615385.jpg",
          title: "被讨厌的勇气：“自我启发之父”阿德勒的哲学课",
          zuozhe: "岸见一郎 古贺史健 | 推荐值87.0%",
          du: "大家都在读",
        },
      ],
      selectedIndex: null,
    };
  },
  methods: {
    selectTab(index) {
      this.selectedIndex = index;
    },
  },
};
</script>
<style scoped>
#du {
  position: absolute;
  top: 65%;
  left: 23%;
  font-size: 1%;
  color: gray;
}

#tui {
  position: absolute;
  top: 45%;
  left: 36%;
  font-size: 1%;
  color: gray;
}

#zuo {
  position: absolute;
  top: 45%;
  left: 23%;
  font-size: 1%;
  color: gray;
  padding-right: 1%;
}

#ming {
  position: absolute;
  top: 20%;
  left: 23%;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

#booklist {
  width: 90%;
  margin-top: 10%;
  margin: auto;
}
#booklist li {
  width: 90%;
  height: 5%;
  position: relative;
}

#booklist img {
  width: 20%;
  height: 20%;
  margin-top: 5%;
  display: inline-block;
}

#booklist span {
  display: inline-block;
}
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
}
html {
  font-size: 26.78571429px;
}
#header {
  width: 100%;
  height: 3.84rem;
  position: relative;
  margin-bottom: 3%;
}
.icon {
  width: 60%;
  height: 60%;
}
#header h5 {
  font-size: 100%;
  text-align: center;
  line-height: 1.92rem;
}
#header input {
  width: 80%;
  height: 50%;
  padding: 0 0.96rem;
  font-size: 0.512rem;
  margin-left: 5%;
  border-radius: 0.64rem;
  border: none;
  outline: none;
  background-color: #f5f2f2;
}
#header a {
  position: absolute;
  top: 58%;
  left: 6%;
}
#main {
  width: 100%;
}
#nav {
  margin-bottom: 12%;
}
#nav li {
  float: left;
  text-align: center;
  width: 20%;
  height: 0.8rem;
  font-size: 0.416rem;
  color: #777777;
  font-weight: bold;
}
#bookshelf {
  width: 90%;
  height: 60%;
  margin: auto;
  background-color: #565860;
  border-radius: 0.64rem;
  margin-bottom: 0.64rem;
}
#bookshelf-title {
  width: 100%;
  height: 1.6rem;
  position: relative;
}
#bookshelf-title img {
  width: 1.4rem;
  height: 1.4rem;
  border-radius: 50%;
  margin-left: 0.64rem;
  margin-top: 0.64rem;
  display: inline-block;
}
#bookshelf-title span {
  font-size: 0.648rem;
  color: #fff;
  position: absolute;
  top: 0.84rem;
  left: 2.4rem;
}
#bookshelf-title a {
  font-size: 0.084rem;
  position: absolute;
  top: 0.804rem;
  left: 6rem;
  color: gray;
}
#bookshelf-main img {
  width: 15%;
  margin-left: 0.64rem;
  margin-top: 5%;
}
#bookshelf-main span {
  width: 0.864rem;
  font-size: 0.448rem;
  float: right;
  margin-top: 6%;
}
</style>
