<template>
    <h1>Register</h1>
    <form>
        <div class="mb-3">
            <input type="text" v-model="name" class="form-control" placeholder="Name">
        </div>
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
        name: '',
        email: '',
        password: ''
    })
}
</script>