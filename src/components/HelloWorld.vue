<template>
  <div class="hello" >
    <h1>{{ msg }}</h1>
    <table>
      <tr v-for="(n, keyOfN) in count" :key="keyOfN" class="tr">
        <td v-for="(i, keyOfI) in count" :key="keyOfI" class="td">
          <span v-if="n === i">{{i}}</span>
          <span v-else-if="(i + n) - n === count + 1 - n">{{i}}</span>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 9,
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

table{
  margin: 0 auto;
}

.tr{
  height:100px;
  width:100px;
  border: 1px solid black;
}

.td{
  height:100px;
  width:100px;
  border: 1px solid black;
  text-align: center;
  vertical-align: middle;
}
</style>
