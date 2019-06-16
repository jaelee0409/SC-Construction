<template>
    <v-container fluid class="pa-0">
        <div class="py-5 blue-grey lighten-3" id="aboutUs">
            <h1 class="mt-5 text-xs-center">About Us</h1>
            <v-divider class="my-4"></v-divider>
            <v-container :class="{'px-5 mb-5': $vuetify.breakpoint.mdAndUp}">
                <blockquote :class="{'blockquote headline': $vuetify.breakpoint.mdAndUp}">SC Construction Company was founded in 1995 by Sung Cho who is serving as the president of Korean American Chamber of Commerce in Austin and the director of Asian Contractor Association of Austin (<a href="http://acta-austin.com">acta-austin.com</a>) currently.</blockquote>
                <blockquote :class="{'blockquote headline': $vuetify.breakpoint.mdAndUp}">We will strive to implement a long term relationship with our clients, based on safety, quality, timely service and an anticipation of their needs. To fulfill this mission, we will treat all employees fairly and involve them in the quality improvement process to insure responsiveness and cost effective work execution. We value the importance of our relationships and will continue to remain fair and true in our dealings with all employees, clients, vendors, and partners.</blockquote>
                <blockquote :class="{'blockquote headline': $vuetify.breakpoint.mdAndUp}">For more than a decade, SC Construction has been doing General Contracting, Construction Management and Design/Build offering construction services in terms of various industrial, manufacturing, office, retail, and commercial projects in the Greater Austin Metro Area.</blockquote>
                <blockquote :class="{'blockquote headline': $vuetify.breakpoint.mdAndUp}">Construction is a people management business. SC's goal is to work within a team atmosphere with the owner, project stakeholders, designers, subcontractors, and suppliers to achieve a quality and timely project for the mutual benefit of everyone on the team. We take great pride in our accomplishments and build on them every day.</blockquote>
            </v-container>
        </div>
        <div class="py-5 orange accent-3 text-xs-center" id="statement">
            <h1>Mission Statement</h1>
            <v-divider class="my-4"></v-divider>
            <v-container :class="{'px-5': $vuetify.breakpoint.mdAndUp}">
                <div class="display-2">To deliver high-quality, cost-effective projects on schedule by employing and supporting motivated, flexible and focused teams.</div>
            </v-container>
        </div>
        <div class="py-5 blue-grey lighten-5 text-xs-center" id="objectives">
            <h1>Our Objectives</h1>
            <v-divider class="my-4"></v-divider>
            <v-container :class="{'px-5': $vuetify.breakpoint.mdAndUp}">
                <v-layout row wrap>
                    <v-flex v-for="i in 3" :key="`4${i}`" xs4>
                        In Progress
                    </v-flex>
                </v-layout>
            </v-container>
        </div>
        <div class="py-5 blue-grey lighten-4 text-xs-center" id="values">
            <h1>Our Values</h1>
            <v-divider class="my-4"></v-divider>
            <v-container :class="{'px-5': $vuetify.breakpoint.mdAndUp}">
                <v-layout row wrap>
                    <v-flex v-for="i in 3" :key="`4${i}`" xs4>
                        In Progress
                    </v-flex>
                    <v-flex v-for="i in 2" :key="`6${i}`" xs6>
                        In Progress
                    </v-flex>
                </v-layout>
            </v-container>
        </div>
    </v-container>
</template>

<script>
export default {
}
</script>

<style>
</style>
