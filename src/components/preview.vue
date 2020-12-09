<template>
    <section class="preview">
        <h3>
            <p class="img-box">IMG</p>
        </h3>
        <div>
            <header>{{ user.name }}</header>
            <p>{{ user.website }}</p>
            <div>
                <h4>{{ user.company.name }}</h4>
                <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book. It has survived not only five centuries,
                    but also the leap into electronic typesetting, remaining
                    essentially unchanged.
                </p>
                <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book. It has survived not only five centuries,
                    but also the leap into electronic typesetting, remaining
                    essentially unchanged. It was popularised in the 1960s with
                    the release of Letraset sheets containing Lorem Ipsum
                    passages, and more recently with desktop publishing software
                    like Aldus PageMaker including versions of Lorem Ipsum.
                </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "preview",
    props: {
        user: {
            type: Object,
            required: true
        }
    }
};
</script>

<style lang="scss" scoped>
.preview {
    border: 1px solid black;
    border-radius: 12px;
    padding: 20px;
}

.img-box {
    border: 1px solid black;
    width: 100%;
    height: 60px;
    text-align: center;
}
</style>
