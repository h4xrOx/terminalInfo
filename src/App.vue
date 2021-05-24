<template>
  <Header :info="info" />
  <Content/>
  <Link :info="info"/>
</template>

<script lang="ts">
import {defineComponent} from 'vue'
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import Link from './components/Link.vue'
export default defineComponent({
  name: 'App',
  components: {
    Header,Content,Link
  },
  setup(){
    const info = {
      title:"NaCo's Info - SSH root@nco.im",
      icon:[
        {name:"github",icon:"fa fa-github-square",url:"https://github.com/nacoliu"},
        {name:"group",icon:"fa fa-terminal",url:"https://github.com/asynsense"},
        {name:"steam",icon:"fa fa-steam-square",url:"https://steamcommunity.com/id/nacodes/"},
        {name:"ins",icon:"fa fa-instagram",url:"https://www.instagram.com/nacoliu/"},
      ]
    }

    return {
      info
    }
  }
})
</script>

<style lang="scss">
@import "https://fonts.googleapis.com/css?family=Noto+Sans+SC";
*{
  margin: 0;
  padding: 0;

}
body{
  display: flex;
  font-family: 'Noto Sans SC',"Comic Sans MS","Courier New",Courier,sans-serif;
  width: 100vw;
  height: 100vh;
  background: #262626;
  justify-content: center;
  align-items: center;
}
#app {
  display: flex;
  flex-direction: column;
  width: 80%;
  height: 500px;
  border-radius: 15px;
  margin: 0 auto;
  box-shadow: 30px 30px 30px rgba(0, 0, 0, 0.36);
  border: 1px solid rgba(0, 0, 0, 0.51);
  background: rgb(28, 28, 28);
  overflow: hidden;
}
textarea{
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0);
  border: none;
  border-radius: 0;
  outline: none;
  font-size: 12px;
  color:white;
  padding: 0 2px;
  font-family: "Courier New",sans-serif;
  box-sizing: content-box;
}
</style>
