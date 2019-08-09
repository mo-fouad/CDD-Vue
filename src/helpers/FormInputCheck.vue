<template>
    <div class="form-element form-element-input-check">
        <label class="">
            <input type="checkbox" checked="checked">
            <span class="checkmark"></span>
            <span>{{checkText}}</span>
        </label>
    </div>
</template>
<script>
    export default {
        name: "FormInputCheck",
        props: {
            checkText: String
        }
    }
</script>
<style lang="scss" scoped>


</style>