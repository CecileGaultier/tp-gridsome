<template>
    <Layout>
        <div class="projet">
            <h1>{{$page.projet.title}}</h1>
            <div class="content" v-html="$page.projet.content"></div>

                <p><img :src="$page.projet.imageURL" alt=""></p>


                <p><b>Like</b> : {{ this.$page.projet.like }}</p>
                <p><b>Tendance</b> : {{ this.$page.projet.color }}</p>
                <p><time><b>Date</b> : {{ this.$page.projet.date }}</time></p>
                <ul>
                    <li v-for="tag of $page.projet.tag" :key="tag" class="tag">{{tag}}</li>
                </ul>
                <div>
                    <div class="auteur">
                        <p><b>Auteur</b> : </p>
                        <p> {{ this.$page.projet.auteur.name }};</p>
                        <p> {{ this.$page.projet.auteur.birthdate }};</p>
                        <p> {{ this.$page.projet.auteur.address.city }};</p>
                    </div>

                </div>

            </div>
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
            like
            color
            auteur{
                public
                name
                birthdate
                address{
                    street
                    city
                    post_code
                }
            }
        }
    }
</page-query>

<script>
    export default {
        name: "Projet",
        metaInfo() {
            return {
                title: this.$page.projet.title,
            }
        }
    }
</script>

<style>

    .auteur p{
        display: inline;
    }

    ul{
        padding-left: 0;
    }

    li {
        list-style: none;
    }

    .tag {
        margin : 5px;
        text-align: center;
        color: white;
        text-decoration: none;
        background-color: #0C9FAD;
        padding: .5rem;
        border-radius: .8rem;
        list-style: none;
        display: inline;
        font-size: 16px;
    }
</style>