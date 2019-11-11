<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :preview-text="recipe.previewText"
    />
  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      // setTimeout(() => {
      resolve({
        recipes: [
          {
            id: '1',
            title: 'Delicious',
            previewText: 'yummy!!!',
            thumbnail:
              'https://images.unsplash.com/photo-1573400780054-c260eb4865b2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1402&q=80'
          },
          {
            id: '2',
            title: 'Yummy',
            previewText: 'good!!!',
            thumbnail:
              'https://images.unsplash.com/photo-1562376552-0d160a2f238d?ixlib=rb-1.2.1&auto=format&fit=crop&w=625&q=80'
          }
        ]
      })
      // }, 1500)
    })
  }
}
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
</style>
