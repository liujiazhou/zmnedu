<script setup lang="ts">
// 简化脚本，移除动画逻辑
</script>

<template>
  <div class="welcome-container">
    <div class="glass-buttons">
      <a href="http://110.41.58.71/home" target="_blank" class="glass-button student-button">
        <div class="button-content">
          <div class="button-icon">👨‍🎓</div>
          <h2>啄木鸟OJ系统</h2>
          <p>在线刷题、作业提交、专项练习</p>
        </div>
      </a>
      
      <a href="https://dz.zmnedu.cc" target="_blank" class="glass-button teacher-button">
        <div class="button-content">
          <div class="button-icon">⌨️</div>
          <h2>啄木鸟打字</h2>
          <p>指法训练、代码记忆、单词学习</p>
        </div>
      </a>
    </div>
  </div>
</template>

<style scoped>
.welcome-container {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0;
  margin: 0;
  background: #e6f7ff; /* 纯色背景 */
  overflow: hidden;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

.glass-buttons {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 1200px;
  z-index: 1;
}

.glass-button {
  position: relative;
  width: 300px;
  height: 300px;
  background: rgba(255, 255, 255, 0.4);
  border-radius: 20px;
  backdrop-filter: blur(8px);
  border: 2px solid rgba(255, 255, 255, 0.7);
  box-shadow: 0 10px 40px rgba(31, 38, 135, 0.2);
  transition: all 0.3s ease;
  overflow: hidden;
  text-decoration: none;
  color: #1a1a1a;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 500;
}

.glass-button:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 50px rgba(31, 38, 135, 0.25);
  border: 2px solid rgba(255, 255, 255, 0.9);
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
  background: linear-gradient(45deg, #90caf9, #42a5f5, #1e88e5); /* 清新明亮的蓝色渐变 */
  background-size: 200% 200%;
  animation: gradientShift 8s ease infinite;
}

.teacher-button::before {
  background: linear-gradient(45deg, #b39ddb, #9575cd, #7986cb); /* 柔和带蓝紫色过渡的渐变 */
  background-size: 200% 200%;
  animation: gradientShift 8s ease infinite;
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
  color: #1a1a1a;
  font-weight: 600;
}

p {
  margin: 0;
  opacity: 0.9;
  font-size: 1rem;
  color: #333333;
  font-weight: 500;
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

@keyframes gradientShift {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
</style>
