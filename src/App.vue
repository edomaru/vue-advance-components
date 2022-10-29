<script>
import Person from "./components/Person.vue"
import Alert from "./components/Alert.vue"
import Alerts from "./components/Alerts.vue"
import LoginForm from "./components/auth/LoginForm.vue"

export default {
  components: {
    Person,
    Alerts,
    Alert,
    LoginForm
},
  data: () => ({
    items: 3,
    show: true,
    alert: {
      message: "Message",
      types: ["success", "warning", "danger"],
    }
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
    <LoginForm @submit="handleSubmit" />
  </div>
</template>
