<template>
    <div :class="['alert', 'alert-' + type]" v-show="show">
        {{ message }}
    </div>
</template>

<script>
export default {
    // props: ['message', 'type', 'show']
    props: {
        message: {
            type: String,
            required: true
        },
        type: {
            type: String,
            default: 'primary',
            validator: function (value) {
                return ['success', 'primary', 'danger', 'warning'].includes(value);
            }
        },
        show: Boolean
    }
}
</script>