<template>
    <v-container fluid>
        <v-card flat color="grey-lighten-3" v-bind="$attrs" v-on="$listeners">
            <v-list-item>
                <v-layout>
                    <v-icon size="48" color="blue">{{ icon }}</v-icon>
                    <v-spacer></v-spacer>
                    <v-btn icon class="bg-grey-lighten-3" flat>
                        <v-icon>mdi-dots-vertical</v-icon>
                    </v-btn>
                </v-layout>
                <v-list-item-title class=" py-3 text-blue">{{
                    title
                }}</v-list-item-title>
                <v-list-item-subtitle>
                    <v-layout>
                        <span>{{ fileCount }}</span>
                        <v-spacer></v-spacer>
                        <b>{{ fileSize }}</b>
                    </v-layout>
                </v-list-item-subtitle>
            </v-list-item>
        </v-card>
    </v-container>
</template>

<script lang="ts">
export default {
    name: "CardBox",

    inheritAttrs: false,
    props: {
        title: { type: String, default: "UnTitle" },
        fileSize: { type: String, default: "0" },
        fileCount: { type: String, default: "0" },
        icon: { type: String, default: "mdi-folder-open-outline" },
    },
};
</script>

<style lang="scss" scoped></style>
