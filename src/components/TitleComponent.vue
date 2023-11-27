<script setup></script>

<template>
    <button :class="buttonClass" @click="onClick">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'TitleComponent',
    props: {
        text: {
            type: String,
            default: 'Titre'
        },
        type: {
            type: String,
            default: 'h2'
        }
    },
    computed: {
        buttonClass() {
            switch (this.type) {
                case 'h1':
                    return 'text-3xl';
                case 'h2':
                    return 'text-2xl';
                case 'h3':
                    return 'text-xl';
                default:
                    return 'text-3xl';
            }
        }
    },
    methods: {
        onClick() {
            this.$emit('click');
        }
    }
}
</script>


