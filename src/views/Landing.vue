<template>
    <v-container fluid class="mt-0 pa-0">
        <section class="d-flex justify-center align-center dark-grad flex-column main-blue pa-10 mb-10">
            <header class="section-header hero mb-10">
                <h1>Explore.</h1>
                <h1>Learn.</h1>
                <h1>Connect.</h1>
            </header>
            <v-btn
            to="/signup"
            color="#E6AF2E"
            dark
            class="pl-10 pr-10"
            >sign up</v-btn>
        </section>
        <section class="d-flex justify-center align-center dark-grad flex-column">
            <header class="section-header mb-10">
                <h1>Have an account?</h1>
            </header>
            <v-btn
            to="/login"
            color="#E6AF2E"
            dark
            class="pl-10 pr-10"
            >log in</v-btn>
        </section>
    </v-container>
</template>

<style scoped>
    .main-blue {
        background: #3D348B;
        color: #fff;
    }

    .hero h1 {
        font-size: 56px;
    }
</style>
