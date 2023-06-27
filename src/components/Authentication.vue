<template>
    <div>
        <h3>Аутентификация</h3>
        <p v-if="isAuthenticated">Пользователь успешно аутентифицирован</p>
        <form action="#" v-else>
            <div>
                <label for="username">Имя пользователя:</label>
                <input type="text" id="username" v-model="userName">
                <p>{{ userName }}</p>
            </div>
            <div>
                <label for="password">Пароль:</label>
                <input type="text" id="password" v-model="password">
                <p>{{ password }}</p>
            </div>


        </form>
    </div>
</template>

<script>
export default {
    name: 'AuthenticationComp',

    props: {
        isAuthenticated: Boolean,
},

    data() {
        return {
            userName: '',
            password: '',
        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>

<style lang="scss" scoped></style>