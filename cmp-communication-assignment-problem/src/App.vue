<template>
  <active-user :username="user.name" :userage="user.age" />
  <user-data @set-data="setUserData" />
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "Shivam",
        age: 22,
      },
    };
  },
  methods: {
    setUserData(name, age) {
      this.user = {
        name: name,
        age: age,
      };
    },
  },
};
</script>

<style>
html {
  font-family: sans-serif;
}
section {
  margin: 2rem auto;
  max-width: 48rem;
  border-radius: 12px;
  border: 1px solid black;
}
</style>
