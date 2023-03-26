<script setup>
import{ref, reactive} from 'vue'
import Export from './Export.vue'
import Share from './Share.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
defineProps({
  msg: {
    type: String,
    required: true
  }
})
const name = ref('Joe')
</script>

<template>
  <div class="headermenu-start">
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="30" height="30" />
    <h2 class="blue">{{ msg }}</h2>
    <!-- <h3>
      For best team retrospective
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Docs</a> 
    </h3> -->
  </div>
  <div class="headermenu-end">
    <Export />
    <Share />
  </div>

</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.headermenu-start{
  height: 8vh;  
  /* border: 1px red solid; */
  display: flex;
  place-items: center;
}
.headermenu-end{
  display: flex;
  justify-content: right;
  height: 100%;  
  /* border: 1px red solid; */
  place-items: center;
  padding-right: 50px;
  gap: 15px;
}
.headermenu-init h1,
.headermenu-init h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .headermenu-init h1,
  .headermenu-init h3 {
    text-align: left;
  }
  .headermenu-start{
  height: 8vh;  
  /* border: 1px red solid; */
}
.headermenu-end{
  display: flex;
  justify-content: right;
  height: 100%;  
  /* border: 1px red solid; */
}
}
</style>
