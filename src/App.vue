<template>
  <div id="app">
    <h1>Vue Form</h1>
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <Form/> -->
    <FormWithItems/>
  </div>
</template>

<script>
import Form from './components/Form.vue';
import FormWithItems from './components/FormWithItems';

export default {
  name: "app",
  components: {
    Form,
    FormWithItems
  }
};
</script>

<style>
#app {
  text-align: center;
}

body {
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
    "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

code {
  font-family: source-code-pro, Menlo, Monaco, Consolas, "Courier New", monospace;
}

.form-item {
  display: flex;
  justify-content: space-between;
  width: 600px;
  padding: 20px 0;
  margin: 0 auto;
}

.form-item__input {
  width: 500px;
  height: 30px;
  border-radius: 5px;
  font-size: 20px;
  padding: 5px 20px;
}


label {
  width: 40px;
  text-align: left;
  padding-right: 20px;
  line-height: 44px;
}

.form-item__submit {
  display: block;
  margin: 0 auto;
  width: 200px;
  height: 40px;
  -webkit-appearance: none;
}

.show-area {
  text-align: left;
  width: 500px;
  margin: 20px auto;
  padding: 20px 50px;
  border: 2px solid #eee;
}

img {
  width: 100px;
  padding-bottom: 10px;
}
</style>
