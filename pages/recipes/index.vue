<template>
    <section class="recipes">
        <recipe 
        v-for="recipe in recipes"
        :key="recipe.id"
        :title="recipe.title"
        :previewDescription="recipe.previewDescription"
        :id="recipe.id"
        />
    </section>
</template>
<script>
import Recipe from '~/components/Recipe';
export default {
    components: {
        Recipe
    },
    asyncData() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipes: [
                        {
                            id: "1",
                            title: "Savoureuse pizza",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "/assets/img/pizza.jpg"
                        },
                        {
                            id: "2",
                            title: "Un big belly burger",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "/assets/img/humberger.jpg"
                        },
                        {
                            id: "3",
                            title: "Une salade 100% bio",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "/assets/img/salade.jpg"
                        }
                    ]
                })
            }, 1000)
        })
    }
}
</script>

<style scoped>
    .recipes
    {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-content: center;
    }
</style>
