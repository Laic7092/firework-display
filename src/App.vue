<script setup lang="ts">
</script>

<template>
  <div>
    <article>
      <header>
        <h1>视频测试页面</h1>
      </header>
    </article>
    <main>
      <h2>webm格式</h2>
      <video controls width="250" playsinline="true" webkit-playsinline="true">
        <source src="/test.webm" type="video/webm" />
      </video>
      <h2>mp4格式</h2>
      <video controls width="250" playsinline="true" webkit-playsinline="true">
        <source src="/test1.mp4" type="video/mp4" />
      </video>
    </main>
  </div>
</template>