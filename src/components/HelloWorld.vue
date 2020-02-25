<template>
  <div class="hello">
    <p>User name: {{ userName }}</p>
    <input v-model="title" placeholder="enter title here">
    <p>User name prefixed with a title: "{{ prefixedMessage }}"</p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      userName: "John Doe",
      // title: ""
      title: "Miss"
    };
  },
  computed: {
    // a computed getter
    prefixedMessage: function() {
      // `this` points to the Vue instance's data option
      return this.title + " " + this.userName;
    }
  }
};
</script>