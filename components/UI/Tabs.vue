<script setup>
import { ref, computed } from "vue";
const props = defineProps(["tabList"]);
const activeTab = ref(0);

const activateTab = (index) => {
  activeTab.value = activeTab.value === index ? null : index;
};

let isFalse = ref(false);


</script>
<template>
  <div class="tabs-container">
    <div class="tab-size">
      <div v-for="(tab, index) in props.tabList"
           :key="index"
           @click="activateTab(index)"
           :class="{ 'active': activeTab === index }" class="tab">
        <img :src="tab.icon" class="tab-icon" v-if="tab.icon" alt="tab-icons">
        <h1>{{ tab.label }}</h1>
      </div>
    </div>

    <div class="content">
      <div v-if="activeTab !== null">
        <div v-if="tabList[activeTab].label === 'Education'" class="education-content">
          <EducationItems :info="tabList[activeTab].content" />
        </div>
        <div v-else class="cool">
          <div v-for="(item, i) in tabList[activeTab].content" :key="i" class="item">
            <ProjectsItems v-if="tabList[activeTab].label === 'Projects'" :info="item" />
            <ExperienceItems v-else-if="tabList[activeTab].label === 'Experience'" :info="item" />
            <AboutItems v-else-if="tabList[activeTab].label=== 'About'" :info="item" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.tabs-container {
  width: 100%;
}
.tab-size {
  border-radius: 2px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  max-width: 40rem;
  margin: 0 auto;
}

.tab-icon {
  margin: 0.4rem auto;
  height: 2rem;
}

.cool {
  width: 95%;
  margin: 0 auto;
}

.content {
  margin: 2rem auto;
  max-width: 48rem;

  align-items: center;

  /* border: solid red 1px; */
}

.tab {
  color: #cacaca;
  width: 90%;
  cursor: pointer;
  padding: 8px 10px;
  margin: 5px 3px;
  transition: background-color 0.3s ease;
  text-align: center;
}

.tab:hover {
  background-color: rgba(255, 255, 255, 0.3);
  color: #61dbfb;
  border-radius: 5px;
}

.tab.active {
  background-color: rgba(255, 255, 255, 0.3);
  opacity: 0.7;
  border-radius: 5px;
  color: #61dbfb;
}

.tab-content {
  display: flex;
  flex-direction: column;

  margin: 1.5rem auto;
  height: 60vh;
  border-radius: 0 0 5px 5px;
}

@media only screen and (max-width: 768px) {
  .cool {
    width: 98%;
    margin: 0 auto;
    padding: 0;
  }
}
</style>
