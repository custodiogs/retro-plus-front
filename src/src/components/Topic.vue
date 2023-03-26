<script setup>
import Card from './Card.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
import{ref, reactive} from 'vue'


defineProps({
  title: {
    type: String,
    required: true
  },
  // return(){
  //   cards:[
  //    {text:'Precisamos melhor nessse e naquele ponto...',votes:1},
  //    {text:'Precisamos melhor nessse e naquele ponto...',votes:0},
  //    {text:'Precisamos melhor nessse e naquele ponto...',votes:1},
  //    {text:'Precisamos melhor nessse e naquele ponto...',votes:3},
  //    {text:'Precisamos melhor nessse e naquele ponto...',votes:1},
  //    {text:'Fomos bem ao preparar a documentação no início da sprint...',votes:6}
  //   ]
  // }
})

const cards = ref([
     {text:'Precisamos melhor nessse e naquele ponto...',votes:1},
     {text:'Precisamos melhor nessse e naquele ponto...',votes:0},
     {text:'Precisamos melhor nessse e naquele ponto...',votes:1},
     {text:'Precisamos melhor nessse e naquele ponto...',votes:3},
     {text:'Precisamos melhor nessse e naquele ponto...',votes:1},
     {text:'Fomos bem ao preparar a documentação no início da sprint...',votes:6}
    ])


</script>

<template>
  <div class="topic-header">
    <b>{{title}}</b>
  </div>
  <Card  v-for="card in cards">
    <template #icon>
      <DocumentationIcon />
    </template>
    {{ card.text }}
  </Card>

</template>

<style>
.topic-header{
  max-width: 400px;
  height: 40px;
  max-height: 40px;
  align-content: center;
  background-color: #f1f1f1;
  padding:5px;  
  border-radius: 5px;
  font-size: 1.2em;
  color: steelblue;
}
h2{
  padding: 0px;
}
</style>
