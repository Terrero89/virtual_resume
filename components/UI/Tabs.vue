<script setup>
import { ref, watch } from "vue";
const props = defineProps(["tabList"]);
const activeTab = ref(0);
const direction = ref('slide-right');

const activateTab = (index) => {
  // Determine the direction of the slide
  direction.value = index > activeTab.value ? 'slide-left' : 'slide-right';
  activeTab.value = activeTab.value === index ? null : index;
};

// Watch for changes in activeTab to apply the correct direction
watch(activeTab, (newVal, oldVal) => {
  direction.value = newVal > oldVal ? 'slide-left' : 'slide-right';
});
</script>

<template>
  <div class="tabs-container">
    <div class="tab-size">
      <div v-for="(tab, index) in props.tabList"
           :key="index"
           @click="activateTab(index)"
           :class="{ 'active': activeTab === index }" class="tab">
        <img :src="tab.icon" class="tab-icon" v-if="tab.icon" :alt="tab.iuco">
        <h1>{{ tab.label }}</h1>
      </div>
    </div>

    <div class="content">
      <transition :name="direction" mode="out-in">
        <div v-if="activeTab !== null" :key="activeTab">
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
      </transition>
    </div>
  </div>
</template>

<style scoped>
.tab h1 {
  text-transform: uppercase;
  font-size: 0.8em;
  font-weight: 700;
}

.tabs-container {
  width: 100%;
}

.tab-size {
  border-radius: 2px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  max-width: 44rem;
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
  overflow: hidden;
  position: relative;
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
  color: #02d5fa;
  border-radius: 5px;
}

.tab.active {
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 5px;
  color: #02d5fa;
}

.tab-content {
  display: flex;
  flex-direction: column;
  margin: 1.5rem auto;
  height: 60vh;
  border-radius: 0 0 5px 5px;
}

.slide-left-enter-active,
.slide-left-leave-active,
.slide-right-enter-active,
.slide-right-leave-active {
  transition: all 0.2s;
}

.slide-left-enter-from {
  opacity: 0;
  transform: translate(50px, 0);
}

.slide-left-leave-to {
  opacity: 0;
  transform: translate(-50px, 0);
}

.slide-right-enter-from {
  opacity: 0;
  transform: translate(-50px, 0);
}

.slide-right-leave-to {
  opacity: 0;
  transform: translate(50px, 0);
}

@media only screen and (max-width: 768px) {
  .cool {
    width: 100%;
    margin: 0 auto;
    padding: 0;
  }
}
</style>
