<template>
    <div class="form-element form-element-input-button">
        <button :type="type" class="login-Btn">{{text}}</button>
    </div>
</template>
<script>
    export default {
        name: 'FormInputButton',
        props: {
            text: String,
            type: String
        }
    }

</script>
<style lang="scss" scoped>
    .login-Btn {
        background: #C63040;
    }
</style>