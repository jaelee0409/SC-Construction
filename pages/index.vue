<template>
    <v-container fluid class="pa-0 ma-0" id="hero_container">
        <!-- Photo by Verne Ho on Unsplash -->
        <v-parallax :src="require('@/assets/hero.jpg')" height="/* */" id="hero_image">
            <v-layout align-center justify-center class="text-xs-center">
                <v-card white class="ma-5 elevation-24" id="hero_card">
                    <h1 class="display-1 font-weight-black mx-4 px-4 black--text">BUILDING TRUST IN BUSINESS RELATIONSHIPS</h1>
                </v-card>
            </v-layout>
        </v-parallax>
    </v-container>
</template>

<script>
export default {
}
</script>

<style>
#hero_container {
    height: 100%;
}

#hero_image {
    height: 100%;
}

.v-parallax__image {
    bottom: -100px;
}

#hero_card {
    background-color: rgba(255, 255, 255, 0.9);
}
</style>

