<template>
  <div>
    <h3>Customer Reviews</h3>
    <div>
      <reviewCard v-for="reviewer in reviewers" :key="reviewer.login.uuid"
      :review="reviewer"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviewers: []
    }
  },
  created () {
   this.fetchUser()
  },
  methods: {
    async fetchUser () {
      const result = await fetch('https://randomUser.me/api/?results=5')
      .then(res => res.json())
      console.log(result.results)
      this.reviewers = result.results
      console.log(reviewers)
  
    }
  }
}
</script>

<style scoped></style>