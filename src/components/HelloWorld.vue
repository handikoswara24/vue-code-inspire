<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <alert mode="primary">First Alert</alert>
    <alert mode="success">Second Alert</alert>
    <alert mode="danger">Third Alert</alert>
    <div>
      <input type="text" v-model="lastName" placeholder="Your nice name?" />
      <p>Welcome, {{lastName}}</p>
    </div>
    <button @click="ClickedMe()">Click Me</button>
    <input type="text" @keyup.enter="DoSomething()" placeholder="Input Your Code" />
    <h3>Using Loop</h3>
    <ul>
      <li v-for="(person, index) in students" v-bind:key="index">{{person}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      lastName: "Aaa",
      students: ["aaa", "aaa", "ccc", "ddd"]
    };
  },
  methods: {
    ClickedMe: function() {
      console.log("You click a button");
    },
    DoSomething: function() {
      console.log("Coupon Applied");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
