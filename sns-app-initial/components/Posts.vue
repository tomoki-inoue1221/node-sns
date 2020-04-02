<template>
	<div>
		<div class="posts overflow-scroll mb-24">
			<post v-for="(post,index) in posts" :post="post.content" :key="index" :user="post.user" :is-liked="post.isLiked"/>
		</div>
	</div>
</template>

<script>
	import Post from '~/components/Post.vue'

	export default {
		components: {
			Post
		},
		data() {
			return {
				posts: [
				{
					user: {
						displayName: 'anna0609',
						photoURL: '/images/post1.jpg'
					},
					content: {
						text: '渋谷なうだぜーい',
						image: '/images/post0.jpg'
					},
					isLiked: true
				},
				{
					user: {
						displayName: 'tomoki1221',
						photoURL: '/images/post0.jpg'
					},
					content: {
						text: '渋谷なうだぜーい',
						image: '/images/post1.jpg'
					},
					isLiked: false
				}
				]
			}
		}
	}
</script>