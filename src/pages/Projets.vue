<template>
  <Layout>
    <h1>Liste des projets</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
    <ul>
      <li v-for="{node:projet} of $page.allProjet.edges" :key="projet.id">
        <g-link :to="projet.path">{{projet.title}}</g-link>
      </li>
    </ul>


  </Layout>
</template>

<page-query>
  query {
    allProjet {
      edges {
        node {
          id
          path
          title
        }
      }
    }
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: 'Liste des projets'
  }
}
</script>
