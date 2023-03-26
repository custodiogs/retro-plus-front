<script setup>
import{ref, reactive} from 'vue'
import Topic from './Topic.vue'
defineProps({
  // title: {
  //   type: String,
  //   required: true
  // }
})
const topics = ref([
{text:'Went Well'},
{text:'To Improve'},
{text:'Action Items'},
{text:'New'}
])
</script>

<template>
  <!-- <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      For best team retrospective
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Docs</a> 
    </h3>
  </div> -->
    <!-- {{ topics.lenth }} -->
      <div class="board">
    <template v-for="topic in topics">    
      <div class="board-column">
      <Topic :title="topic.text" />    
    </div>
    </template> 
  </div>
    <!-- <div v-for="topic in topics">
      {{ topic.text }}
      <Topic  /> 
    </div>     -->
</template>

<style scoped>
.board{
display: flex;
flex-direction: row;
justify-content: flex-start;
align-items: stretch;
gap: 30px;
}
.board-column{
  min-width: 400px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
