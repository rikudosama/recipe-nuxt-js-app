<template>
    <section class="recipes">
        <recipe 
        v-for="recipe in recipes"
        :key="recipe.id"
        :title="recipe.title"
        :thumbnail="recipe.thumbnail"
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
                            thumbnail: "http://www.wellandpizza.com/wp-content/uploads/2017/11/Lucianos-Pizzeria-Welland-Pizza4.jpg"
                        },
                        {
                            id: "2",
                            title: "Un big belly burger",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "http://assets.epicurious.com/photos/57c5c6d9cf9e9ad43de2d96e/master/pass/the-ultimate-hamburger.jpg"
                        },
                        {
                            id: "3",
                            title: "Une salade 100% bio",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "https://cdn2.tmbi.com/TOH/Images/Photos/37/1200x1200/Holiday-Lettuce-Salad_exps41195_CW132792B07_09_6bC_RMS.jpg"
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
