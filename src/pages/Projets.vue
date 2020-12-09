<template>
  <Layout>
    <h1>Liste des articles</h1>
    <p>
      Retrouvez tous les articles de surfing !
    </p>
    <ul>
      <li v-for="{node:projet} of $page.allProjet.edges" :key="projet.id">
        <g-link :to="projet.path" class="link">{{projet.title}} </g-link>
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


<style>
.home-links a {
  margin-right: 1rem;
}
img{
  max-width: 760px;
}
.link {
  margin-left: 20px;
  color: white;
  text-decoration: none;
}
</style>
