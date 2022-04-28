<template>
  <div>
    <h1>HTTP GET Component</h1>
    <ul>
      <li v-for="array in arrays" :key="array.id">
        {{ array.id }}
        {{ array.user }}
        {{ array.email }}
      </li>
    </ul>
    <button @click="httpGet">URL GET</button>
  </div>
</template>

<script>
export default {
  name: 'HttpComponent',
  data() {
    return {
      url: 'https://jsonplaceholder.typicode.com/users/',
      arrays: []
    }
  },
  methods: {
    httpGet() {
      fetch(this.url)
    .then((data) => data.json())
    .then((obj) => {
      // eslint-disable-next-line no-console
      console.table(obj)
      this.arrays = obj
    })
    }
  },
}
</script>
