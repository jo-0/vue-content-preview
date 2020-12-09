<template>
    <div class="card">
        <div class="card-data">
            <h2>{{ userName }}</h2>
            <p>{{ website }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "card",
    props: {
        userName: {
            type: String,
            required: true
        },
        website: {
            type: String,
            required: true
        }
    }
};
</script>

<style lang="scss" scoped>
.card {
    border: 1px solid black;
    border-radius: 12px;
    display: flex;
    flex-basis: 260px;
    margin: 20px 20px;

    &-data {
        padding: 20px;
    }
}
</style>
