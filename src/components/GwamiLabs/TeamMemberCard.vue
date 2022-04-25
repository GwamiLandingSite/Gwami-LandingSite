<template>
    <div class="card">
        <div class="card-body">
            <a :href="require(`../assets/PageThree/${image}`)">Test</a>
            <img :src="require(`../assets/PageThree/${image}`)" alt="image-photo"/>
            <span>{{name}}</span>
            <span>{{credentials}}</span>
            <a :href="twitter">
                <TwitterBird />
            </a>
            
        </div>
    </div>
</template>
<script>
import TwitterBird from "./icons/TwitterBird.vue";
export default {
    name: "TeamMemberCard",
    props: {
        image: String,
        name: String,
        credentials: String,
        twitter: String,
    },
    components: { TwitterBird },
}
</script>