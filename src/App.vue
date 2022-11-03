<script>
import Person from "./components/Person.vue"
import Alert from "./components/Alert.vue"
import Alerts from "./components/Alerts.vue"
import LoginForm from "./components/auth/LoginForm.vue"
import BaseInput from "./components/BaseInput.vue"
import BaseButton from "./components/BaseButton.vue"
import IconCheck from "./components/icons/IconCheck.vue"
import IconExclamation from "./components/icons/IconExclamation.vue"

export default {
  components: {
    Person,
    Alerts,
    Alert,
    LoginForm,
    BaseInput,
    BaseButton,
    IconCheck,
    IconExclamation
},
  data: () => ({
    items: 3,
    show: true,
    alert: {
      message: "Message",
      types: ["success", "warning", "danger"],
    },
    email: '',
    password: '',
    message: "Alert message"
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
    <Alert type="danger" :show="show" @alert-close="show = false">
    </Alert>
  </div>
</template>
