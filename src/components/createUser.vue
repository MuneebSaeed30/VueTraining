<template>
  <div class="form">
    <form>
        <label for="name">Name</label>
        <input type="text" id="name" name="firstname" placeholder="Your name..">

        <label for="title">Job Title</label>
        <select id="position" name="title" v-model="job">
            <option value="engineer">Engineer</option>
            <option value="lead">Lead</option>
            <option value="manager">Manager</option>
        </select>
    
        <input type="submit">
    </form>
        <p><pre> data: {{ $data }}</pre></p>
  </div>
</template>

<style>
    input[type=text], select {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    }

    input[type=submit] {
    width: 100%;
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    }

    input[type=submit]:hover {
    background-color: #45a049;
    }

    div.form {
        border-radius: 5px;
        background-color: #f2f2f2;
        padding: 20px;
        width: 30rem; 
    }
</style>

<script>
export default {
  name: "CreateUser",
  data() {
    return {
      name: "",
      job: "manager",
    };
  },
};
</script>

