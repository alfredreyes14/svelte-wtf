<script>
	import * as prismicH from '@prismicio/client'

	export let slice;

	const reverse = slice.slice_label === 'emoji_right';
  const serializer = {
    paragraph: ({ children }) => `<p>${children}</p>`
  }
</script>

<div>
	<article class:reverse>
		<div class="emoji">{slice.primary.emoji[0].text}</div>
		<div class="text">
			{@html prismicH.asHTML(slice.primary.text, { serializer })}
		</div>
	</article>
</div>

<style>
	article {
		display: flex;
		align-items: flex-start;
		gap: 1.2rem;
		padding: 2rem 2rem 2rem 1.4rem;
	}

	.emoji {
		font-size: 2rem;
	}

	.reverse {
		flex-direction: row-reverse;
		padding: 2rem 1.4rem 2rem 2rem;
	}
</style>
