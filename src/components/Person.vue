<template>
    <div>
        <p><strong>Full name</strong>: {{ fullName }}</p>
        <p><strong>Age</strong>: {{ age }} years</p>
    </div>
</template>

<script>
export default {
    props: ['firstName', 'lastName', 'age'],
    computed: {
        fullName () {
            return this.firstName + ' ' + this.lastName;
        }
    }
}
</script>