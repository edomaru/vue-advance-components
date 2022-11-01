<template>
    <div class="mb-3">
        <label class="form-label">{{ label }}</label>
        <input type="text" class="form-control" v-model="value">
    </div>
</template>

<script>
export default {
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