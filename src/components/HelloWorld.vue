<template>
  <div class="hello">
    <!-- <p>{{msg}}</p>
    <div v-for="(value, index) in items" :key="index">
      {{ index }}.{{ value }}
    </div>
    <button @click="switchPosition">淡淡的</button>
    <button @click="switchPosition">淡淡的</button> -->
	  <timeLine :medicalRecords='medicalRecords'></timeLine>
  </div>
</template>

<script>
import timeLine from './TimeLine'
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
      items2: ['gfhfgh', 'sdcsdf', 'tetert'],
      medicalRecords: [{
        time: '2017-04-25 10:21:00',
        hospital: '上海市长海医院',
        medicalType: '住院',
        code: '7382734823748273',
        Diagnosis: '入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111'
      }, {
        time: '2017-04-25 10:21:00',
        hospital: '上海市长海医院',
        medicalType: '住院',
        code: '7382734823748273',
        Diagnosis: '入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111'
      }, {
        time: '2017-04-25 10:21:00',
        hospital: '上海市长海医院',
        medicalType: '住院',
        code: '7382734823748273',
        Diagnosis: '入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111'
      }, {
        time: '2017-04-25 10:21:00',
        hospital: '上海市长海医院',
        medicalType: '住院',
        code: '7382734823748273',
        Diagnosis: '入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111'
      }, {
        time: '2017-04-25 10:21:00',
        hospital: '上海市长海医院',
        medicalType: '住院',
        code: '7382734823748273',
        Diagnosis: '入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111，入院诊断1111'
      }]
    }
  },
  components: {
    timeLine
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
