<template>
    <div>
        <p><strong>Full name</strong>: {{ fullName }}</p>
        <p><strong>Age</strong>: {{ age }} years</p>
    </div>
</template>

<script>
export default {
    // props: ['firstName', 'lastName', 'age'],
    props: {
        firstName: String,
        lastName: String,
        age: [Number, String]
    },
    computed: {
        fullName () {
            return this.firstName + ' ' + this.lastName;
        }
    }
}
</script>