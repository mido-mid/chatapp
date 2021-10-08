<template>
    <div class="chat-app">
        <Conversation :contact="SelectedContact" :messages="messages"/>
        <contact-list :contacts="contacts"/>
    </div>
</template>

<script>
    import Conversation from "./Conversation";
    import ContactList from "./ContactList";
    export default {
        data: function(){
            return {
                SelectedContact: null,
                contacts: [],
                messages: [],
            }
        },
        components: {ContactList, Conversation},
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
