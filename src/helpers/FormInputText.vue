<template>
    <div class="form-element form-element-input-text">
        <label for="">{{label}}</label>
        <input
                :type="type"
                :colrClass="colorClass"
                :placeholder="placeholder"
                :required="required"
                v-bind:value="inputVal"
                @input="$emit('input', $event.target.value)"
        >
    </div>
</template>
<script>
    export default {
        name: "FormInputText",
        props: {
            label: String,
            type: String,
            placeholder: String,
            colorClass: String,
            required: Boolean,
            inputVal: String
        }
    }
</script>
<style lang="scss" scoped>
    .input-text {

    }
</style>