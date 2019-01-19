<template>
    <view class="container">
        <text class="text-color-primary">My Vue Native App</text>
        <button v-bind:onPress="handleBtnClickCount" :title="btnTitle"/>
    </view>
</template>

<style>
    .container {
        background-color: white;
        align-items: center;
        justify-content: center;
        flex: 1;
    }

    .text-color-primary {
        color: blue;
    }
</style>

<script>
    export default {
        props: {
            navigation: {
                type: Object
            }
        },
        data: function () {
            return {
                btnTitle: "Back to HomeScreen",
            };
        },
        methods: {
            handleBtnClickCount: function () {
                this.navigation.goBack();
            }
        }
    };
</script>
