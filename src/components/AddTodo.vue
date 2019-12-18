<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo...">
      <br/>
      <input type="date" v-model="date" name="date">
      <br/>
      <br/>

      <select v-model="selected">
      <option :value="Done" disabled>Done?</option>
        <option>Yes </option>
        <option>No </option>
      </select>
      <br/>
      <input type="text" v-model="title" name="title" placeholder="Notes...">
      <br>
      <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
// import uuid from 'uuid';
export default {
  name: "AddTodo",
  data() {
    return {
      title: ''
    }
  },
  methods: {
    addTodo() {
      const newTodo = {
        title: this.title,
        completed: false
      }
      // Send up to parent
      this.$emit('add-todo', newTodo);
      this.title = '';
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
  }
  input[type="text"] {
    flex: 10;
    padding: 5px;
  }
  input[type="submit"] {
    flex: 2;
  }
</style>