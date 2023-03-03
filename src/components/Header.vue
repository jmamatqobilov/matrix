<template>
    <v-app-bar :elevation="0" class="navbar" style="width: 100%;">
        <div class="container" style="width: 100%;">
            <div style="display: flex;justify-content: space-between;">
                <div class="header-left">
                    <img :src="require('../assets/logo.svg')" />
                </div>
                <div class="header-right">
                    <div class="header-search">
                        <span>o</span>
                        <input class="header-input" type="text" placeholder="Find what interests you">
                    </div>
                    <div class="header-terminal">
                        <span>
                            Terminal ES
                        </span>
                        <button>
                            k
                        </button>
                    </div>
                    <div class="header-premium">
                        Get Premium
                    </div>
                    <div class="header-profile">
                        <img :src="require('../assets/profhead.svg')" />
                        <img :src="require('../assets/profbody.svg')" />
                    </div>
                    <div class="header-notif">
                        
                    </div>
                </div>
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
.navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
}

.header-notif {
    width: 40px;
    height: 40px;
    background: #FFFFFF;
    border-radius: 6px;
}

.header-profile {
    width: 40px;
    height: 40px;
    background: #FFFFFF;
    border-radius: 6px;
    margin-right: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.header-premium {
    width: 158px;
    height: 40px;
    box-sizing: border-box;
    background: #F9ED35;
    border-radius: 6px;
    margin-right: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}

.header-terminal {
    width: 150px;
    height: 40px;
    box-sizing: border-box;
    background-color: #FFFFFF;
    border-radius: 6px;
    margin-right: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}

.header-terminal button {
    margin-left: 8px;
}

.header-search {
    width: 340px;
    height: 40px;
    box-sizing: border-box;
    background: #FFFFFF;
    opacity: 0.2;
    border-radius: 6px;
    display: flex;
    align-items: center;
    padding: 5px;
    margin-right: 12px;
}

.header-search input {
    padding-left: 5px;
    border: none;
    outline: none;
}

::-moz-placeholder,
::placeholder,
::-webkit-input-placeholder {
    font-weight: 400;
    font-size: 12px;
    line-height: 25px;
    letter-spacing: -0.149625px;
    color: #ffffff;
    background-color: #FFFFFF;
}

.header-right {
    display: flex;
    align-items: center;

}

.container {
    padding: 60px;
}

.navbar {
    border-bottom-left-radius: 42px;
    background: linear-gradient(261.11deg, #77CABA 0%, #229A87 90.84%);
}
</style>
  