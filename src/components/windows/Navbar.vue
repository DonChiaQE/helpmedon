<template>
<nav class="navbar-container">
    <div alt="start" class="start-menu" v-on:click="$store.commit('setActiveWindow', 'Menu')" :class="$store.getters.getActiveWindow=='Menu' ? 'start-menu-depressed' : 'start-menu'">
        <div class="" :class="$store.getters.getActiveWindow=='Menu' ? 'border' : 'container-border'">
            <img class="start-icon" src="https://i.imgur.com/0hcVoV2.png"/>
                <button style="padding-left: 3px; font-size: 0.9rem; font-weight: bold;"></button>
                </div>
        </div>
    
    <div class="spacer"></div>

<div class="spotify-player">
    <iframe style="border-radius:12px" 
            src="https://open.spotify.com/embed/playlist/1xINbJobcTdfnGaJIQNRTM?utm_source=generator&theme=0" 
            width="100%" 
            height="152" 
            frameBorder="0" 
            allowfullscreen="" 
            allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
            loading="lazy">
    </iframe>
</div>
</nav>
</template>

<style scoped>
/*-------------------------------------------*\
    Container
\*-------------------------------------------*/

.navbar-container {
    width: 100%;
    height: 50px;
    background: #292829;
    border-top: solid #292829 2px;
    z-index: 100;
    display: flex;
    flex-direction: row;
    align-items: center;
}

/*-------------------------------------------*\
    Navbar Items
\*-------------------------------------------*/

.navbar-item {
    width: 100px;
    height: 28px;
    border-radius: 10px;
    margin-left: 2px;
    margin-right: 2px;
    box-shadow: 1.5px 1.5px black;
    border-top: solid rgb(250, 250, 250) 1.5px;
    border-left: solid rgb(250, 250, 250) 1.5px;
    border-bottom: solid rgb(90, 90, 90) 1.5px;
    border-right: solid rgb(90, 90, 90) 1.5px;
    background: rgb(192, 192, 192);
    border-radius: 0.5px;
    display: flex;
    justify-content: flex-start;
    align-items: center !important;
    padding-left: 5px;
    padding-right: 5px;
    font-weight: bold;
    font-size: 0.7rem;
    padding-top: 2px;
}

.navbar-item:active {
    background: rgb(192, 192, 192);
    box-shadow: none;
    border-top: solid rgb(0, 0, 0) 1.5px;
    border-left: solid rgb(0, 0, 0) 1.5px;
    border-bottom: solid rgb(250, 250, 250) 1.5px;
    border-right: solid rgb(250, 250, 250) 1.5px;
}

.navbar-item:hover {
    cursor: pointer;
}

.navbar-item-depressed {
    width: 100px;
    height: 28px;
    border-radius: 10px;
    margin-left: 2px;
    margin-right: 2px;
    border-radius: 0.5px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding-left: 5px;
    padding-right: 5px;
    font-weight: bold;
    font-size: 0.7rem;
    background: rgb(192, 192, 192);
    box-shadow: none;
    background: repeating-conic-gradient(rgb(189, 190, 189) 0% 25%, rgb(255, 255, 255) 0% 50%) 50% / 2px 2px;
    border-top: solid rgb(0, 0, 0) 1.5px;
    border-left: solid rgb(0, 0, 0) 1.5px;
    border-bottom: solid rgb(250, 250, 250) 1.5px;
    border-right: solid rgb(250, 250, 250) 1.5px;
    padding-top: 2px;
}

.start-icon {
    width: 60px;
    height: 50px;
}

.start-menu {
    width: 70px;
    margin: 1px;
    height: 50px;
    box-shadow: 1.5px 1.5px rgb(65, 63, 63);
    border-top: solid rgb(83, 81, 81) 1.5px;
    border-left: solid rgb(83, 80, 80) 1.5px;
    border-bottom: solid rgb(79, 76, 76) 1.5px;
    border-right: solid rgb(74, 73, 73) 1.5px;
    background: #3e3d3e;

    display: flex;
    /* justify-content: space-between; */
    justify-content: center;
    align-items: center;
}

.start-menu:hover {
    cursor: pointer;
}

.start-menu:active {
    background: rgb(192, 192, 192);
    box-shadow: none;
    border-top: solid rgb(0, 0, 0) 1.5px;
    border-left: solid rgb(0, 0, 0) 1.5px;
    border-bottom: solid rgb(250, 250, 250) 1.5px;
    border-right: solid rgb(250, 250, 250) 1.5px;
}

.start-menu-depressed {
    box-shadow: none;
    background: repeating-conic-gradient(rgb(189, 190, 189) 0% 25%, rgb(255, 255, 255) 0% 50%) 
              50% / 2px 2px;
    border-top: solid rgb(0, 0, 0) 1.5px;
    border-left: solid rgb(0, 0, 0) 1.5px;
    border-bottom: solid rgb(250, 250, 250) 1.5px;
    border-right: solid rgb(250, 250, 250) 1.5px;
}

.container-border {
    display: flex;
    justify-content: center;
    align-items: center;
}

.border {
    display: flex;
    justify-content: center;
    align-items: center;
    border: black dotted 1px;
}

/*-------------------------------------------*\
    Utilities
\*-------------------------------------------*/


.spotify-player {
    width: 20%;
    height: 150px;
    position: relative;
    top: -50px;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    border: none;
    overflow: hidden;
}

.spacer {
    flex-grow: 1;
}

.time {
    width: 100px;
    margin: 1px;
    height: 50px;
    background: rgb(192, 192, 192);
    border-right: solid rgb(250, 250, 250) 1.5px;
    border-bottom: solid rgb(250, 250, 250) 1.5px;
    border-top: solid rgb(90, 90, 90) 1.5px;
    border-left: solid rgb(90, 90, 90) 1.5px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    font-size: 0.6em;
}

@media only screen and (max-width: 700px) { 
    .time {
        width: auto !important; 
        padding-left: 5px;
        padding-right: 5px;
    }
    .icon-image {
        width: 0px;
        height: 0px;
        margin-right: 0px;
    }
    .navbar-item {
        width: auto;
        padding-top: 0;
    }

    .navbar-item-depressed {
        width: auto;
        padding-top: 0;
    }
}

/*-------------------------------------------*\
    CSS Normalisation 
\*-------------------------------------------*/

button {
    background: none;
    color: inherit;
    border: none;
    font: inherit;
    outline: inherit;
}

p {
    margin: 0;
    padding: 0;
}
</style>

<script>
import moment from 'moment'
export default {
    name: 'Navbar',
    data: function () {
        return {
            activeWindows: this.$store.getters.getActiveWindows,

            // date time for moment.js
            time: '',
            date: ''
        }
    },
    beforeMount() {
        setInterval(() => {
            this.time = moment().format('hh:mm A')
        }, 1000)
        setInterval(() => {
            this.date = moment().format('ddd DD MMMM')
        }, 1000)
    },
    methods: {
        openWindow(windowId) {
            const payload = {
                'windowState': 'open',
                'windowID': windowId
            }
            this.$store.commit('setWindowState', payload)
        },
    }
}
</script>
