
<template>
  <Page>
    <ActionBar title="Form Example" />
    <StackLayout class="form-container">
      <Label text="Name" class="label" />
      <TextField v-model="name" class="input" />

      <Label text="Email" class="label" />
      <TextField v-model="email" class="input" keyboardType="email" />

      <Button text="Submit" @tap="submitForm" class="submit-btn" />
    </StackLayout>
  </Page>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
    };
  },
  methods: {
    submitForm() {
      // Perform form validation and submit logic here
      console.log('Submitted!');
      console.log('Name:', this.name);
      console.log('Email:', this.email);
    },
  },
};
</script>

<style scoped>
.form-container {
  padding: 20px;
}

.label {
  font-size: 18px;
  margin-bottom: 5px;
}

.input {
  height: 40px;
  padding: 5px;
  border-width: 1px;
  border-color: gray;
  margin-bottom: 15px;
}

.submit-btn {
  margin-top: 20px;
  height: 40px;
}
</style>
