<template>
  <section>
    <header><h1>Nome e idade</h1></header>
    <ul>
      <active-user :user-name="Name" :user-age="Age"> </active-user>
    </ul>
    <user-data @add-user="addUser"> </user-data>
  </section>
</template>

<script>
export default {
  data() {
    return {
      Name: "Maria",
      Age: 48,
    };
  },
  methods: {
    addUser(name, age) {
      this.Name = name;
      this.Age = +age;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Jost&display=swap");

* {
  box-sizing: border-box;
}

html {
  font-family: "Jost", sans-serif;
}

body {
  margin: 0;
}

header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem auto;
  border-radius: 10px;
  padding: 1rem;
  background-color: #4682b4;
  color: aliceblue;
  text-align: center;
  width: 70%;
  max-width: 40rem;
}

#app ul {
  margin: 1rem auto;
  padding: 0;
  list-style: none;
  text-align: center;
  width: 70%;
  max-width: 40rem;
}

#app form {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 70%;
  max-width: 40rem;
}

#app h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: #4682b4;
  margin: 0 0 1rem 0;
}

#app button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #4682b4;
  background-color: #4682b4;
  color: white;
  padding: 0.05rem 1rem;
  border-radius: 10px;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

#app input {
  font: inherit;
  padding: 0.15rem;
}
</style>
