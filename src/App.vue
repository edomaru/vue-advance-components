<script>
import Person from "./components/Person.vue"
import Alert from "./components/Alert.vue"
import Alerts from "./components/Alerts.vue"
import LoginForm from "./components/auth/LoginForm.vue"
import BaseInput from "./components/BaseInput.vue"

export default {
  components: {
    Person,
    Alerts,
    Alert,
    LoginForm,
    BaseInput
},
  data: () => ({
    items: 3,
    show: true,
    alert: {
      message: "Message",
      types: ["success", "warning", "danger"],
    },
    email: ''
  }),
  methods: {
    handleSubmit (email, password) {
      alert(email + ' ' + password);
    }
  }
}
</script>

<template>
  <div class="container py-5">
    <!-- <Person :age="25" first-name="John" last-name="Doe" /> -->
    <!-- <Alerts v-bind="alert" /> -->
    <!-- <Alert message="Alert message" type="danger" :show="show" @alert-close="show = false" /> -->
    <!-- <LoginForm @submit="handleSubmit" /> -->
    <!-- <input type="email" class="form-control" :value="email" @input="email = $event.target.value" placeholder="Email" /> -->
    <BaseInput v-model="email" label="Email" />
    {{ email }}
  </div>
</template>
