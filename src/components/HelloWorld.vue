<template>
  <div>
    <h1>Hello Forum</h1>
    <div v-for="(thread, index) in threads" :key="index">
      <h2>{{thread.name}}</h2>
      <div v-for="(postId, index) in thread.posts" :key="index">
        <p>{{posts[postId].text}}</p>
      </div>
    </div>
  </div>
</template>

<script>
import sourceDate from '@/data'
export default {
  name: 'HelloWorld',
  data() {
    return {
      threads: sourceDate.threads,
      posts: sourceDate.posts,
      users: sourceDate.users
    }
  }
}
</script>
