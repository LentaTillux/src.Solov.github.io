<template>
  <div class="container">
    <div>
      <p>Hi</p>
      <NLink to="/">
        Home page
      </NLink>
      <p>Timestamp: {{ date }}</p>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'About page'
  },
  name: 'Date',
  serverCacheKey () {
    // Will change every 10 secondes
    return Math.floor(Date.now() / 10000)
  },
  data () {
    return { date: Date.now() }
  }
}
</script>
