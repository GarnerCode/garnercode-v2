<template>
    <section id="tech" class="section-pb">
        <h2 class="section-header">Skills & Experience</h2>
        <div class="section-content">
            <div class="tech-container">
                <div class="tech" v-for="(tech, index) of techList" :key="index">
                    <div class="icon-container">
                        <img :src="tech.imageUrl" :alt="`${tech.label} logo`">
                    </div>
                    <p class="label">{{ tech.label }}</p>
                </div>
            </div>
            <div class="experience-container">
                <div class="experience">
                    <p class="date">2022 - 2023</p>
                    <div class="details">
                        <p class="title">Junior Front-End Developer</p>
                        <a class="company" href="https://www.runwayproptech.com/" target="_blank">Runway Proptech</a>
                        <p class="summary">Worked alongside UI designer and QA team to develop and debug client applications and consumer-facing websites for multiple corporations including Howard Hughes and Disney.</p>
                        <ul class="tech-list">
                            <li>TypeScript</li>
                            <li>Angular</li>
                            <li>Vue</li>
                            <li>Sass</li>
                            <li>Bulma</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="button-container">
                <a href="https://drive.google.com/file/d/139KydJAvsLkpU2kU7fc9Nb8spMbqozbb/view?usp=sharing" target="_blank" class="button button-primary">View Resume</a>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #tech {
            h2 {
                text-align: center;
            }
            .tech-container {
                display: flex;
                flex-direction: column;
                gap: 2rem;
            }
            .tech {
                display: grid;
                grid-template-columns: 30px 1fr;
                gap: 2rem;
                background-color: var(--color-black-alt);
                border-radius: var(--border-radius);
                padding: 8px 32px;
                border-right: 10px solid var(--color-primary);
                .label {
                    font-size: 1.5rem;
                }
                .icon-container {
                    width: 30px;
                    height: 30px;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    img {
                        width: 100%;
                    }
                }
            }
            .experience-container {
                margin-top: 5rem;
            }
            .experience {
                padding: 8px 32px;
                background-color: var(--color-black-alt);
                border-radius: var(--border-radius);
                .date {
                    font-size: 1rem;
                }
                .title {
                    font-size: 1.25rem;
                    font-family: var(--font-family-primary);
                    color: var(--color-primary);
                }
                .company {
                    margin-bottom: 1rem;
                    font-size: 1.25rem;
                    line-height: 2rem;
                    transition: var(--transition);
                    &:hover {
                        color: var(--color-primary);
                    }
                }
                .summary {
                    font-size: 1rem;
                }
                .tech-list {
                    list-style: none;
                    padding: 0;
                    margin: 0;
                    display: flex;
                    flex-direction: row;
                    flex-wrap: wrap;
                    margin-top: 1rem;
                    gap: 1rem;
                    li {
                        background-color: var(--color-black);
                        border-radius: var(--border-radius);
                        padding: 5px;
                    }
                }
            }
            .button-container {
                margin-top: 2rem;
                .button {
                    margin: 0 auto;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        #tech {
            .tech-container {
                display: grid;
                grid-template-columns: 1fr 1fr;
            }
            .experience {
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                background: none;
                padding: 0;
                border-radius: 0;
                .date {
                    padding-top: 8px;
                    width: 30rem;
                }
                .details {
                    background-color: var(--color-black-alt);
                    padding: 8px 32px;
                    border-radius: var(--border-radius);
                }
            }
            .button-container {
                display: flex;
                flex-direction: row;
                justify-content: flex-end;
                .button {
                    margin: 0;
                }
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #tech {
            .experience {
                .date {
                    padding-top: 8px;
                    width: 20rem;
                }
            }
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { techList } from '~/const/techList';

    export default defineComponent({
        name: 'Tech',
        data: () => {
            return {
                techList,
            }
        }
    })
</script>