<template>
  <div>
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
</template>
<script>
import fldata from "../components/Fldata.vue";
export default {
    name:'asdsadad'
    components{
      Fldata
    }
};
</script>
