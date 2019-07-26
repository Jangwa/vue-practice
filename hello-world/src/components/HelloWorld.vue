<template>
  <div class="hello" v-if="msg.aTestDataVar === 7">
    My First Hellow Word {{ msg.aTestDataVar === 7 ? 'Seven' : 'Not Seven' }}
    <button v-on:click="$emit('parentAlert')"> Click Here</button>
    <ol>
      <li v-for="item in aList.aList" v-bind:key="item.text">
        {{ item.text }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: Object,
    aList: Object
  }
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
</style>
