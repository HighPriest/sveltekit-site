/// <reference path="@types/tryghost__content-api" />

<script lang="ts">
    import GhostContentAPI from '@tryghost/content-api';
    //import GhostContentAPI from '@types/tryghost__content-api';
    
    
    const api = new GhostContentAPI({
        url: 'http://localhost:2368',
        key: '862c158e70ce6fb7c02323a223',
        version: "v3"
    });

    api.posts.browse({limit: 5, include: ['tags','authors']})
        .then((posts) => {
            console.log(posts);
            //return {props: {posts: posts}}
        }).catch((err) => {
            console.log(err);
        });
</script>

<main>
    Hello world
    <!--{#each posts as post}
        <li><a href="/posts/{post.slug}">{post.title}</a></li>
    {/each}-->
</main>