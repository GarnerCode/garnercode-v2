<template>
    <div id="layout">
        <Header></Header>
        <main>
            <Nuxt />
        </main>
        <Footer></Footer>
    </div>
</template>

<style lang="scss">
    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(1rem);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    :root {
        --color-primary: #2AE98D;
        --color-black: #1D1D1F;
        --color-black-alt: #313133;
        --color-white: #FBFBFD;
        --color-alt-white: #F2F2F2;
        --font-family-primary: 'Rubik', sans-serif;
        --font-family-secondary: 'Red Hat Mono', sans-serif;
        --border-radius: 6px;
        --transition: all ease 0.3s;
    }
    * {
        font-family: var(--font-family-secondary);
        color: var(--color-white);
    }
    html {
        overflow-x: hidden;
        scroll-behavior: smooth;
    }
    body {
        margin: 0;
        background-color: var(--color-black);
    }
    h1, h2, h3, p {
        margin: 0;
    }
    h1, h2, h3 {
        font-family: var(--font-family-primary);
        span {
            font-family: var(--font-family-primary);
        }
    }
    .section-pb {
        padding-bottom: 15rem;
        padding-top: 1rem;
    }
    .section-header {
        margin-bottom: 2rem;
        letter-spacing: 2px;
        text-align: center;
    }
    .text-highlight {
        color: var(--color-primary);
    }
    @media screen and (min-width: 0px) {
        h1 {
            font-size: 3rem;
        }
        h2 {
            font-size: 2.5rem;
        }
        h3 {
            font-size: 2rem;
        }
        p {
            font-size: 1.25rem;
            line-height: 2rem;
        }
        section {
            padding: 0 2rem;
        }
        button, .button {
            display: block;
            background: none;
            border: 1px solid var(--color-white);
            border-radius: var(--border-radius);
            font-size: 1.5rem;
            color: var(--color-white);
            padding: 8px 32px;
            transition: var(--transition);
            text-decoration: none;
            text-align: center;
            width: fit-content;
            cursor: pointer;
            &:hover {
                background-color: var(--color-white);
                color: var(--color-black);
                transform: translateY(-5px);
                box-shadow: 5px 5px 0 black;
            }
            &.button-primary {
                border: 1px solid var(--color-primary);
                &:hover {
                    background-color: var(--color-primary);
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        section {
            padding: 0 4rem;
        }
    }
    @media screen and (min-width: 1024px) {
        section {
            padding: 0 12rem;
        }
    }
    @media screen and (min-width: 1180px) {
        section {
            padding: 0 15rem;
        }
    }
    @media screen and (min-width: 1440px) {
        h1 {
            font-size: 5rem;
        }
        h2 {
            font-size: 3rem;
        }
        section {
            padding: 0 20rem;
        }
    }
    @media screen and (min-width: 1920px) {
        section {
            padding: 0 30rem;
        }
    }
</style>