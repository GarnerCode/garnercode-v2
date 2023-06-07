<template>
    <section id="portfolio" class="section-pb">
        <h2 class="section-header">Portfolio</h2>
        <div class="portfolio-content">
            <div class="project" v-for="(project, index) of projects" :key="index">
                <img class="project-img" :src="project.imageUrl" :alt="`${project.title} thumbnail`">
                <div class="project-details">
                    <div class="details-text">
                        <p class="title">{{ project.title }}</p>
                        <p class="summary">{{ project.description }}</p>
                        <ul class="tech-list">
                            <li v-for="(tech, index) of project.tech" :key="index">
                                {{ tech }}
                            </li>
                        </ul>
                    </div>
                    <div class="buttons">
                        <a class="button button-primary" :href="project.liveUrl" target="_blank">Visit Site</a>
                        <a class="button small" :href="project.gitUrl" target="_blank">View Code</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #portfolio {
            .portfolio-content {
                display: flex;
                flex-direction: column;
                gap: 5rem;
            }
            .project-img {
                width: 100%;
                border-radius: var(--border-radius);
            }
            .title {
                font-size: 1.5rem;
                color: var(--color-primary);
            }
            .summary {
                font-size: 1rem;
            }
            .buttons {
                display: flex;
                flex-direction: column;
                gap: 1rem;
                margin-top: 1rem;
                .small {
                    font-size: 1rem;
                }
            }
            .tech-list {
                list-style: none;
                padding: 0;
                margin: 0;
                display: flex;
                flex-direction: row;
                flex-wrap: wrap;
                gap: 1rem;
                margin-top: 1rem;
                li {
                    background-color: var(--color-black-alt);
                    border-radius: var(--border-radius);
                    padding: 5px;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        #portfolio {
            .project {
                display: flex;
                flex-direction: row;
                gap: 2rem;
            }
            .project-details {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
            }
            .project-img {
                width: 300px;
                height: 300px;
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #portfolio {
            .project-img {
                width: 350px;
                height: 350px;
            }
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { projects } from '~/const/projects';

    export default defineComponent({
        name: 'Portfolio',
        data: () => {
            return {
                projects,
            }
        }
    })
</script>