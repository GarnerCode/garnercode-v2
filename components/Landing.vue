<template>
    <section id="landing">
        <h1>Hi, I'm <span class="text-highlight">Tyler</span></h1>
        <p>I work with Vue to develop complex user-interfaces and web applications.</p>
        <a href="#contact" class="button button-primary">Contact</a>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #landing {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 2rem;
            h1, p {
                text-align: center;
            }
            h1 {
                opacity: 0;
                transform: translateY(1rem);
                animation: fadeInUp 0.5s ease 0.75s forwards;
            }
            p, a {
                opacity: 0;
                animation: fadeIn 0.5s ease 1.5s forwards;
            }
        }
    }
    @media screen and (min-width: 768px) {
        #landing {
            p {
                width: 450px;
            }
        }
    }
</style>