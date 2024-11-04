<script setup lang="ts">
import { ref } from 'vue';

const show = ref(false);
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
      <video controls width="320" playsinline="true" webkit-playsinline="true" preload="metadata">
        <source src="/flower.webm" type="video/webm" />
      </video>
      <h2>mp4格式</h2>
      <video controls width="320" playsinline="true" webkit-playsinline="true" preload="metadata">
        <source src="/flower.mp4" type="video/mp4" />
      </video>
      <template v-if="show">
        <h2>短视频(mp4)</h2>
        <video controls width="320" playsinline="true" webkit-playsinline="true" preload="metadata">
          <source src="/big.mp4#t=0.01" type="video/mp4" />
        </video>
        <h2>中长视频(mp4)</h2>
        <video controls width="320" playsinline="true" webkit-playsinline="true" preload="metadata"
          poster="/poster.png">
          <source src="/biger.mp4" type="video/mp4" />
        </video>
      </template>
      <div v-else style="padding: 2em;">
        <input type="button" value="展示更多" @click="show = true"
          style="font-size: 1.2rem;padding: 1em 2em;border-radius: 4px;border: none;" />
      </div>
      <footer>
        <div>
          <ul>
            <li>
              在safari浏览器(webkit内核) 的 video 播放，需要设置 poster 属性，否则会显示空白。
            </li>
          </ul>
        </div>
      </footer>
    </main>
  </div>
</template>