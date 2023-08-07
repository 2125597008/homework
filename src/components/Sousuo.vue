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
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
#header {
  width: 100%;
  height: 3.84rem;
  position: relative;
  margin-bottom: 3%;
  position: sticky;
  top: 0;
  background: white;
  z-index: 1;
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
</style>
