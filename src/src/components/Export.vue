<template>
   <button @click="pdf">Exportar</button>
   <i >
      <slot name="icon"></slot>
    </i> 
</template>

<script>
export default{
    name:'Export',
    data(){
        return{
        msgTudo:"Tudo nosso"
        }
    },
    methods:{
        pdf(event){
            alert('exporting');
        }
    }
}
</script>
<style>
button{
    height: 50px;
    width:100px;
}
i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }
</style>