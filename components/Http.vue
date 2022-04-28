<template>
  <div>
    <h1>HTTP GET Component</h1>
    <button @click="httpGet">URL GET</button>
  </div>
</template>

<script>
export default {
  name: 'HttpComponent',
  data() {
    return {
      url: 'https://jsonplaceholder.typicode.com/users/'
    }
  },
  methods: {
    httpGet() {
      fetch(this.url)
    .then((data) => data.json())
    .then((obj) => {
      // eslint-disable-next-line no-console
      console.table(obj)
    })
    }
  }
}
</script>
