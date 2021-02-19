<template>
    <li @click="$emit('increment')">click</li>

</template>

<script>
export default {
    name:'ListItem',
}
</script>