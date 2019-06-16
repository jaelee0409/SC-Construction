<template>
    <v-container fluid class="pa-0 ma-0" id="hero_container">
        <!-- Photo by Verne Ho on Unsplash -->
        <v-parallax :src="require('@/assets/hero.jpg')" height="/* */" id="hero_image">
            <v-layout align-center justify-center class="px-5 text-xs-center">
                <v-card white class="elevation-24" id="hero_card">
                    <div :class="{'ma-3 px-2 display-1 font-weight-bold font-italic': $vuetify.breakpoint.mdAndUp,
                        'px-2 py-2 headline font-weight-bold font-italic': $vuetify.breakpoint.smAndDown}">
                        "BUILDING TRUST IN BUSINESS RELATIONSHIPS"
                    </div>
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
    background-color: rgba(178, 133, 108, 0.95);
    border-radius: 12px;
}
</style>

