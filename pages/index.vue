<template>
    <v-container fluid>
        <v-row>
            <v-col>
                <v-layout>
                    <h3 class="text-grey-darken-1">ແຟ້ມເອກະສານ</h3>
                    <v-spacer></v-spacer>
                    <v-btn icon flat>
                        <v-icon>mdi-arrow-right</v-icon>
                    </v-btn>
                </v-layout>
            </v-col>
        </v-row>
        <v-divider />
        <v-row>
            <v-col>
                <card-box title="ເອກະສານເຂົ້າທັງໜົດ" fileCount="14 Files" fileSize="200 MB" />
            </v-col>
            <v-col>
                <card-box title="ເອກະສານອອກທັງໜົດ" fileCount="14 Files" fileSize="200 MB" />
            </v-col>
            <v-col>
                <card-box title="ເອກະສານອອກທັງໜົດ" fileCount="14 Files" fileSize="200 MB" />
            </v-col>
        </v-row>
        <v-row>
            <v-col>
                <v-layout wrap>
                    <h3 class="pt-3 title text-grey-darken-1">ເອກະສານຫຼ້າສຸດ</h3>
                    <v-spacer></v-spacer>
                    <v-btn icon flat>
                        <v-icon>mdi-arrow-right</v-icon>
                    </v-btn>
                </v-layout>
                <v-list>
                    
                    <v-list-item v-for="(item, i) in itemRecents" :key="i">
                        <template #prepend>
                            <v-icon size="large">{{ item.icon }}</v-icon>
                            <v-list-item-title>{{ item.title }}</v-list-item-title>
                            <v-list-item-subtitle>{{ item.subTitle }}</v-list-item-subtitle>
                            <v-list-item-action>
                                <small>
                                    {{ item.size }}
                                </small>
                            </v-list-item-action>
                        </template>
                    </v-list-item>
                </v-list>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import CardBox from '~/components/CardBox'
export default {
    components: {
        CardBox,
    },
    data: () => ({
        itemRecents: [
            {
                icon: 'mdi-folder-open-outline',
                title: 'Text',
                subTitle: 'image...',
                size: '2 MB'
            },
            {
                icon: 'mdi-folder-open-outline',
                title: 'Text',
                subTitle: 'image...',
                size: '2 MB'
            },

        ]
    }),

};
</script>
