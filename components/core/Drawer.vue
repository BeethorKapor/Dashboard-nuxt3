<template>
    <v-navigation-drawer id="app-drawer" v-model="inputValue" width="260" elevation="5" floating>
        <v-list-item class="text-center" two-line>
            <v-avatar color="white">
                <v-img
                    src="https://cdn.vuetifyjs.com/docs/images/logos/vuetify-logo-v3-light.svg"
                    height="34"
                    contain
                />
            </v-avatar>

            <v-list-item-title class="title">ລະບົບຈັດການຫ້ອງການ</v-list-item-title>
        </v-list-item>

        <v-divider class="mx-3 mb-3" />

        <v-list density="compact" nav variant="flat">
            <v-list-item v-for="(link, i) in links" :key="i" :to="link.to" active-class="primary white--text" active-color="indigo-darken-4">
                <template #prepend>
                    <v-icon size="large">{{ link.icon }}</v-icon>
                </template>
                <v-list-item-title class="pt-3 pb-3" style="font-size: 18px">{{ link.text }}</v-list-item-title>
            </v-list-item>
        </v-list>

        
    </v-navigation-drawer>
</template>

<script>
// Utilities

import { mapActions, mapState } from 'pinia';
import { useAppStore } from '../../stores/app';

export default {
    data: () => ({
        links: [
            {
                to: '/',
                icon: 'mdi-view-dashboard',
                text: 'ໜ້າຫຼັກ',
            },
            {
                to: '/Manage-staff',
                icon: 'mdi-account-group',
                text: 'ຈັດການຂໍ້ມູນພະນັກງານ',
            },
            {
                to: '/file-cabinet',
                icon: 'mdi-file-cabinet',
                text: 'ຈັດການຕູ້ເກັບເອກະສານ',
            },
            {
                to: '/documents',
                icon: 'mdi-file-document-multiple',
                text: 'ຈັດການເອກະສານ',
            },
            
            {
                to: '/maps',
                icon: 'mdi-map-marker', 
                text: 'ທີ່ຕັ້ງ',
            },
            {
                to: '/setting',
                icon: 'mdi-cog',
                text: 'ການຕັ້ງຄ່າ',
            },
        ],
    }),
    computed: {
        ...mapState(useAppStore, ['color']),
        inputValue: {
            get() {
                return useAppStore().drawer;
            },
            set(val) {
                this.setDrawer(val);
            },
        },
    },

    methods: {
        ...mapActions(useAppStore, ['setDrawer', 'toggleDrawer']),
    },
};
</script>


