<script setup>
import { ref, onMounted } from 'vue'
import { RouterLink } from 'vue-router'

const themes = [
    { name: 'light', icon: '🌞' },
    { name: 'dark', icon: '🌚' },
    { name: 'cupcake', icon: '🧁' },
    { name: 'bumblebee', icon: '🐝' },
    { name: 'emerald', icon: '💚' },
    { name: 'corporate', icon: '🏢' },
    { name: 'synthwave', icon: '🌃' },
    { name: 'halloween', icon: '🎃' },
    { name: 'forest', icon: '🌲' },
    { name: 'lofi', icon: '🎧' },
    { name: 'pastel', icon: '🩷' },
    { name: 'night', icon: '🌙' },
    { name: 'coffee', icon: '☕' },
    { name: 'dracula', icon: '🧛‍♂️' },
]

const selectedTheme = ref(localStorage.getItem('theme') || 'light')

const setTheme = (theme) => {
    selectedTheme.value = theme
    document.documentElement.setAttribute('data-theme', theme)
    localStorage.setItem('theme', theme)
}

onMounted(() => {
    setTheme(selectedTheme.value)
})
</script>



<template>
    <div class="navbar bg-base-300 shadow-md">

        <!-- Logo Section - With Logo-->
        <!-- <div class="flex flex-1 pl-5">
            <div class="flex items-center">
                <RouterLink to="/" class="bg-primary rounded-md">
                    <img alt="Kura Ninja logo" class="logo hover:animate-pulse" src="@/assets/logo-remove-bg-io.png" width="50" />
                </RouterLink>
                <div class="divider divider-horizontal"></div>
                <div>
                    <div class="flex-col">
                        <div class="flex-col">Kura-</div>
                        <div class="flex-col">Ninja</div>
                    </div>
                </div>
            </div>
        </div>         -->

        <!-- Logo Section - Without Logo -->
        <div class="flex flex-1 pl-5">
            <div class="font-mono font-black">Ini</div>
            <div class="font-mono font-thin">Logo</div>
        </div>

        <!-- Navigation Links -->
        <div class="flex flex-1 justify-center">
            <nav>
                <RouterLink to="/" class="btn btn-ghost">Home</RouterLink>
                <RouterLink to="/about" class="btn btn-ghost">About</RouterLink>
            </nav>
        </div>

        <!-- Theme Selector -->
        <div class="flex flex-1 justify-end">
            <div class="dropdown dropdown-end">
                <div tabindex="0" role="button" class="btn m-1 capitalize">
                    {{themes.find(t => t.name === selectedTheme)?.icon}}
                    {{ selectedTheme }}
                </div>
                <ul tabindex="0" class="dropdown-content menu bg-base-100 rounded-box z-[1] w-52 p-2 shadow-sm">
                    <li v-for="theme in themes" :key="theme.name">
                        <a @click="setTheme(theme.name)" class="capitalize">
                            <span class="mr-2">{{ theme.icon }}</span>
                            {{ theme.name }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>




    </div>
</template>
