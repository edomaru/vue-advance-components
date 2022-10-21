<template>
    <div :class="['alert', 'alert-' + type]">
        {{ message }}
    </div>
</template>

<script>
export default {
    props: ['message', 'type']
}
</script>