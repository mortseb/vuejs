<script setup></script>

<template>
    <button :class="buttonClass" @click="onClick">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'ButtonComponent',
    props: {
        text: {
            type: String,
            default: 'Button'
        },
        type: {
            type: String,
            default: 'primary'
        }
    },
    computed: {
        buttonClass() {
            switch (this.type) {
                case 'primary':
                    return 'bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded';
                case 'secondary':
                    return 'bg-gray-500 hover:bg-gray-700 text-white font-bold py-2 px-4 rounded';
                case 'danger':
                    return 'bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded';
                // Ajoutez d'autres types de boutons ici
                default:
                    return 'bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded';
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


