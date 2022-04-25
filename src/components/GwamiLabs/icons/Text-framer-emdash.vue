<template>
    <svg width="24" height="2" viewBox="0 0 24 2" fill=none xmlns="http://www.w3.org/2000/svg">
    <path d="M0 1H24" stroke={{color}} stroke-width="2"/>
    </svg>
</template>
<script>
    export default {
        name: "textFramerEmDash",
        props:{
            color: {
                type: String,
                default: "#000000",
                }
        },
    }
</script>
