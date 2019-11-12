<template>
  <Layout class="content">
    <p class="title is-4">
      Need a mentors? We have {{ $page.eightBase.usersList.count }} waiting to hear from you!
    </p>
    <hr>
    <a href="https://github.com/">Gridsome + 8base Repo Available here</a>
  </Layout>
</template>

<page-query>
query {
  eightBase {
    usersList {
        count
    }
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: 'About'
  }
}
</script>
