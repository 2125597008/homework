<template>
  <div id="box1">
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
  </div>
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
<script type="text/javascript">
(function () {
  var styleNode = document.createElement("style");
  var w = document.documentElement.clienwidth;
  var w = document.documentElement.clientWidth / 12;
  styleNode.innerHTML = "html{font-size:" + w + "px!important}";
  document.head.appendChild(styleNode);
})();
</script>
