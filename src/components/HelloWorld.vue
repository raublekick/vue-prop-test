<template>
  <div class="hello">
    <p>
      String prop:
      {{ msg }}
      <button @click="modifyString()">Modify</button>
    </p>

    <p>
      Object prop:
      {{ data }}
      <button @click="modifyObject()">Modify</button>
    </p>    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    data: Object
  },
  methods: {
    modifyString() {
      this.msg = "The prop 'msg' has been modified. Check the console for a warning.";
    },
    modifyObject() {
      this.data.property1 = "Property 1 has been modified. No warnings!";
    }
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
