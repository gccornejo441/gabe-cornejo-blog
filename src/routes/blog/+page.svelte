<script>
  import { blogPageDescription, blogPageTitle } from '../../lib/config';
  import PostsList from '../../lib/components/PostsList.svelte';
  /**
   * @type {{ posts: any; }}
   */
   export let data
</script>

<svelte:head>
	<title>{blogPageTitle}</title>

	<meta name="twitter:title" content="Gabe Cornejo's photography" />
	<meta name="twitter:description" content="Photography by Gabe Cornejo" />
	<meta data-key="description" name="description" content={blogPageDescription}>

</svelte:head>

<div class="faqs text">
	<h1 class="header-tag">Blog</h1>
	<div class="faqs-content">
		<section>
			<PostsList posts={data.posts} />
		</section>
	</div>
</div>

<style>
    .header-tag {
        font-weight: 700;
        line-height: 1.2;
        margin-bottom: 1.5rem;
        margin-top: 1.5rem;
        text-align: center;
    }

	.faqs {
		margin: 0 auto; 
    border: 2px solid black;
	}

	h1,
	.faqs-content {
		max-width: var(--sk-line-max-width);
		margin: 0 auto;
	}
</style>