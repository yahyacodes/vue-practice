<template>
  <div>
    <label>To do:</label>
    <input type="text" v-model="todo" />
    <br />
    <br />
    <button @click="handleClick">Add</button>
    <ul v-for="todo in todos">
      <li>{{ todo }}</li>
    </ul>
  </div>
</template>
<script>
export default {
  methods: {
    handleClick() {
      this.todos.push(this.todo);
      this.todo = "";
    },
  },
  data() {
    return {
      todo: "",
      todos: [],
    };
  },
};
</script>
<style>
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}

ul {
  list-style: none;
}

ul li {
  background-color: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
input {
  padding: 10px 6px;
  width: 40%;
  box-sizing: border-box;
  border-radius: 4px;
  border: 1px solid #ddd;
  color: #555;
}

button {
  background: #0faf87;
  color: white;
  border: none;
  padding: 8px 24px;
  border-radius: 4px;
  font-size: 16px;
  letter-spacing: 1px;
  cursor: pointer;
  margin: 10px;
}
h2 {
  background-color: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
</style>
