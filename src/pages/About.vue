<template>
  <Layout>
    <h1>About us</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </Layout>
</template>

<page-query>
  query ($id: ID!) {
    projet(id: $id) {
      title
      imageURL
      date(format: "DD MMMM YYYY", locale: "fr")
      tag
      content
    }
  }
</page-query>
<script>
export default {
  metaInfo: {
    title: 'About us'
  }
}
</script>
