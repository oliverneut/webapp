<template>
    <div class="contact" >
        <ContactForm/>
    </div>
</template>

<script>
    import ContactForm from '../components/ContactForm'

    export default {
        name: 'Contact',
        components: {
            ContactForm
        }
    }
</script>

<style scoped>

    *{
        color: white;
    }
</style>