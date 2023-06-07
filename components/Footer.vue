<template>
    <footer>
        <div class="columns">
            <div class="logo">
                GarnerCode<span class="text-highlight">.io</span>
            </div>
            <ul class="nav-list">
                <li v-for="(nav, index) of navItems" :key="index">
                    <a :href="nav.route">{{ nav.label }}</a>
                </li>
            </ul>
            <div class="social">
                <a href="https://github.com/GarnerCode" target="_blank">Github</a>
                <a href="https://www.linkedin.com/in/tgarner98/" target="_blank">LinkedIn</a>
            </div>
        </div>
        <p>© {{ getYear() }} Tyler Garner</p>
    </footer>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        footer {
            padding: 0 2rem;
            .columns {
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 2rem;
            }
            .logo {
                font-size: 1.5rem;
                text-align: center;
                color: var(--color-white);
            }
            .nav-list {
                list-style: none;
                padding: 0;
                margin: 0;
                display: flex;
                flex-direction: column;
                gap: 2rem;
                li {
                    width: fit-content;
                    margin: 0 auto;
                }
                a {
                    font-size: 1rem;
                    text-decoration: none;
                    transition: var(--transition);
                    &:hover {
                        color: var(--color-primary);
                    }
                }
            }
            .social {
                display: flex;
                flex-direction: row;
                justify-content: center;
                gap: 2rem;
                a {
                    transition: var(--transition);
                    &:hover {
                        color: var(--color-primary);
                    }
                }
            }
            p {
                text-align: center;
                font-size: 1rem;
                font-size: 12px;
                margin-top: 2rem;
            }
        }
    }
    @media screen and (min-width: 768px) {
        footer {
            .nav-list {
                flex-direction: row;
                justify-content: center;
                li {
                    margin: 0;
                }
            }
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { navItems } from '~/const/navItems';

    export default defineComponent({
        name: 'Footer',
        data: () => {
            return {
                navItems,
            }
        },
        methods: {
            getYear(): number {
                const year = new Date().getFullYear();
                return year;
            }
        }
    })
</script>