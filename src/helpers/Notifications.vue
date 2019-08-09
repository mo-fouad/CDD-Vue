<template>
    <div class="notification">
        <span> Login successful. Please wait while we redirect...</span>
    </div>
</template>
<script>

</script>
<style lang="scss">
    @import "../scss/vars";

    .notification {
        position: absolute;
        z-index: 99;
        top: 22px;
        left: 0;
        right: 0;
        margin: 0 auto;
        width: 500px;
        height: 60px;
        padding: 18px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        border-radius: 4px;
        color: #fff;
        text-align: center;
        background-color: $notification-wait;

        span {
            font-size: 14px;
            line-height: 24px;
        }
    }

    @media only screen and (max-width: 768px) {
        .notification {
            width: 90%;
            max-width: 375px;
            height: auto;

            // I dont konw why it is Deleted from the mobile in the design
            display: none;
        }
    }

</style>
