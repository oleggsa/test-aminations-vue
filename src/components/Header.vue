<template>
    <div class="logo">
        <div class="logo-inner">
            <img src="../assets/mozgi.svg" alt="logo">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style lang="scss" scoped>
.logo {
    position: relative;
    z-index: 2;
}
svg {
    fill: red;
}
</style>