<template>
  <div class="hello">
    {{ initial }}
    <br>
    {{ fromOptions }}
  </div>
</template>

<script>
function makeForm() {
  return {
    d: this.propsData.initial.d
  };
}

export default {
  name: "HelloWorld",

  makeForm,

  props: {
    initial: Object
  },
  data() {
    return {
      fromOptions: this.$options.makeForm()
    };
  }
};
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
