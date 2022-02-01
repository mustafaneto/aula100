<template>
  <form @submit.prevent="updateData">
      Name: <input type="text" v-model="enteredName" /> Age:
      <input type="number" v-model="enteredAge" />
    <button>Atualizar</button>
  </form>
</template>

<script>
export default {
  emits: ["add-user"],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    updateData() {
      this.$emit("add-user", this.enteredName, this.enteredAge);
    },
  },
};
</script>
