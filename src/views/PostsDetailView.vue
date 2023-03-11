<template>
  <div class="post-details">
  <h1>This is a post page</h1>
  <p>Display the content of post with ID of {{ route.param.id}} here!</p>
  <div>
    <button @click="ShowPostID">Show Post ID</button>
  </div>
  <div>
    <button @click="GoHomeAfter3Seconds">Redirect to home after 3 seconds</button>
  </div>
  <p><RouterLink to="/posts">&lt; Back</RouterLink></p>
</div>
</template>

<script setup>
import {RouterLink, useRoute, useRouter} from 'vue-router'

const route = useRoute()
const router = useRouter()



const ShowPostID =  () => {
  console.log(route.params.id)
}

const GoHomeAfter3Seconds = () => {
setTimeout(() => {
  router.push('/')
}, 3000)

}

</script>