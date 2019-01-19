<template>
    <app-navigation></app-navigation>
</template>

<script>
    import {StackNavigator} from "vue-native-router";
    import HomeScreen from "./src/screens/HomeScreen.vue";
    import SecondScreen from "./src/screens/SecondScreen.vue";

    const AppNavigation = StackNavigator(
        {
            Home: HomeScreen,
            Second: SecondScreen,
        },
        {
            initialRouteName: 'Home',
        }
    );
    export default {
        components: {AppNavigation}
    }
</script>
