<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/michael_merritt.jpg" width="360" height="360" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<div class="author__intro">
			Michael Merritt
		</div>

		<p class="author__location">
			Software Engineer in
		</p>

		<p class="author__location2">
			San Francisco
		</p>

		<p class="author__links">
			<a href="//github.com/mjmj/">GitHub</a>
			<a href="//linkedin.com/in/mjmj/">Linkedin</a>
			<a href="//github.com/mjmj/talks">Talks</a>
			<a href="//twitter.com/devm0de">Twitter</a>
			<a href="mailto:m@devm0de.com">Email</a>
		</p>

		<!-- <p class="author__bio">
			Hi, I'm Michael.
		</p> -->

	</div>
</template>

<static-query>
query {
  metadata {
	siteName
  }
}
</static-query>


<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 1) 0;


	&__image {
		border-radius: 100%;
		width: 180px;
		height: 180px;
		margin-bottom: 1em;
	}

	&__intro {
		text-align: center;
		opacity: .8;
		font-weight:bold;
		font-size: 1.5em;
	}

	&__location {
		margin: 0 auto;
	}

	// &__location2 {
	// }

	// &__bio {
	// }

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
