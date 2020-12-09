<template>
  <div class="layout">
    <header class="header">

      <strong>
        <g-link to="/" class="title">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Accueil</g-link>
        <g-link class="nav__link" to="/about/">À propos</g-link>
        <g-link class="nav__link" to="/projets/">Projets</g-link>

      </nav>
    </header>

    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: "Oswald",sans-serif;
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
  background-color: #3ACDC6;
  padding: 1rem;
}

h1{
  color: #3ACDC6;
}

p{
  font-family: "Quicksand",sans-serif;
}

.title:hover{
  color: white;
  text-decoration: none;

}

.title{
  color: white;
  text-decoration: none;
  font-size: 30px;
}

.nav__link {
  margin-left: 20px;
  color: white;
  text-decoration: none;
}

.nav__link:hover {
  margin-left: 20px;
  color: white;
  text-decoration: none;
}
</style>
