<template>
    <div>
        <ul>
            <li v-for="user in users" :key="user.id">
                <UserComp :user="user"/>
            </li>
        </ul>
    </div>
</template>

<script>
import UserComp from './User.vue';

export default {
    name: 'UserList',

    components: {
        UserComp,
    },
    props: {
        users: Array,
    },

    data() {
        return {

        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>

<style lang="scss" scoped></style>