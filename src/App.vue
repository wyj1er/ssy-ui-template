<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import { Button } from 'ssy-ui-vite';
</script>

<template>
  <header>
    <div class="container">
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
      <div class="content">
        <HelloWorld msg="You did it!" />
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </nav>
      </div>
    </div>
    <section>
      <h2>示例组件</h2>
      <div class="button-group">
        <SButton color="blue">主要按钮</SButton>
        <SButton color="green">绿色按钮</SButton>
        <SButton color="gray">灰色按钮</SButton>
        <SButton color="yellow">黄色按钮</SButton>
        <SButton color="red">红色按钮</SButton>
      </div>
      <div class="button-group">
        <SButton color="blue" plain>朴素按钮</SButton>
        <SButton color="green" plain>绿色按钮</SButton>
        <SButton color="gray" plain>灰色按钮</SButton>
        <SButton color="yellow" plain>黄色按钮</SButton>
        <SButton color="red" plain>红色按钮</SButton>
      </div>
      <div class="button-group">
        <SButton size="small" plain>小按钮</SButton>
        <SButton size="medium" plain>中按钮</SButton>
        <SButton size="large" plain>大按钮</SButton>
      </div>
      <div class="button-group">
        <SButton color="blue" round plain>搜索按钮</SButton>
        <SButton color="green" round plain>编辑按钮</SButton>
        <SButton color="gray" round plain>成功按钮</SButton>
        <SButton color="yellow" round plain>提示按钮</SButton>
        <SButton color="red" round plain>删除按钮</SButton>
      </div>
    </section>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  background-color: #f5f5f5;
  padding: 2rem 0;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 1rem;
}

.logo {
  display: block;
  margin-right: 2rem;
}

.content {
  flex: 1;
  text-align: left;
}

nav {
  margin-top: 1rem;
  font-size: 14px;
}

nav a {
  display: inline-block;
  padding: 0.5rem 1rem;
  margin-right: 1rem;
  color: #333;
  text-decoration: none;
  border-radius: 4px;
  transition: background-color 0.3s;
}

nav a.router-link-exact-active {
  background-color: #007bff;
  color: white;
}

nav a:hover {
  background-color: #f0f0f0;
}

section {
  max-width: 1200px;
  margin: 2rem auto;
  padding: 0 1rem;
}

.button-group {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 2rem;
}

.button-group>* {
  flex-shrink: 0;
}

@media (max-width: 768px) {
  header {
    flex-direction: column;
    align-items: center;
  }

  .logo {
    margin-bottom: 1rem;
  }

  .content {
    text-align: center;
  }

  nav {
    margin-top: 1rem;
  }

  nav a {
    margin-right: 0.5rem;
  }

  .button-group {
    flex-wrap: wrap;
  }
}
</style>
