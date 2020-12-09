<template>
    <Layout>
        <div class="projet">
            <h1 class="text-center">{{$page.projet.title}}</h1>
            <div class="content m-3" v-html="$page.projet.content"></div>
            <div class="container my-5">
                <div class="row">
                    <div class="col-7">
                        <p><img :src="$page.projet.imageURL" class="img-fluid" alt=""></p>
                    </div>
                    <div class="col-5">
                        <p><time>Date : {{ this.$page.projet.date }}</time></p>
                        <ul>
                            <li v-for="tag of $page.projet.tag" :key="tag" class="link">{{tag}}</li>
                        </ul>
                    </div>
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

    .link {
        margin : 20px auto;
        display: block;
        text-align: center;
        color: white;
        text-decoration: none;
        background-color: #3ACDC6;
        padding: 1rem;
        border-radius: .8rem;
        list-style: none;

    }
</style>