<template>
  <button :style="{backgroundColor:bgColor}">{{btnLabel}}</button>
</template>

<script>
export default {
    props: {
        btnLabel: String,
        bgColor: String,
    }
}
</script>

<style>

</style>