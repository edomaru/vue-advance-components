<script>
import Person from "./components/Person.vue"
import Alert from "./components/Alert.vue"
import Alerts from "./components/Alerts.vue"
import LoginForm from "./components/auth/LoginForm.vue"
import BaseInput from "./components/BaseInput.vue"
import BaseButton from "./components/BaseButton.vue"

export default {
  components: {
    Person,
    Alerts,
    Alert,
    LoginForm,
    BaseInput,
    BaseButton
},
  data: () => ({
    items: 3,
    show: false,
    alert: {
      message: "Message",
      types: ["success", "warning", "danger"],
    },
    email: '',
    password: ''
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
    <!-- <input type="email" class="form-control" v-model.lazy="email" placeholder="Email" /> -->
    <!-- <LoginForm @submit="handleSubmit" v-model:email.lowercase="email" v-model:password="password" />
      {{ email }} - {{ password }} -->
    <!-- <Alert message="Alert message" type="danger" :show="show" @alert-close="show = false" /> -->
    <!-- <BaseButton text="Submit" theme="primary" @click="show = true" class="mt-3" id="btn-submit" /> -->
    <BaseInput v-model.lowercase="email" label="Email" type="email" />
  </div>
</template>
