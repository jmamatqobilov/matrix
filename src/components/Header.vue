<template>
    <v-app-bar :elevation="0" class="navbar">
        <div class="container">
            <div class="navbar-container">
                <div class="">
                    <img :src="require('../assets/logo.svg')" />
                </div>
                <v-spacer></v-spacer>
                <input type="text" placeholder="dfdsdsfdf">
            </div>
        </div>
    </v-app-bar>
</template>
  
<script>

export default {
    name: 'Header',
}
</script>

<style scoped>
.container {
    padding: 60px;
}

.navbar {
    border-bottom-left-radius: 42px;
    background: linear-gradient(261.11deg, #77CABA 0%, #229A87 90.84%);
}


.navbar-container {
    display: flex;
    
}
</style>
  