<template>
  <div class="hello">
    <p>{{msg}}</p>
    <div v-for="(value, index) in items" :key="index">
      {{ index }}.{{ value }}
    </div>
    <button @click="switchPosition">淡淡的</button>
    <button @click="switchPosition">淡淡的</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      message: 'I love you',
      fullName: 'I love you Welcome to Your Vue.js App',
      age: '3',
      x: ['1', '2', '3'],
      y: ['4', '5', '36', '37'],
      items: ['sdsd', 'sdcsdf', 'rtyrty'],
      items2: ['gfhfgh', 'sdcsdf', 'tetert']
    }
  },
  methods: {
    cc () {
      console.log(this.age)
    },
    switchPosition () {
      let set = new Set()
      for (let i = 0; i < this.items.length; i++) {
        set.add(this.items[i])
      }
      for (let i = 0; i < this.items2.length; i++) {
        set.add(this.items2[i])
      }
      this.items = Array.from(set)
      console.log(set)
    },
    warn: function (message, event) {
      // 现在我们可以访问原生事件对象
      if (event) event.preventDefault()
      alert(message)
    }
  },
  watch: {
  },
  computed: {
    reverseedMessage: function () {
      return this.message.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}
#ccc {
  color: red;
}
a {
  color: #42b983;
}
</style>
