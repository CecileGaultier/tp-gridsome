<template>
  <Layout>



    <h1>Bienvenue sur All&Surfing !</h1>

    <p>
      Le surf (abréviation française de l'anglais surf-riding, où riding signifie « monter » et surf « (vagues) déferlantes ») est une action ou une pratique physique individuelle de glisse sur les vagues, au bord de l'océan. Avec ce sens général, le surf englobe toutes les pratiques dans les vagues, sans restriction d'une posture (debout, sur le ventre, à genoux) ou du type de flotteur1. Faisant depuis des temps immémoriaux partie de la culture hawaïenne, le surf a notamment a été popularisé dans le monde par le double champion olympique du 100 m nage libre Duke Kahanamoku dans les premières décennies du XXe siècle.
    </p>

    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="surf" src="~/surf.jpg" class="img-fluid" />

    <p>
      Au sens plus moderne, le surf est aussi une discipline sportive codifiée à la fin du XXe siècle, un sport individuel pratiqué debout sur une planche courte (shortboard), par opposition à toutes les autres disciplines de glisse sur les vagues comme le longboard, le bodyboard, le bodysurf, le skimboard, le stand up paddle, le windsurf.
    </p>

    <p>
      Le surf se pratique sur des sites de surf, appelés « spots », plages qui sont baignées par des vagues plus ou moins grandes et propices à la glisse.
    </p>




    <div class="container">
      <div class="row">
        <div class="col-5">
          <p>
            Les pratiquants sont nommés globalement « surfeurs » ou « surfers » (ou exceptionnellement aquaplanchistes[réf. nécessaire]4), sans distinction pour le niveau ou le type de pratique. D'autres termes plus spécifiques existent, comme shortboarder, bodyboardeur, longboardeur, bodysurfeur, etc.
          </p>
        </div>

        <div class="col-5">
          <g-image alt="surf 2" src="~/surf2.jpg" class="img-fluid" />
        </div>
      </div>
    </div>


    <div>
      <p class="home-links">
        <g-link class="link" to="/about/">À propos</g-link>
        <g-link class="link" to="/projets/">Projets</g-link>
      </p>
    </div>



  </Layout>
</template>



<script>
export default {
  metaInfo: {
    title: 'Bienvenue sur All&Surfing !'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}

.link {
  margin : 20px auto;
  display: block;
  text-align: center;
  color: white;
  text-decoration: none;
  background-color: #3ACDC6;
  padding: 1rem;
  border-radius: .8rem;
}

.link:hover{
  color: white;
  text-decoration: none;

}
</style>
