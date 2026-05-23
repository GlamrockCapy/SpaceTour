<template>
  <Header />
  <main>
    <HomePage />
  </main>
  <footer>
    <p>© 2026 SpaceTour.</p>
  </footer>
</template>

<script>
import Header from './components/Header.vue'
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    Header,
    HomePage
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: #333;
  line-height: 1.6;
}

main {
  min-height: calc(100vh - 200px);
}

footer {
  background: #1e40af;
  color: white;
  padding: 2rem;
  text-align: center;
  margin-top: 4rem;
}

footer p {
  margin: 0;
}
</style>