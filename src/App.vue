<script>
export default {
    data() {
        return {
            drawer: false,
            items: [
                { label: "Home", to: "/home" },
                { label: "Sign In", to: "/signin" },
                { label: "Register", to: "/register" },
            ],
        };
    },
};
</script>
<template>
    <pv-toast />
    <header>
        <pv-toolbar class="bg-primary fixed-toolbar" style="background-color: #F3A7A7;">
            <template #start>
                <img src="@/assets/logo.png" alt="Logo" class="toolbar-logo" >
            </template>
            <template #end>
                <div class="flex-row">
                    <router-link
                            v-for="item in items"
                            :to="item.to"
                            custom
                            v-slot="{ navigate, href }"
                            :key="item.label"
                    >
                        <pv-button
                                class="p-button-text text-white"
                                :href="href"
                                @click="navigate"
                        >{{ item.label }}</pv-button
                        >
                    </router-link>
                </div>
            </template>
        </pv-toolbar>
    </header>
    <pv-sidebar v-model:visible="drawer"> </pv-sidebar>
    <RouterView />
</template>

<style scoped>
.toolbar-logo {
    max-height: 100%;
    height: 50px;
    flex-shrink: 0;
    object-fit: contain;
}

.bg-primary {
    background-color: #F3A7A7 !important;
}

.flex-row {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-end;
    gap: 1rem;
}

.p-button-text {
    font-size: 1rem;
}

.fixed-toolbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
}
</style>

