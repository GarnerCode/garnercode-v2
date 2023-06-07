<template>
    <section id="contact" class="section-pb">
        <h2 class="section-header">Contact</h2>
        <form action="https://getform.io/f/607da9e8-ff5a-4f71-9905-0979b0840530" method="POST">
            <div class="field">
                <div class="label-container">
                    <label for="name">Name</label>
                </div>
                <input type="text" name="name">
            </div>
            <div class="field">
                <div class="label-container">
                    <label for="email">Email</label>
                </div>
                <input type="email" name="email">
            </div>
            <div class="field">
                <div class="label-container">
                    <label for="name">Message</label>
                </div>
                <textarea name="message"></textarea>
            </div>
            <div class="field">
                <button class="button-primary">Submit</button>
            </div>
        </form>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #contact {
            form {
                background-color: var(--color-black-alt);
                padding: 8px 32px;
                border-radius: var(--border-radius);
                width: calc(100% - 4rem);
                display: flex;
                flex-direction: column;
                gap: 1rem;
                .label-container {
                    margin-bottom: 0.5rem;
                    label {
                        font-size: 1.25rem;
                    }
                }
                .field {
                    width: 100%;
                }
                input, textarea {
                    background-color: var(--color-black);
                    color: var(--color-white);
                    font-size: 16px;
                    font-family: var(--font-family-primary);
                    padding: 8px;
                    border: none;
                    border-radius: var(--border-radius);
                    resize: none;
                    width: calc(100% - 16px);
                    &:focus {
                        outline: none;
                    }
                }
                textarea {
                    height: 10rem;
                }
                button {
                    margin: 0 auto;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        #contact {
            form {
                width: 25rem;
                margin: 0 auto;
            }
        }
    }
</style>