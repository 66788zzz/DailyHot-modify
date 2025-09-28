<!-- src/components/Footer.vue -->
<template>
  <footer>
    <div class="copyright">
      <span class="own-by">
        Own By
        <a class="link" target="_blank" href="https://ios1.top">Simple</a>
        | Contact Me By
        <a class="link" href="mailto:simple@ios1.top">Email</a>
      </span>
    </div>

    <div class="copyright">
      <span class="description">今日热榜</span>
      <a class="link author" target="_blank" href="https://github.com/imsyy">
        @ License By imsyy
      </a>
    </div>
  </footer>
</template>

<script setup>
// 纯静态，不写 package.json 也不写 ref
const jumpLink = (url) => window.open(url, '_blank')
</script>

<style scoped>
footer {
  height: 100px;
  padding: 0 5vw;
  max-width: 1800px;
  margin: 20px auto 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  color: var(--n-text-color-base);   /* 普通文字颜色 */
}

.copyright {
  margin-bottom: 4px;
}

/* 普通文字 */
.description {
  color: var(--n-text-color-base);
}

/* 链接文字：默认亮蓝色 */
.link {
  color: #409eff;          /* Element 蓝，可换成任意色 */
  text-decoration: none;    /* 去掉下划线 */
  cursor: pointer;          /* 手型光标 */
  margin: 0 4px;
  transition: color 0.3s;
}

/* 悬停时变色 */
.link:hover {
  color: #79bbff;           /* 悬停更亮 */
}
</style>
