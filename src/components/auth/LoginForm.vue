<template>
    <h1>Login</h1>
    <form @submit.prevent="$emit('submit', email, password)">
        <div class="mb-3">
            <input type="email" v-model="email" class="form-control" placeholder="Email">
        </div>
        <div class="mb-3">
            <input type="password" v-model="password" class="form-control" placeholder="Password">
        </div>
        <div class="mb-3">
            <button class="btn btn-primary">Login</button>
        </div>
    </form>
</template>

<script>
export default {
    data: () => ({
        email: '',
        password: ''
    }),
    emits: {
        submit: (email, password) => {
            if (email && password) {
                return true;
            } else {
                console.warn("Invalid submit event payload.");
                return false;
            }
        }
    }
}
</script>