<template>
  <div>
    <ul class="link">
      <li v-for="(item) in info.icon"><a :href="item.url" target="_blank" :title="item.name"><i :class="item.icon" aria-hidden="true"></i></a></li>
    </ul>
  </div>
</template>

<script lang="ts">
export default {
  name: "Link",
  props:['info']

}
</script>

<style lang="scss">
.link {
  width: 100%;
  font-size: 35px;
  padding: 10px;
  box-sizing: border-box;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  background: rgba(0, 0, 0, 0.54);
  color: white;
  list-style: none;
  backdrop-filter: blur(10px);

  li {
    padding: 0 20px;
  }

  a {
    color: white;
  }
}
</style>