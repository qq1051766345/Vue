<template>
    <div>
      <h2>Home组件内容</h2>
      <div>
        <ul class="nav nav-tabs">
          <li>
            <router-link 
              class="list-group-item" 
              active-class="active" 
              to="/home/news"
              >News
            </router-link>
          </li>
          <li>
            <router-link 
              class="list-group-item" 
              active-class="active" 
              to="/home/message"
              >Message
            </router-link
            >
          </li>
        </ul>
        <!-- include的值代表需要缓存的组件名 -->
        <!-- 缓存一个 -->
        <!-- <keep-alive include="News">
          <router-view></router-view>
        </keep-alive> -->

        <!-- 缓存多个 -->
        <keep-alive :include="['News','Message']">
          <router-view></router-view>
        </keep-alive>
      </div>
    </div>
</template>

<script>
export default {
  name: "Home",
  /* mounted(){
      console.log('Home组件挂载完毕了',this);
      window.homeRoute = this.$route;
      window.homeRouter = this.$router;
    } */
};
</script>

<style>
</style>