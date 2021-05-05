<template>
  <div id="app">
    <h1>💥 FOSS-POF (Free or Open Source Software Points Of Fail)</h1>
    <p>This is a simple app to self-analyse your Open Source Project and help you take the necessary measures to prevent it from being doomed to fail. <a href="https://github.com/s3rrot/foss-pof">Learn more</a></p>
    <list />
  </div>
</template>

<script>
import List from '@/components/list/List.vue'

export default {
  name: 'App',
  components: {
    List
  }
}
</script>
