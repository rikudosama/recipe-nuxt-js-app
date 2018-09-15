<template>
    <p>
        <section class="single-recipe">
            <article>
                <h1>{{ recipe.title }}</h1>
                <div>
                    <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
                </div>
                <p>
                    {{ recipe.description }}
                </p>
            </article>
        </section>
    </p>
</template>
<script>
export default {
    asyncData(context) {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipe: [
                        {
                            id: "1",
                            title: "Savoureuse pizza",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "http://www.wellandpizza.com/wp-content/uploads/2017/11/Lucianos-Pizzeria-Welland-Pizza4.jpg",
                            description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore velit aut reiciendis laborum totam. Perspiciatis eligendi veniam voluptatibus provident fuga facilis enim sequi voluptas mollitia! Laboriosam voluptatem nihil quia placeat?"
                        },
                        {
                            id: "2",
                            title: "Un big belly burger",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "http://assets.epicurious.com/photos/57c5c6d9cf9e9ad43de2d96e/master/pass/the-ultimate-hamburger.jpg",
                            description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore velit aut reiciendis laborum totam. Perspiciatis eligendi veniam voluptatibus provident fuga facilis enim sequi voluptas mollitia! Laboriosam voluptatem nihil quia placeat?"
                        },
                        {
                            id: "3",
                            title: "Une salade 100% bio",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "https://cdn2.tmbi.com/TOH/Images/Photos/37/1200x1200/Holiday-Lettuce-Salad_exps41195_CW132792B07_09_6bC_RMS.jpg",
                            description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore velit aut reiciendis laborum totam. Perspiciatis eligendi veniam voluptatibus provident fuga facilis enim sequi voluptas mollitia! Laboriosam voluptatem nihil quia placeat?"
                        }
                    ].find(el => el.id === context.params.id)
                })
            }, 1000)
        })
    }
}
</script>
<style scoped>
    .single-recipe 
    {
        display: flex;
        flex-flow: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 30px;
    }
    .recipe-image
    {
        width: 100%;
    }
</style>


