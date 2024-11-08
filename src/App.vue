<template>
  <div class="common-layout">
    <el-container class="layout-container">
      <el-header class="layout-header">
        <TopNav />
      </el-header>
      <el-main class="layout-main">
        <Title />
      </el-main>
      <el-footer class="layout-footer">
        <CourseList />
      </el-footer>
    </el-container>
  </div>
</template>

<script>
import TopNav from "./components/TopNav.vue";
import Title from "./components/Title.vue";
import CourseList from "./components/CourseList.vue";

export default {
  components: {
    TopNav,
    Title,
    CourseList,
  },
};
</script>

<style>
html, body {
  padding: 0;
  margin: 0;
}

.layout-main {
  padding: 0
}

</style>
