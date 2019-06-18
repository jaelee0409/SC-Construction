<template>
    <v-container fluid class="pa-0">
        <div class="py-5 blue-grey lighten-3">
            <h4 class="mt-5 pt-4 display-1 font-weight-bold text-xs-center">About Us</h4>
            <v-divider class="my-4"></v-divider>
            <v-container class="hidden-xs-only" id="aboutUsDesktop">
                <div class="mx-5 px-5 headline font-weight-light">
                    <p class="mb-4">SC Construction Company was founded in 1995 by Sung Cho who is serving as the president of Korean American Chamber of Commerce in Austin and the director of Asian Contractor Association of Austin (<a href="http://acta-austin.com">acta-austin.com</a>) currently.</p>
                    <p class="mb-4">We will strive to implement a long term relationship with our clients, based on safety, quality, timely service and an anticipation of their needs. To fulfill this mission, we will treat all employees fairly and involve them in the quality improvement process to insure responsiveness and cost effective work execution. We value the importance of our relationships and will continue to remain fair and true in our dealings with all employees, clients, vendors, and partners.</p>
                    <p class="mb-4">For more than a decade, SC Construction has been doing General Contracting, Construction Management and Design/Build offering construction services in terms of various industrial, manufacturing, office, retail, and commercial projects in the Greater Austin Metro Area.</p>
                    <p class="mb-4">Construction is a people management business. SC's goal is to work within a team atmosphere with the owner, project stakeholders, designers, subcontractors, and suppliers to achieve a quality and timely project for the mutual benefit of everyone on the team. We take great pride in our accomplishments and build on them every day.</p>
                </div>
            </v-container>
            <v-container class="hidden-sm-and-up">
                <div class="subheading font-weight-light text-xs-center">
                    <p class="mb-4">SC Construction Company was founded in 1995 by Sung Cho who is serving as the president of Korean American Chamber of Commerce in Austin and the director of Asian Contractor Association of Austin (<a href="http://acta-austin.com">acta-austin.com</a>) currently.<p>
                    <p class="mb-4">We will strive to implement a long term relationship with our clients, based on safety, quality, timely service and an anticipation of their needs. To fulfill this mission, we will treat all employees fairly and involve them in the quality improvement process to insure responsiveness and cost effective work execution. We value the importance of our relationships and will continue to remain fair and true in our dealings with all employees, clients, vendors, and partners.</p>
                    <p class="mb-4">For more than a decade, SC Construction has been doing General Contracting, Construction Management and Design/Build offering construction services in terms of various industrial, manufacturing, office, retail, and commercial projects in the Greater Austin Metro Area.</p>
                    <p>Construction is a people management business. SC's goal is to work within a team atmosphere with the owner, project stakeholders, designers, subcontractors, and suppliers to achieve a quality and timely project for the mutual benefit of everyone on the team. We take great pride in our accomplishments and build on them every day.</p>
                </div>
            </v-container>
        </div>
        <div class="py-5 orange accent-3 text-xs-center" id="statement">
            <h4 class="display-1 font-weight-bold">Mission Statement</h4>
            <v-divider class="my-4"></v-divider>
            <v-container class="px-5 pb-5 hidden-xs-only">
                <div class="display-2 font-weight-light">To deliver high-quality, cost-effective projects on schedule by employing and supporting motivated, flexible and focused teams.</div>
            </v-container>
            <v-container class="hidden-sm-and-up">
                <div class="display-1 font-weight-light">To deliver high-quality, cost-effective projects on schedule by employing and supporting motivated, flexible and focused teams.</div>
            </v-container>
        </div>
        <div class="py-5 blue-grey lighten-5 text-xs-center" id="objectives">
            <h4 class="display-1 font-weight-bold text-xs-center">Our Objectives</h4>
            <v-divider class="my-4"></v-divider>
            <v-container class="pb-5 hidden-xs-only">
                <v-layout row wrap>
                    <v-flex v-for="i in objectives" xs4>
                        <div class="px-3 headline font-weight-light">
                            {{ i.text }}
                        </div>
                    </v-flex>
                </v-layout>
            </v-container>
            <v-container class="hidden-sm-and-up">
                <v-layout row wrap>
                    <v-flex v-for="i in objectives" xs12>
                        <div class="mb-3 subheading font-weight-light">
                            {{ i.text }}
                        </div>
                        <br>
                    </v-flex>
                </v-layout>
            </v-container>
        </div>
        <div class="py-5 blue-grey lighten-4 text-xs-center" id="values">
            <h4 class="display-1 font-weight-bold text-xs-center">Our Values</h4>
            <v-divider class="my-4"></v-divider>
            <v-container class="px-5 hidden-xs-only">
                <v-layout row justify-center wrap>
                    <v-flex v-for="i in values" xs4>
                        <div class="my-4">
                            <v-icon size="50" class="ma-2">{{ i.icon }}</v-icon>
                            <h5 class="mb-3 headline font-weight-medium">{{ i.title }}</h5>
                            <p class="px-3 pt-2 pb-5 subheading font-weight-light">{{ i.text }}</p>
                        </div>
                    </v-flex>
                </v-layout>
            </v-container>
            <v-container class="hidden-sm-and-up">
                <v-layout row wrap>
                    <v-flex v-for="i in values" xs12>
                        <div class="mb-5">
                            <v-icon size="30" class="ma-2">{{ i.icon }}</v-icon>
                            <h5 class="headline font-weight-medium">{{ i.title }}</h5>
                            <p class="px-3 pt-2 subheading font-weight-light">{{ i.text }}</p>
                        </div>
                    </v-flex>
                </v-layout>
            </v-container>
        </div>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            objectives: [
                {
                    text: 'To perform for our customers the highest level of quality construction services at fair and market competitive prices.'
                },
                {
                    text: 'To ensure the longevity of our company through repeat and referral business achieved by customer satisfaction in all areas including timeliness, attention to detail and service-minded attitudes.'
                },
                {
                    text: 'To maintain the highest levels of professionalism, integrity, honesty and fairness in our relationships with our suppliers, subcontractors, professional associates and customers.'
                }
            ],
            values: [
                {
                    title: 'Trust', text: 'We place trust at the center of every relationship - with customers, subcontractors, suppliers, architects, engineers and fellow team members.', icon: 'lock'
                },
                {
                    title: 'Teamwork', text: 'People are our greatest strength. SC people work with customers and business partners in a spirit of collaboration and trust to tackle the challenges of construction.', icon: 'people'
                },
                {
                    title: 'Responsibility', text: 'We are responsible to team members, customers, subcontractors, suppliers, architects, engineers and the communities in which we live and work.', icon: 'child_friendly'
                },
                {
                    title: 'Safety', text: 'We are committed to eliminating all worker injury. Every SC team member and every customer, subcontractor, supplier, architect and engineer can expect that our work sites place their personal safety as our highest priority.', icon: 'security'
                },
                {
                    title: 'Service', text: 'We embrace a customer service culture. We believe our future is secured by advancing the interests and success of our customers.', icon: 'favorite'
                }
            ]
        }
    } 
}
</script>

<style>
#aboutUsDesktop {
    text-indent: 45px;
}
</style>
