<template>
    <h1>Login</h1>
    <form @submit.prevent="$emit('submit', email, password)">
        <div class="mb-3">
            <input type="email" :value="email" @input="handleInputEmail" class="form-control" placeholder="Email">
        </div>
        <div class="mb-3">
            <input type="password" :value="password" @input="$emit('update:password', $event.target.value)" class="form-control" placeholder="Password">
        </div>
        <div class="mb-3">
            <button class="btn btn-primary">Login</button>
        </div>
    </form>
</template>

<script>
export default {
    props: {
        email: String,
        emailModifiers: {
            type: Object,
            default: () => ({})
        },
        password: String
    },
    methods: {
        handleInputEmail (event) {
            let value = event.target.value;
            if (this.emailModifiers.lowercase) {
                value = value.toLowerCase();
            }
            this.$emit('update:email', value);
        }
    },
    emits: {
        submit: (email, password) => {
            if (email && password) {
                return true;
            } else {
                console.warn("Invalid submit event payload.");
                return false;
            }
        },
        'update:email': null,
        'update:password': null,
    }
}
</script>