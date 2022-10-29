<template>
    <div :class="['alert', 'alert-' + type]" v-show="show">
        {{ message }}
    </div>
</template>

<script>
export default {
    props: ['message', 'type', 'show']
}
</script>