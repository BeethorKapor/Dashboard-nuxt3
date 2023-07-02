<template>
    <v-app>
        <core-drawer />
        <core-app-bar />
        <core-view>
            <slot></slot>
        </core-view>
    </v-app>
</template>

<style>

@font-face {
font-family: 'Phetsarath_OT'; 
src: url('../assets/fonts/Phetsarathwebfonts/phetsarath_ot.eot'); 
src: url('@/assets/fonts/Phetsarathwebfonts/phetsarath_ot.eot?#iefix') format('embedded-opentype'), 
url('@/assets/fonts/Phetsarathwebfonts/phetsarath_ot.woff2') format('woff2'), 
url('@/assets/fonts/Phetsarathwebfonts/phetsarath_ot.woff') format('woff'), 
url('@/assets/fonts/Phetsarathwebfonts/phetsarath_ot.ttf') format('truetype'),
url('@/assets/fonts/Phetsarathwebfonts/phetsarath_ot.svg#Phetsarath_OT') format('svg'); 
font-weight: normal;
font-style: normal; 
}
*{ 
font-family:Phetsarath_OT;
}

.main {
  background-color: #e0e5eb;
  color: black;
}
</style>