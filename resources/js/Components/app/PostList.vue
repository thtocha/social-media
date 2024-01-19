<script setup>
import PostItem from "@/Components/app/PostItem.vue";
    const post1 = {
        user: {
            id: 1,
            avatar: 'https://randomuser.me/api/portraits/lego/1.jpg',
            name: 'Ilon Musk',
        },
        group: null,
        attachments: [
            {
                id: 1,
                name: 'test.png',
                url: 'https://picsum.photos/1000',
                mime: 'image/png'
            },
            {
                id: 2,
                name: 'test2.png',
                url: 'https://picsum.photos/1000',
                mime: 'image/png'
            },
            {
                id: 3,
                name: 'MyDocument.docx',
                url: '#',
                mime: 'application/msword'
            }
        ],
        body:
            `
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut commodi dolores eos et exercitationem facere, fugit illo laboriosam nostrum tempore? A dolor ipsam odio officia quaerat! Nihil nobis rerum veritatis.</p>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut commodi dolores eos et exercitationem facere, fugit illo laboriosam nostrum tempore? A dolor ipsam odio officia quaerat! Nihil nobis rerum veritatis.</p>
            `,
        created_at: '2024-01-11 11:33'
    }
    const post2 = {
        user: {
            id: 2,
            avatar: 'https://randomuser.me/api/portraits/lego/2.jpg',
            name: 'Mark Shadow',
        },
        group: {
            id: 1,
            name: 'Laravel developers'
        },
        body:
            `
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut commodi dolores eos et exercitationem facere, fugit illo laboriosam nostrum tempore? A dolor ipsam odio officia quaerat! Nihil nobis rerum veritatis.</p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut commodi dolores eos et exercitationem facere, fugit illo laboriosam nostrum tempore? A dolor ipsam odio officia quaerat! Nihil nobis rerum veritatis.</p>
                `,
        created_at: '2024-02-22 22:22'
    }

    defineProps({
        posts: Array
    })
</script>

<template>
    <div class="flex-1 overflow-auto">
        <PostItem v-for="post of posts" :key="post.id" :post="post"/>
    </div>
</template>

<style scoped>

</style>
