<template>
    <div class="Content" contenteditable="true">
      <div class="welcome">Last login: {{updateTime}} on NaCo's Info</div>
        <br>
        <p>~bash: ./GetInfo.sh -User NaCo</p>
        <ul class="info">
          <li>name: NaCo</li>
          <li>age: 21</li>
          <li>email: naco@nco.im</li>
          <li>Skill: Flutter / JavaScript / NodeJs / PHP / Mysql</li>
        </ul>
      <br>
      <p>~bash: ./GetInfo.sh -project NaCo</p>
      <ul class="info">
        <li>github: https://github.com/nacoliu</li>
        <li>team: https://www.asynsense.com</li>
      </ul>
    </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue'
  export default defineComponent({
    name:"Content",
    setup(){
      const nowDate = new Date();
      const date = {
        year: nowDate.getFullYear(),
        month: nowDate.getMonth() + 1,
        date: nowDate.getDate(),
      }
      const newMonth = date.month>10?date.month:'0'+date.month
      const day = date.date>10?date.date:'0'+date.date
      let updateTime = date.year + '/' + newMonth + '/' + day

      return{
        updateTime
      }
    }
  })
</script>

<style lang="scss">
  .Content{
    height: 100%;
    outline: none;
    padding: 5px;
    font-family:"Courier",sans-serif;
    color:white;
    font-size: 13px;
    *{
      line-height: 18px;
    }
  }
</style>