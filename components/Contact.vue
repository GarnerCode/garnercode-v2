<template>
    <section id="contact" class="section-pb">
        <h2 class="section-header">Contact</h2>
        <form action="https://getform.io/f/607da9e8-ff5a-4f71-9905-0979b0840530" method="POST">
            <div class="field">
                <div class="label-container">
                    <label for="name">Name</label>
                </div>
                <input v-model="formData.name" type="text" name="name">
            </div>
            <div class="field">
                <div class="label-container">
                    <label for="email">Email</label>
                </div>
                <input v-model="formData.email" type="email" name="email">
            </div>
            <div class="field">
                <div class="label-container">
                    <label for="name">Message</label>
                </div>
                <textarea v-model="formData.message" name="message"></textarea>
            </div>
            <div class="field">
                <button :disabled="submitDisabled" class="button-primary">Submit</button>
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
                    &:disabled {
                        color: var(--color-black);
                        border: 1px solid var(--color-black);
                        cursor: default;
                        &:hover {
                            background: none;
                            transform: translateY(0);
                            box-shadow: none;
                        }
                    }
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

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'Contact',
        data: () => {
            return {
                formData: {
                    name: '',
                    email: '',
                    message: '',
                },
                submitDisabled: true,
            }
        },
        watch: {
            'formData': {
                handler: function(val) {
                    if (val) {
                        if (this.formData.name !== '' && 
                        this.formData.email !== '' && 
                        this.formData.message !== '') {
                            this.submitDisabled = false;
                        } else {
                            this.submitDisabled = true;
                        }
                    }
                },
                deep: true,
            }
        }
    })
</script>