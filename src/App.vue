<template>
    <div class="container">
        <div class="card-container">
            <card
                v-for="user in users"
                :key="user.id"
                :user-name="user.name"
                :website="user.website"
                @click.native="showPreview(user)"
            />
        </div>
        <preview v-if="isPreviewActive" :user="user" />
    </div>
</template>

<script>
import Card from "@/components/card";
import Users from "@/users";
import Preview from "@/components/preview";

export default {
    name: "App",
    components: {
        Card,
        Preview
    },
    data() {
        return {
            users: Users.users,
            isPreviewActive: false,
            user: null
        };
    },
    methods: {
        showPreview(user) {
            // if (this.isPreviewActive && user.id === this.user.id) {
            //     this.isPreviewActive = false;
            // }
            this.isPreviewActive = true;
            this.user = user;
        }
    }
};
</script>

<style lang="scss" scoped>
.container {
    display: flex;
    margin: 20px 60px;
}

.card-container {
    display: flex;
    flex-wrap: wrap;
    margin: 20px 60px;
}
</style>
