<template>
    <v-container fluid pa-0>
        <v-container fluid mt-5 px-0 pt-3 pb-0 class="hidden-sm-and-down">
            <v-tabs grow color="blue-grey lighten-3">
                <v-tab class="subheading font-weight-bold" active-class="teal lighten-2" v-for="n in tabs" :key="n.id" v-on:click="currentTab = n.id">
                    {{ n.title }}
                </v-tab>
            </v-tabs>
            <v-timeline class="pa-3 blue-grey lighten-4">
                <v-timeline-item v-for="(i, index) in tabs[currentTab].count" :key="i" color="#CD5C5C">
                    <template v-slot:opposite>
                        <span class="title font-weight-medium">{{ projects[currentTab][index].completionDate }}</span>
                    </template>
                    <v-card class="ma-3 elevation-24">
                        <v-carousel v-if="projects[currentTab][index].numPics > 0" height="auto">
                            <v-carousel-item v-for="(p, cur) in projects[currentTab][index].numPics" :key="p" :src="projects[currentTab][index].src[cur]">
                            </v-carousel-item>
                        </v-carousel>
                        <v-card-title class="py-3 justify-center projectTitle headline font-weight-bold">{{ projects[currentTab][index].name }}</v-card-title>
                        <v-card-text class="subheading font-weight-regular">
                            <div class="pa-1"><b>Address:</b> {{ projects[currentTab][index].address }}</div>
                            <div class="pa-1"><b>Size:</b> {{ projects[currentTab][index].size }} ft&sup2;</div>
                            <div class="pa-1" v-if="projects[currentTab][index].contractAmount"><b>Contract Amount:</b> {{ projects[currentTab][index].contractAmount }}</div>
                            <div class="pa-1"><b>Architect:</b> {{ projects[currentTab][index].architect }}</div>
                            <div class="pa-1"><b>Contact:</b> {{ projects[currentTab][index].contact }}</div>
                            <div class="pa-1"><b>Tel:</b> {{ projects[currentTab][index].tel }}</div>
                            <div class="pa-1" v-if="projects[currentTab][index].fax">
                                <b>Fax:</b> {{ projects[currentTab][index].fax }}
                            </div>
                            <div class="pa-1"><b>Job Description:</b> {{ projects[currentTab][index].jobDescription }}</div>
                        </v-card-text>
                    </v-card>
                </v-timeline-item> 
            </v-timeline>
        </v-container>

        <v-container fluid pa-0 class="hidden-xs-only hidden-md-and-up">
            <v-card class="mt-5 pt-2 elevation-16" height="auto">
                <v-tabs grow color="blue-grey lighten-4">
                    <v-tab class="font-weight-bold subheading" active-class="teal lighten-3" v-for="n in tabs" :key="n.id" v-on:click="currentTab = n.id">
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
                    <v-tab class="font-weight-bold" active-class="teal lighten-3" v-for="t in tabs" :key="t.id" v-on:click="currentTab = n.id">
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
            ],
            projects: [
                [
                    { name: 'KoMiCo Technology, Inc.', size: '15,000', contact: 'Mike Sykora | Operations Director', tel: '(512)-238-2400', fax: '(512)-238-2498', address: '201 Michael Angelo Way, Austin, TX 78728', architect: 'FTC Architect', contractAmount: '$1,494,901.76', completionDate: 'July 10, 2013', jobDescription: 'New Building Expansion, Logistics, Electrical, Mechanical, Plumbing, Fire Systems, Elevator, Chemical Storage, Warehouse, Parking Lot, Concrete Foundation, ADA Ramps, Sidewalks, Landscaping', numPics: 3, src: [require('@/assets/komiko3.jpg'), require('@/assets/komiko4.jpg'), require('@/assets/komiko5.jpg')] },

                    { name: 'KoMiCo Technology, Inc.', size: '1,600', contact: 'Mike Sykora | Operations Director', tel: '(512)-238-2400', fax: '(512)-238-2498', address: '201 Michael Angelo Way, Austin, TX 78728', architect: 'FTC Architect', contractAmount: '$173,489.00', completionDate: 'April 12, 2012', jobDescription: 'New Building for Truck Loading Dock, Electrical, Mechanical, Fire Systems, Concrete Foundation, ADA Ramps, Sidewalks, Trucking Driveway, Landscaping, Light Poles', numPics: 3, src: [require('@/assets/komiko0.jpg'), require('@/assets/komiko1.jpg'), require('@/assets/komiko2.jpg')] },

                    { name: 'Sam Squared Technologies, Inc.', size: '36,000', contact: 'Min Ho Tan | Owner', tel: '(512)-977-8041', fax: '(512)-517-3985', address: '9007 Tuscany Way, Austin, TX 78754', architect: 'RFG Architect', contractAmount: '$4,190,000.00', completionDate: 'May 25, 2011', jobDescription: 'New Building for Industrial and Commercial, Site Development(8 Acres), Fab Room, Electrical, Mechanical, Plumbing, Fire System, Parking Lot, Concrete Foundation, ADA Ramps, Sidewalks, Landscaping' },
                ],
                [
                    { name: 'W by Azwell, Inc.', size: '10,000', contact: 'Stephen Yeah | Owner', tel: '(601)-918-5104, (901)-861-0309', fax: '(601)-919-1101', address: '4948 Merchants Park Cir Ste 1000, Collierville, TN 38017', architect: 'NaNeMone Interior Design', completionDate: 'September 11, 2011', jobDescription: 'New Store, Tenant Improvement', numPics: 2, src: [require('@/assets/azwell0.jpg'), require('@/assets/azwell2.jpg')] },

                    { name: 'W by Azwell, Inc.', size: '8,500', contact: 'Stephen Yeah | Owner', tel: '(601)-918-5104, (901)-861-0309', fax: '(601)-919-1101', address: '132 Market St, Flowood, MS 39110', architect: 'Woodridge & Associates', completionDate: 'November 15, 2010', jobDescription: 'New Store, Tenant Improvement', numPics: 3, src: [require('@/assets/azwell1.jpg'), require('@/assets/azwell3.jpg'), require('@/assets/azwell4.jpg')] },

                    { name: 'YoGo Sweet Yogurt', size: '2,000', contact: 'Jung Kim | Owner', tel: '(512)-924-4917', address: '12854 US Hwy 183 N, Austin, TX 78750', architect: 'McCann and Associates', completionDate: 'August 21, 2010', jobDescription: 'New Store, Tenant Improvement, Finish-Out', numPics: 5, src: [require('@/assets/yogo0.jpg'), require('@/assets/yogo1.jpg'), require('@/assets/yogo2.jpg'), require('@/assets/yogo3.jpg'), require('@/assets/yogo4.jpg')] },

                    { name: 'Berkeley Academy', size: '1,800', contact: 'James Seo | Owner', tel: '(512)-968-7571', address: '9707 Anderson Mill Rd Ste 330, Austin, TX 78750', architect: 'McCann and Associates', completionDate: 'August 7, 2010', jobDescription: 'New Store, Tenant Improvement, Finish-Out', numPics: 7, src: [require('@/assets/berkeley0.jpg'), require('@/assets/berkeley1.jpg'), require('@/assets/berkeley2.jpg'), require('@/assets/berkeley3.jpg'), require('@/assets/berkeley4.jpg'), require('@/assets/berkeley5.jpg'), require('@/assets/berkeley6.jpg')] },

                    { name: 'Umiya Japanese Restaurant', size: '1,800', contact: 'Sang Han | Owner', tel: '(512)-797-8618', address: '1540 Cypress Creek Rd 106, Austin, TX 78613', architect: 'McCann and Associates', completionDate: 'April 3, 2010', jobDescription: 'New Store, Tenant Improvement, Finish-Out', numPics: 7, src: [require('@/assets/umiya0.jpg'), require('@/assets/umiya1.jpg'), require('@/assets/umiya2.jpg'), require('@/assets/umiya3.jpg'), require('@/assets/umiya4.jpg'), require('@/assets/umiya5.jpg'), require('@/assets/umiya6.jpg')] },

                    { name: "YoYo's Frozen Yogurt", size: '3,000', contact: 'Dona Kim | Owner', tel: '(254)-371-3018', address: '1335 E Whitestone Blvd, Cedar Park, TX 78613', architect: 'McCann and Associates', completionDate: 'October 9, 2009', jobDescription: 'New Store, Tenant Improvement, Finish-Out', numPics: 8, src: [require('@/assets/yoyo0.jpg'), require('@/assets/yoyo1.jpg'), require('@/assets/yoyo2.jpg'), require('@/assets/yoyo3.jpg'), require('@/assets/yoyo4.jpg'), require('@/assets/yoyo5.jpg'), require('@/assets/yoyo6.jpg'), require('@/assets/yoyo7.jpg')] },

                    { name: 'Yanagi Japanese Restaurant', size: '4,300', contact: 'Pyung Yang | Owner', tel: '(512)-363-9179', address: '4404 W William Cannon Dr Ste B, Austin, TX 78749', architect: 'McCann and Associates', completionDate: 'June 15, 2009', jobDescription: 'New Store, Tenant Improvement, Finish-Out', numPics: 6, src: [require('@/assets/yanagi0.jpg'), require('@/assets/yanagi1.jpg'), require('@/assets/yanagi2.jpg'), require('@/assets/yanagi3.jpg'), require('@/assets/yanagi4.jpg'), require('@/assets/yanagi5.jpg')] },

                    { name: 'Seoul Garden Restaurant', size: '2,700', contact: 'Young Park | Owner', tel: '(512)-917-6141', fax: 'N/A', address: '9616 N Lamar, Austin, TX 70753', architect: 'McCann and Associates', completionDate: 'May 7, 2009', jobDescription: 'New Store, Tenant Improvement, Finish-Out', numPics: 3, src: [require('@/assets/seoulgarden0.jpg'), require('@/assets/seoulgarden1.jpg'), require('@/assets/seoulgarden2.jpg')] },

                    { name: 'Austin Kuk Sool Won', size: '4,000', contact: 'Byung Lee | Owner, Grand Master', tel: '(512)-619-2344', fax: 'N/A', address: '13584 Pond Springs Rd, Austin, TX 78729', architect: 'McCann and Associates', completionDate: 'February 1, 2009', jobDescription: 'Building Expansion, Finish-Out' },

                    { name: 'Buffet Palace', size: '2,500', contact: 'Sam Shim | Owner', tel: '(512)-694-2999', fax: 'N/A', address: '4608 Westgate Blvd, Austin, TX 78745', architect: 'FTC Architect', completionDate: 'October 21, 2008', jobDescription: 'Finish-Out' },
                ],
                [
                    { name: 'JSMILEHEART, INC.', size: '6,000', contact: 'Jaewoo Jang | Owner', tel: '(512)-541-0579', address: '2500 W Parmer Ln Ste 100, Austin, TX 78757', architect: 'ARCH Woo Associates, LLC', jobDescription: 'New Store, Tenant Improvement' },

                    { name: 'Berkeley2 Academy', size: '3,600', contact: 'Jason Hong | Owner', tel: '(512)-968-7571, (512)-347-7575', address: '12871 N US-183 Hwy Ste 100, Austin, TX 78750', architect: 'NaNeMone Interior Design', jobDescription: 'New Office, Remodeling' },

                    { name: 'OSIO SUSHI, Inc.', size: '600', contact: 'Hye Lee | Owner', tel: '(512)-906-7100', address: '2901 S Capital of Texas Hwy H-20, Austin, TX 78746', architect: 'Architectura SA, Inc.', jobDescription: 'New Store, Tenant Improvement' },
                ]
            ]
        }

    }
}
</script>

<style>
.projectTitle {
    background-color: #CD5C5C;
}

.v-tabs__container {
    height: 50px;
}
</style>
