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
  </div>
</template>
<style scoped>
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
}
.icon {
  width: 0.608rem;
  height: 0.608rem;
}
#header h5 {
  font-size: 0.544rem;
  text-align: center;
  line-height: 1.92rem;
}
#header input {
  width: 70%;
  height: 1.12rem;
  padding: 0 0.96rem;
  font-size: 0.512rem;
  margin-left: 0.8rem;
  border-radius: 0.64rem;
  border: none;
  outline: none;
  background-color: #f5f2f2;
}
#header a {
  position: absolute;
  top: 2.08rem;
  left: 0.992rem;
}
#main {
  width: 100%;
}
#nav li {
  float: left;
  text-align: center;
  width: 2.4rem;
  height: 0.8rem;
  font-size: 0.416rem;
  color: #777777;
  font-weight: bold;
}
#bookshelf {
  width: 90%;
  height: 4.8rem;
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
  width: 0.8rem;
  height: 0.8rem;
  border-radius: 50%;
  margin-left: 0.64rem;
  margin-top: 0.64rem;
  display: inline-block;
}
#bookshelf-title span {
  font-size: 0.448rem;
  color: #fff;
  position: absolute;
  top: 0.64rem;
  left: 1.76rem;
}
#bookshelf-title a {
  font-size: 0.384rem;
  position: absolute;
  top: 0.704rem;
  left: 3.84rem;
  color: gray;
}
#bookshelf-main img {
  width: 1.92rem;
  margin-left: 0.64rem;
  margin-top: 0.16rem;
}
#bookshelf-main span {
  width: 0.864rem;
  font-size: 0.448rem;
  float: right;
  margin-top: 0.704rem;
}
</style>
<script type="text/javascript">
(function () {
  var styleNode = document.createElement("style");
  var w = document.documentElement.clienwidth;
  var w = document.documentElement.clientWidth / 12;
  styleNode.innerHTML = "html{font-size:" + w + "px!important}";
  document.head.appendChild(styleNode);
})();
</script>
