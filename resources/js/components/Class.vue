<template>
    <v-container>
        <v-card color="basil" style="margin-bottom: 20px;">
            <v-card-title class="text-center justify-center py-6">
            </v-card-title>

            <v-tabs
                background-color="transparent"
                color="white"
                grow
                v-model="tab"
            >
                <v-tab

                    style="color:white;font-size: 100%"
                    :key="item.name"
                    v-for="item in items"

                >

                        {{ item.name }}


                </v-tab>
            </v-tabs>

            <v-tabs-items v-model="tab">
                <v-tab-item>
                    <v-card style="padding-bottom: 10%;padding-top:5%">
                        <Information></Information>
                    </v-card>
                </v-tab-item>
                <v-tab-item>
                    <v-card style="padding: 10%;padding-top:0%">
                        <Announcement></Announcement >
                    </v-card>
                </v-tab-item>
                <v-tab-item>
                    <v-card style="padding: 10%;padding-top:0%">
                        <Assaignment></Assaignment>
                    </v-card>
                </v-tab-item>
                <v-tab-item>
                    <v-card style="padding: 10%;padding-top:5%;padding-bottom: 1000%">
                        <Student></Student>
                    </v-card>
                </v-tab-item>
                <v-tab-item>
                    <v-card style="padding: 10%;padding-top:5%;padding-bottom: 1000%">
                        <Exam></Exam>
                    </v-card>
                </v-tab-item>
            </v-tabs-items>
        </v-card>


    </v-container>

</template>
<script>
    import invite_dilog from "./invite_dilog";
    import dilog from './Material_dilog.vue';
    import Information from "./Information.vue";
    import Announcement from "./Announcement.vue";
    import Assaignment from "./Assaignment.vue";
    import Student from "./Student.vue";
    import Exam from "./Exam.vue";

    export default {

        components: {dilog, invite_dilog,Information,Announcement,Assaignment,Student,Exam},
        data() {
            return {
                tab: null,
                items: [
                    {
                        name: 'INFORMATION',
                        to: '/information',
                    },
                    {
                        name: 'ANNOUNCEMENTS',
                        to: '/announcement',

                    },
                    {
                        name: 'ASSIGNMENTS',
                        to: '/assignment',

                    },
                    {
                        name: 'STUDENTS',
                        to: '/student',

                    },
                    {
                        name: 'Exam',
                        to: '/discussion'
                    },

                ],
                desserts: [
                    {
                        name: 'Class Name:',
                        calories: 'Physics-107',
                    },
                    {
                        name: 'Section:',
                        calories: '1',
                    },
                    {
                        name: 'created on:',
                        calories: '20th Auugust 2019',
                    },
                    {
                        name: 'Class Code:',
                        calories: '7g58df41',
                    },


                ],

            }
        },
    }
</script>
<style>
    /* Helper classes */
    .basil {
        background-color: #b380ff !important;
    }

    .basil--text {
        color: white !important;
    }
</style>
