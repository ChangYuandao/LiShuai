<template>
  <div class="top-nav">
    <!-- 左边的 Logo 和选择框、搜索框 -->
    <div class="left-section">
      <div class="logo">
        <img src="/src/assets/coursera-vector-logo-2022.png" alt="Logo" />
      </div>

      <div class="center-section">
        <el-select placeholder="探索" class="category-select">
        </el-select>

        <el-input placeholder="您想学习什么？" class="search-input" clearable>
          <template #append>
            <el-button type="primary" class="search-button" circle>
              <el-icon><Search /></el-icon>
            </el-button>
          </template>
        </el-input>
      </div>
    </div>

    <!-- 右边的菜单和按钮 -->
    <div class="right-section">
      <span class="menu-item">在线学习</span>
      <span class="menu-item">工作机会</span>
      <span class="menu-item login-item">登录</span>

      <el-button type="primary" class="join-button">免费加入</el-button>
    </div>
  </div>
</template>


<script>
import { Search } from "@element-plus/icons-vue";

export default {
  components: {
    Search,
  },
};
</script>

<style scoped>
.top-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 100%;
  padding: 0 20px;
  overflow: hidden;
}

.left-section {
  display: flex;
  align-items: center;
}

.logo img {
  height: 40px;
}

.center-section {
  display: flex;
  align-items: center;
  gap: 10px; /* 控制选择框和搜索框之间的间距 */
  margin-left: 20px; /* 调整与 Logo 的间距 */
}

.category-select,
.search-input {
  width: 200px;
}

.right-section {
  display: flex;
  align-items: center;
  gap: 20px;
}

.menu-item {
  cursor: pointer;
}

.join-button {
  margin-left: 10px;
}
</style>
