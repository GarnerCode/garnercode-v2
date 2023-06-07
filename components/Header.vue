<template>
    <header>
        <div class="logo">GarnerCode<span class="text-highlight">.io</span></div>
        <ul class="nav-list">
            <li v-for="(nav, index) of navItems" :key="index">
                <a :href="nav.route">{{ nav.label }}</a>
            </li>
        </ul>
    </header>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        header {
            position: absolute;
            top: 0;
            left: 0;
            padding: 0 2rem;
            width: calc(100vw - 4rem);
            height: 60px;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            opacity: 0;
            animation: fadeIn 0.5s ease 0.25s forwards;
            .logo {
                font-size: 1.5rem;
                font-family: var(--font-family-primary);
                color: var(--color-white);
                span {
                    font-family: var(--font-family-primary);
                }
            }
            .nav-list {
                display: none;
            }
        }
    }
    @media screen and (min-width: 768px) {
        header {
            padding: 0 4rem;
            width: calc(100vw - 8rem);
            .nav-list {
                list-style: none;
                padding: 0;
                margin: 0;
                display: flex;
                flex-direction: row;
                gap: 1.5rem;
                a {
                    text-decoration: none;
                    transition: var(--transition);
                    &:hover {
                        color: var(--color-primary);
                    }
                }
            }
        }
    }
    @media screen and (min-width: 1024px) {
        header {
            padding: 0 12rem;
            width: calc(100vw - 24rem);
        }
    }
    @media screen and (min-width: 1180px) {
        header {
            padding: 0 15rem;
            width: calc(100vw - 30rem);
        }
    }
    @media screen and (min-width: 1440px) {
        header {
            padding: 0 20rem;
            width: calc(100vw - 40rem);
        }
    }
    @media screen and (min-width: 1920px) {
        header {
            padding: 0 30rem;
            width: calc(100vw - 60rem);
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { navItems } from '~/const/navItems';

    export default defineComponent({
        name: 'Header',
        data: () => {
            return {
                navItems,
            }
        }
    })
</script>