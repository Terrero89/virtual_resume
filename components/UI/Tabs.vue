<script setup>
import {ref} from 'vue';

const activeTab = ref(0);

const activateTab = (index) => {
  activeTab.value = activeTab.value === index ? null : index;
};


let ShowArrowSign = ref(true)

const tabs = ref([
  {
    label: 'About',
    content: [{
      header: 'About me',
      sub: "part of my story",
      text: ' is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the ' +
          'industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of ' +
          'type and scrambled it to make a type specimen book. It has survived not only five centuries, but ' +
          'also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in ' +' is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the ' +
          'industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of ' +
          'type and scrambled it to make a type specimen book. It has survived not only five centuries, but ' +
          'also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in ' +
       'sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.'
    }]
  },
  {
    label: 'Education', content: [{
      degree: 'Computer Science',
      school: 'Quincy College',
      year: '2018-2020',
      grad: true,

    }, {
      degree: 'Information Techonology',
      school: 'Umass Boston ',
      year: '2020-2023',
      grad: true,

    }]
  },

  {label: 'Skills', content: [{tech: ["Go", "Vue", "React", "Node", "Express", "Mongoose"]}]},
  {
    label: 'Projects',
    content: [
      {
        project: 'Payment UI',
        year: '2020',
        description: '',
        technology: ['Go, Vue', 'React']
      },
      {
        project: 'Foodie App',
        year: '2021',
        description: '',
        technology: ['Node', 'React', 'Express', "Mongoose", "MongoDB",]
      }, {
        project: 'Airplane App',
        year: '2021',
        description: '',
        technology: ['Node', 'React', 'Express', "Mongoose", "MongoDB",]
      },
      {
        project: 'Card Payment UI',
        year: '2024',
        technology: ['Node', 'React', 'Express', "Mongoose", "MongoDB",]
      }]
  },

]);


const filteredTabs = computed(() => tabs.value.map((item) => item.content.value))

</script>


<template>
  <div class="tabs-container vertical">
    <div class="tab-size">
      <div v-for="(tab, index) in tabs" :key="index" @click="activateTab(index)"
           :class="{ 'active': activeTab === index }" class="tab ">
        {{ tab.label }}

      </div>

    </div>
<!--    <div v-if="activeTab !== null" class="tab-content">-->

      <UCarousel v-slot="{ item, n }" :items="tabs[activeTab].content" :ui="{ item: 'basis-full' }"
                 class="rounded-lg cool"
                 indicators draggable="true">
        <div class="content">

          <EducationItems :info="item"/>
          <ProjectsItems :info="item"/>
          <SkillsItems :info="item"/>
          <AboutItems :info="item"/>

        </div>
      </UCarousel>

    </div>
<!--  </div>-->
</template>


<style scoped>
.cool {
  height: 70%;
  /*border: solid #e3e3e5 1px;*/
  width: 90%;
  margin: 0 auto;


}

.content {
  margin: 0 auto;
  align-content: center;
  align-items: center;
  display: flex;
  justify-content: center;
  min-height: 15rem;


}

.tabs-container {
  width: 100%;
}

.tab-size {

  border-radius: 2px;

  display: flex;

  flex-direction: row;
  min-width: 100%;

}


.tab {
  color: #cacaca;
  width: 100%;
  cursor: pointer;
  padding: 8px 10px;
  margin: 5px 0;
  transition: background-color 0.3s ease;
  text-align: center;
}

.tab:hover {
  background-color: #36373f;
  color: #61DBFB;
}

.tab.active {
  background-color: #36373f;
  border-radius: 5px;
  color: #61DBFB;


}

.tab-content {
  display: flex;
  flex-direction: column;
 /* justify-content: center; when bigger */
  justify-content: center;
  border: solid 1px red;
  padding: 10px;


  margin: 2rem auto;
  height: 60vh;
  border-radius: 0 0 5px 5px;
  //display: block;
}

@media only screen and (min-width: 1080px) {
  .tab {

  }
}
</style>
