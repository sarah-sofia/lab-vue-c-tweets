<template>
   <span class="timestamp">{{ timestamp }}</span>
</template>

<script>
export default {
    name: 'Timestamp',
    props: {
    timestamp: String,
    },
}
</script>