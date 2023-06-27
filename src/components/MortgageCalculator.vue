<template>
    <div>
        <div>
            <label for="summ">Сумма кредита:</label>
            <input type="number" id="summ" v-model="summ">
        </div>
        <div>
            <label for="percent">Процент по кредиту:</label>
            <input type="number" id="percent" v-model="percent">
        </div>
        <div>
            <label for="term">Срок кредита в годах:</label>
            <input type="number" id="term" v-model="term">
        </div>

        <p>Ежемесячный платеж: {{ montlyPayment }}</p>
        <p>Общая сумма выплат по кредиту: {{ totalPayment }}</p>
    </div>
</template>

<script>
export default {
    name: 'MortgageCalculator',

    data() {
        return {
            summ: 0,
            percent: 0,
            term: 0
        };
    },

    computed: {
        montlyPayment: function () {
            return (Number(this.summ) + (Number(this.summ) * (Number(this.percent) * Number(this.term))) / 100 ) / (Number(this.term) * 12);
        },

        totalPayment: function () {
            return this.montlyPayment * Number(this.term) * 12;
        }
    },

    methods: {

    },
};
</script>

<style lang="scss" scoped></style>