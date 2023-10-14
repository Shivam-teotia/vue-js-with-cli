<template>
  <form @submit.prevent="submitData">
    <div>
      <label> Name </label>
      <input type="text" v-model="enteredName" />
    </div>
    <div>
      <label> Email </label>
      <input type="email" v-model="enteredEmail" />
    </div>
    <div>
      <label> Phone </label>
      <input type="tel" v-model="enteredPhone" />
    </div>
    <button>Add Friend</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      enteredName: "",
      enteredEmail: "",
      enteredPhone: "",
    };
  },
  methods: {
    submitData() {
      this.$emit(
        "add-contact",
        this.enteredName,
        this.enteredPhone,
        this.enteredEmail
      );
    },
  },
  emits: ["add-contact"],
};
</script>
