<template>
    <div>
        {{ user.firstName }} {{ user.lastName }} {{ user.email }}
    </div>
</template>

<script>
export default {
    name: 'UserComp',
    props: {
        user: Object,
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