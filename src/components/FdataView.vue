<template>
  <div id="booklist">
    <ul>
      <li v-for="(item, index) in list" :key="index">
        <img :src="item.img" />
        <span id="ming">{{ item.title }}</span>
        <span id="zuo">{{ item.zuozhe }}</span>
        <span id="du">{{ item.du }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/75/cpplatform_vkins1c9mzkmfbt3kjlrn9/t6_cpplatform_vkins1c9mzkmfbt3kjlrn91677476708.jpg",
          title: "长相思 (杨紫 张晚意 邓为 檀健次",
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
    };
  },
  methods: {},
};
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
}
#booklist {
  width: 90%;
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
  margin-top: 8%;
  display: inline-block;
}

#booklist span {
  display: inline-block;
}
#du {
  position: absolute;
  top: 70%;
  left: 23%;
  font-size: 1%;
  color: gray;
}

#zuo {
  position: absolute;
  top: 52%;
  left: 23%;
  font-size: 1%;
  color: gray;
}

#ming {
  width: 75%;
  position: absolute;
  top: 30%;
  left: 23%;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
