<template>
  <div class="container">
    <h1>Info Component</h1>
    <p>{{ info }}</p>
    <ul>
      <li v-for="array in arrays" :key="array.id">
        {{ array.id }}
        {{ array.name }}
        {{ array.age }}
      </li>
    </ul>
    <button @click="alert">click</button>
  </div>
</template>

<script>
export default {
  name: 'InfoComponent',
  data() {
    return {
      info: 'これは、情報を表示するコンポーネントです',
      arrays: [
        {id: 1, name: 'Taro', age: 28},
        {id: 2, name: 'Hanako', age: 25},
        {id: 3, name: 'Sato', age: 24}
      ]
    }
  },
  methods: {
    // eslint-disable-next-line vue/return-in-computed-property
    alert() {
      // eslint-disable-next-line no-console
      window.alert('こんばんは!')
    }
  }
}
</script>

<style scoped>
.container h1 {
  color: lightgrey;
  font-weight: bold;
}
.container p {
  color: darkblue;
}
.container ul {
  list-style-type: none;
}
</style>
