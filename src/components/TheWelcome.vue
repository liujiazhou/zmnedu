<script setup lang="ts">
// 不再需要RouterLink
</script>

<template>
  <div class="welcome-container">
    <div class="glass-buttons">
      <a href="http://110.41.58.71/home" target="_blank" class="glass-button student-button">
        <div class="button-content">
          <div class="button-icon">👨‍🎓</div>
          <h2>啄木鸟OJ系统</h2>
          <p>查看课程、完成作业、参与讨论</p>
        </div>
      </a>
      
      <a href="https://dz.zmnedu.cc" target="_blank" class="glass-button teacher-button">
        <div class="button-content">
          <div class="button-icon">👩‍🏫</div>
          <h2>啄木鸟打字</h2>
          <p>管理课程、批改作业、查看统计</p>
        </div>
      </a>
    </div>
  </div>
</template>

<style scoped>
.welcome-container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  background: linear-gradient(135deg, #6e8efb, #a777e3);
}

.glass-buttons {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 1200px;
}

.glass-button {
  position: relative;
  width: 300px;
  height: 300px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 20px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  box-shadow: 0 8px 32px rgba(31, 38, 135, 0.2);
  transition: all 0.3s ease;
  overflow: hidden;
  text-decoration: none;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 500;
}

.glass-button:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(31, 38, 135, 0.3);
  border: 1px solid rgba(255, 255, 255, 0.6);
}

.glass-button::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
  border-radius: 20px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.student-button::before {
  background: linear-gradient(45deg, #4776E6, #8E54E9);
}

.teacher-button::before {
  background: linear-gradient(45deg, #FF512F, #DD2476);
}

.glass-button:hover::before {
  opacity: 1;
}

.button-content {
  text-align: center;
  padding: 2rem;
}

.button-icon {
  font-size: 4rem;
  margin-bottom: 1rem;
}

h2 {
  margin: 0.5rem 0;
  font-size: 1.8rem;
}

p {
  margin: 0;
  opacity: 0.9;
  font-size: 1rem;
}

@media (max-width: 700px) {
  .glass-buttons {
    flex-direction: column;
    align-items: center;
  }
  
  .glass-button {
    width: 100%;
    max-width: 300px;
    height: 250px;
  }
}
</style>
