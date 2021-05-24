<template>
  <el-row type="flex" class="row-bg" justify="">
    <el-col :span="8">
      <ul class="header-control">
        <li>
          <span></span>
        </li>
        <li></li>
        <li></li>
      </ul>
    </el-col>
    <el-col :span="8" class="title">
      <span>
       <img src="../assets/home.png" alt="{{info.title}}">{{info.title}}
      </span>
    </el-col>
    <el-col :span="8">
      <span></span>
    </el-col>
  </el-row>

</template>

<script lang="ts">
export default {
  name: "Header",
  props:['info']
}
</script>

<style lang="scss">
.el-row {
  color: white;
  padding: 5px;
  display: flex;
  align-items: center;
  background: rgb(60, 60, 60);

  ul {
    display: flex;

    li {
      list-style: none;
      width: 12px;
      height: 12px;
      margin: 0 4px;
      background: rgb(238, 105, 94);
      border-radius: 100%;
      cursor: pointer;

      &:first-child {
        display: flex;
        justify-content: center;
        align-items: center;

        span {
          width: 4px;
          height: 4px;
          border-radius: 100%;
          display: block;
          background: rgb(140, 26, 16);
        }
      }

      &:nth-child(2) {
        background: rgb(245, 189, 79);
      }

      &:last-child {
        background: rgb(98, 196, 84);
      }
    }


  }
  .title{
    display: flex;
    justify-content: center;
  }
  span {
    text-align: center;
    color:rgb(180,180,180);
    font-weight: 800;
    font-size: 13px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-shadow: 0 0 3px rgba(0, 0, 0, 0.18);
    img{
      width: 18px;
      margin-right: 10px;
    }
  }
}

</style>