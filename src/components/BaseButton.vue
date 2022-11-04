<template>
    <button :class="['btn', 'btn-' + theme]">{{ text }}</button>
</template>

<script>
export default {
    created () {
        console.log(this.$attrs);
    },
    props: {
        text: {
            type: String,
            required: true
        },
        theme: {
            type: String,
            default: 'secondary',
            validator: function (value) {
                return ['primary', 'secondary', 'success','info', 'warning', 'danger'].includes(value);
            }
        },
    },
}
</script>