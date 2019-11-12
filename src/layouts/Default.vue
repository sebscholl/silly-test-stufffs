<template>
  <div class="container">
    <header class="header">
      <g-link class="title" :to="{ name: 'mentors'}">Mentors</g-link>
      <g-link class="subtitle" :to="{ name: 'about' }">About {{ $static.eightBase.companyName }}</g-link>
    </header>
    <slot/>
  </div>
</template>

<static-query>
query {
  eightBase {
    companyName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
