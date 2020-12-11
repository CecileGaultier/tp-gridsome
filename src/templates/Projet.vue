<template>
    <Layout>
        <div class="projet">
            <h1>{{$page.projet.title}}</h1>
            <div class="content" v-html="$page.projet.content"></div>
            <b-container>
                <b-row>
                    <b-col cols="7">
                        <p><img :src="$page.projet.imageURL" alt=""></p>
                    </b-col>
                    <b-col cols="5">
                        <p>Like : {{ this.$page.projet.like }}</p>
                        <p><time>Date : {{ this.$page.projet.date }}</time></p>
                        <ul>
                            <li v-for="tag of $page.projet.tag" :key="tag" class="tag">{{tag}}</li>
                        </ul>
                    </b-col>
                </b-row>
            </b-container>

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
            auteur
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

    li {
        list-style: none;
    }

    .tag {
        margin : 20px auto;
        text-align: center;
        color: white;
        text-decoration: none;
        background-color: #0C9FAD;
        padding: 1rem;
        border-radius: .8rem;
        list-style: none;

    }
</style>