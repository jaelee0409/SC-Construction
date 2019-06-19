<template>
    <v-container fluid pa-0>
        <v-container fluid mt-5 px-0 pt-3 pb-0 class="hidden-sm-and-down">
                <v-tabs grow color="blue-grey lighten-4">
                    <v-tab class="font-weight-bold subheading" active-class="teal lighten-3" v-for="n in tabs" :key="n.id" @click="onClick(n.id)">
                        {{ n.title }}
                    </v-tab>
                </v-tabs>
                <v-timeline class="pa-5 blue-grey lighten-5">
                    <v-timeline-item v-for="i in 3" :key="i" color="red darken-3">
                        <template v-slot:opposite>
                            <span>Date</span>
                        </template>
                        <v-card class="elevation-4">
                            <v-card-title class="headline">{{ i }}</v-card-title>
                            <v-card-text>
                                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
                            </v-card-text>
                        </v-card>
                    </v-timeline-item> 
                </v-timeline>
        </v-container>

        <v-container fluid pa-0 class="hidden-xs-only hidden-md-and-up">
            <v-card class="mt-5 pt-2 elevation-16" height="auto">
                <v-tabs grow color="blue-grey lighten-4">
                    <v-tab class="font-weight-bold subheading" active-class="teal lighten-3" v-for="n in tabs" :key="n.id" @click="onClick(n.id)">
                        {{ n.title }}
                    </v-tab>
                </v-tabs>
                <v-timeline class="pa-4 blue-grey lighten-5">
                    <v-timeline-item v-for="i in 3" :key="i" color="red darken-3">
                        <template v-slot:opposite>
                            <span>Date</span>
                        </template>
                        <v-card class="elevation-4">
                            <v-card-title class="headline">{{ i }}</v-card-title>
                            <v-card-text>
                                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
                            </v-card-text>
                        </v-card>
                    </v-timeline-item> 
                </v-timeline>
            </v-card>
        </v-container>

        <v-container fluid pa-0 class="hidden-sm-and-up">
            <v-card class="mt-5 pt-2 pb-5 elevation-16 blue-grey lighten-5" height="auto">
                <v-tabs grow color="blue-grey lighten-4">
                    <v-tab class="font-weight-bold" active-class="teal lighten-3" v-for="t in tabs" :key="t.id" @click="onClick(t.id)">
                        {{ t.title }}
                    </v-tab>
                </v-tabs>
                <v-card v-for="t2 in 3" :key="t2" class="elevation-4 pa-3 ma-4">
                    <v-card-title class="headline">Company name</v-card-title>
                    <v-card-text>
                        Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
                    </v-card-text>
                </v-card>
            </v-card>
        </v-container>
    </v-container>
</template>

<script>
export default {
    name: 'projects',
    data() {
        return {
            currentTab: 0,
            tabs: [
                { title: 'Ground Up Buildings', id: 0, count: 3 },
                { title: 'Finish-outs', id: 1, count: 10 },
                { title: 'Current Projects', id: 2, count: 3 }
            ]
        }

    },
    methods: {
        onClick(id) {
            console.log('Current tab re-clicked:' + id);
        }
    }
}
</script>

<style>
</style>
