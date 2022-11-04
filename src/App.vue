<script>
import Person from "./components/Person.vue"
import Alert from "./components/Alert.vue"
import Alerts from "./components/Alerts.vue"
import LoginForm from "./components/auth/LoginForm.vue"
import BaseInput from "./components/BaseInput.vue"
import BaseButton from "./components/BaseButton.vue"
import IconCheck from "./components/icons/IconCheck.vue"
import IconExclamation from "./components/icons/IconExclamation.vue"
import Modal from "./components/Modal.vue"
import TodoList from "./components/TodoList.vue"

export default {
  components: {
    Person,
    Alerts,
    Alert,
    LoginForm,
    BaseInput,
    BaseButton,
    Modal,
    IconCheck,
    IconExclamation,
    TodoList
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
    <!-- <Alert type="success" :show="show" @alert-close="show = false" v-slot="{ alertLink }">
      The alert message <a href="#" :class="alertLink">Alert link</a>
    </Alert> -->
    <TodoList>
      <template #default="{ name }">
        <input type="checkbox" class="form-check-input me-1">
        <label class="form-check-label">{{ name }}</label>
      </template>
      <template #footer="{ all, todo, done }">
        <div class="d-flex justify-content-between align-items-center">
          <span class="text-muted">All ({{ all }})</span>
          <span class="text-muted">Todo ({{ todo }})</span>
          <span class="text-muted">Done ({{ done }})</span>
        </div>
      </template>
    </TodoList>
  </div>
</template>
