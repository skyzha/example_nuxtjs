<template>
  <section class="single-recipe">
    <h1>{{ recipe.id }}</h1>
    <div>
      <img :src="recipe.thumbnail" :alt="recipe.title" />
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  asyncData() {
    return new Promise((resolve, reject) => {
      //   setTimeout(() => {
      resolve({
        recipe: [
          {
            id: '1',
            title: 'Delicious',
            previewText: 'yummy!!!',
            descriptionText: 'This is very delicious, amazing !!!',
            thumbnail:
              'https://images.unsplash.com/photo-1573400780054-c260eb4865b2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1402&q=80'
          },
          {
            id: '2',
            title: 'Yummy',
            previewText: 'good!!!',
            descriptionText: 'This is very delicious, amazing !!!',
            thumbnail:
              'https://images.unsplash.com/photo-1562376552-0d160a2f238d?ixlib=rb-1.2.1&auto=format&fit=crop&w=625&q=80'
          }
        ]
        // .find((el) => el.id === context.params.id)
      })
      //   }, 1500)
    })
  }
}
</script>
<style scoped>
a {
  text-decoration: none;
  color: black;
}
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
</style>
