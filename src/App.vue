<script>
import Person from "./components/Person.vue"
import Alert from "./components/Alert.vue"
import Alerts from "./components/Alerts.vue"

export default {
  components: {
    Person,
    Alerts,
    Alert
},
  data: () => ({
    items: 3,
    show: false,
    alert: {
      message: "Message",
      types: ["success", "warning", "danger"],
    }
  })
}
</script>

<template>
  <div class="container py-5">
    <Person age="25" first-name="John" last-name="Doe" />
  </div>
</template>
