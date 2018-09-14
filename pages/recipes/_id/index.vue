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
                            thumbnail: "/assets/img/pizza.jpg",
                            description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore velit aut reiciendis laborum totam. Perspiciatis eligendi veniam voluptatibus provident fuga facilis enim sequi voluptas mollitia! Laboriosam voluptatem nihil quia placeat?"
                        },
                        {
                            id: "2",
                            title: "Un big belly burger",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "/assets/img/humberger.jpg",
                            description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore velit aut reiciendis laborum totam. Perspiciatis eligendi veniam voluptatibus provident fuga facilis enim sequi voluptas mollitia! Laboriosam voluptatem nihil quia placeat?"
                        },
                        {
                            id: "3",
                            title: "Une salade 100% bio",
                            previewDescription: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                            thumbnail: "/assets/img/salade.jpg",
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


