<template>
    <div class="mb-3">
        <label class="form-label">{{ label }}</label>
        <input type="text" class="form-control">
    </div>
</template>

<script>
export default {
    props: {
        label: {
            type: String,
            required: true
        }
    }
}
</script>