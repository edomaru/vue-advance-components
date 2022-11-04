<template>

        <label class="form-label">{{ label }}</label>
        <input v-bind="$attrs" class="form-control" v-model="value">

</template>

<script>
export default {
    // inheritAttrs: false,
    props: {
        label: {
            type: String,
            required: true
        },
        modelValue: {
            type: String,
            required: true
        },
        modelModifiers: {
            type: Object,
            default: () => ({})
        }
    },
    emits: ['update:modelValue'],
    computed: {
        value: {
            get () {
                return this.modelValue;
            },
            set (value) {
                if (this.modelModifiers.lowercase) {
                    value = value.toLowerCase();
                }
                this.$emit('update:modelValue', value);
            }
        }
    }
}
</script>