<template>
    <v-container fluid class="pa-0">
        <div class="py-5 blue-grey lighten-4  hidden-xs-only">
            <h4 class="mt-5 pt-4 display-1 font-weight-bold text-xs-center">Contact Us</h4>
            <v-divider class="my-4"></v-divider>
            <v-layout class="mb-5 pt-4 text-xs-center">
                <v-layout justify-end>
                    <v-flex mr-5 xs12 class="title font-weight-regular text-xs-right">
                        <p>Tel: (512)-238-3061</p>
                        <p>Fax: (512) 655-2101</p>
                        <p>Cell: (512)-773-0001</p>
                    </v-flex>
                </v-layout>
                <v-layout>
                    <v-flex ml-5 xs12 class="title font-weight-regular text-xs-left">
                        <p>Email: <a href="mailto:773sung@gmail.com" id="emailLink">773sung@gmail.com</a></p>
                        <p>Mail: 15046 Jacks Pond Rd</p>
                        <p>Austin, TX 78728</p>
                    </v-flex>
                </v-layout>
            </v-layout>
            <p class="mt-5 title font-weight-regular text-xs-center">Got a question? We'd love to hear from you.</p>
            <p class="title font-weight-regular text-xs-center"> Send us a message and we'll respond as soon as possible.</p>
            <v-container class="px-5">
                <form action="https://formspree.io/jaelee0409@gmail.com" method="POST">
                    <v-container class="px-5">
                        <v-layout row justify-center>
                            <v-flex pa-0 xs10>
                                <v-text-field background-color="blue-grey lighten-5"
                                              :rules="nameRules"
                                              label="Name"
                                              type="text"
                                              name="name"
                                              required box browser-autocomplete>
                                </v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout row justify-center>
                            <v-flex pa-0 xs10>
                                <v-text-field background-color="blue-grey lighten-5" 
                                              :rules="emailRules"
                                              label="E-mail"
                                              type="email"
                                              name="_replyto"
                                              required box browser-autocomplete>
                                </v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout row justify-center>
                            <v-flex pa-0 xs10>
                                <v-text-field background-color="blue-grey lighten-5"
                                              :rules="messageRules"
                                              label="Message"
                                              height="300"
                                              name="message"
                                              required box clearable>
                                </v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout mt-3 justify-center>
                            <v-btn large round type="submit">Send Message</v-btn>
                        </v-layout>
                    </v-container>
                </form>
            </v-container>
        </div>
        <div class="py-5 blue-grey lighten-4 hidden-sm-and-up">
            <h4 class="mt-5 pt-4 display-1 font-weight-bold text-xs-center">Contact Us</h4>
            <v-divider class="my-4"></v-divider>
            <v-layout class="pt-5 text-xs-center">
                <v-flex xs12>
                    <p class="title font-weight-light">Tel: 512.238.3061</p>
                    <p class="title font-weight-light">Fax: 512.655.2101</p>
                    <p class="title font-weight-light">Cell: 512.773.0001</p>
                    <p class="title font-weight-light"><a href="mailto:773sung@gmail.com" id="emailLink">773sung@gmail.com</a></p>
                    <p class="title font-weight-light">15046 Jacks Pond Rd<br>Austin, TX 78728</p>
                </v-flex>
            </v-layout>
            <v-container mt-5 pa-0>
                <form action="https://formspree.io/jaelee0409@gmail.com" method="POST">
                    <v-container pa-0>
                        <v-layout row justify-center>
                            <v-flex pa-0 xs8>
                                <v-text-field background-color="brown lighten-5"
                                              :rules="nameRules"
                                              label="Name"
                                              type="text"
                                              name="name"
                                              required box browser-autocomplete>
                                </v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout row justify-center>
                            <v-flex pa-0 xs8>
                                <v-text-field background-color="brown lighten-5" 
                                              :rules="emailRules"
                                              label="E-mail"
                                              type="email"
                                              name="_replyto"
                                              required box browser-autocomplete>
                                </v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout row justify-center>
                            <v-flex pa-0 xs8>
                                <v-text-field background-color="brown lighten-5"
                                              :rules="messageRules"
                                              label="Message"
                                              height="200"
                                              name="message"
                                              required box clearable>
                                </v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout justify-center>
                            <v-btn round type="submit">Send Message</v-btn>
                        </v-layout>
                    </v-container>
                </form>
            </v-container>
        </div>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            nameRules: [v => !!v || "Name is required"],
            emailRules: [
                v => !!v || "E-mail is required",
                v => /.+@.+/.test(v) || "E-mail must be valid"
            ],
            messageRules: [v => !!v || "Message is required"]
        };
    },
}
</script>

<style>
#emailLink {
    text-decoration: none;
}
</style>
