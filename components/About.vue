<template>
    <section id="about" class="section-pb">
        <h2 class="section-header">About</h2>
        <div class="about-content">
            <img class="headshot" src="images/headshot.webp" alt="Tyler Garner headshot">
            <div class="about-paragraphs">
                <p>My name is Tyler Garner. I am a front-end web developer that specializes in Vue. With over 5 years of web development experience, I am proficient in developing complex user-interfaces and web applications.</p>
                <p>As my focus is in front-end, I utilize the open-source service Supabase when back-end code and databases are necessary in order to develop full-stack websites and applications.</p>
                <p>When I'm not coding, you can find me writing campaigns for Dungeons & Dragons, or staying active with paintball.</p>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #about {
            .headshot {
                width: 100%;
                border-radius: var(--border-radius);
                margin-bottom: 2rem;
            }
            p {
                margin-bottom: 2rem;
                font-size: 1rem;
            }
        }
    }
    @media screen and (min-width: 768px) {
        #about {
            .about-content {
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                gap: 2rem;
            }
            .headshot {
                width: 15rem;
                height: 15rem;
            }
        }
    }
</style>