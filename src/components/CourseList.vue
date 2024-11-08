<template>
  <div class="common-layout">
    <el-container>
      <el-header> <h1>找到适合您的学位</h1></el-header>
      <el-main>
        <!-- Flexbox container for alignment -->
        <div class="filter-row">
          <p>筛选依据</p>
          <el-select placeholder="级别计划" class="category-select"></el-select>
          <el-select placeholder="主题" class="category-select"></el-select>

          <!-- Align button to the right -->
          <el-button  type="primary" plain class="email-button"
            >通过电子邮件向我发送相关信息</el-button
          >
        </div>

        <!-- 学位列表 -->
        <div class="degrees">
          <el-card
            v-for="(degree, index) in degrees"
            :key="index"
            shadow="hover"
            class="degree-card"
          >
            <div slot="header" class="clearfix">
              <el-image
                :src="degree.logo"
                fit="cover"
                style="width: auto; height: auto;"
              ></el-image>
            </div>
            <p>{{ degree.university }}</p>
            <p>{{ degree.degreeName }}</p>
            <p>{{ degree.description }}</p>
            <p>
              <em>申请截止日期 {{ degree.applicationDeadline }}</em>
            </p>
          </el-card>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
import image from '@/assets/image.png';
export default {
  data() {
    return {
      degrees: [
        {
          logo: image, // 使用 require 语法引入图片
          university: 'University A',
          degreeName: 'Bachelor of Science',
          description: 'A science degree focusing on ...',
          applicationDeadline: '2024-12-01'
        },
        {
          logo: 'https://via.placeholder.com/150',
          university: 'University B',
          degreeName: 'Master of Arts',
          description: 'An arts degree focusing on ...',
          applicationDeadline: '2024-11-15'
        },
        {
          logo: 'https://via.placeholder.com/150',
          university: 'University B',
          degreeName: 'Master of Arts',
          description: 'An arts degree focusing on ...',
          applicationDeadline: '2024-11-15'
        },
        {
          logo: 'https://via.placeholder.com/150',
          university: 'University B',
          degreeName: 'Master of Arts',
          description: 'An arts degree focusing on ...',
          applicationDeadline: '2024-11-15'
        }
      ]
    };
  }
};
</script>

<style >

.filter-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.filter-row p {
  margin-right: 10px;
}

.category-select {
  margin-right: 10px;
  width: 200px;
}

.el-select__wrapper {
  box-shadow: 0 0 0 2px white !important;
}

.email-button {
  margin-left: auto;
}

/* Grid layout for the card container */
.degrees {
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* Four cards per row */
  gap: 20px; /* Spacing between cards */
  margin-top: 20px;
}

.degree-card {
  width: 100%;
}

.el-header h1 {
  padding-left: 10px;
  padding-top: 20px;
  color: black;
  font-size: 20px; /* 调整字体大小 */
}
</style>
