<script>
	// todo Fontart is not done yet
	import Fontart from "./components/fontart.svelte";
	import FloatArrow from "./components/FloatArrow.svelte";
	import WebCom from "./components/WebCom.svelte";
	let y;
	const projectlist = [
		{
			link: "https://egg.cephas.monster",
			src: "/assets/egg.png",
			description: "This is easter egg generator. create by svelte",
		},
		{
			link: "https://Tamagotchi.cephas.monster",
			src: "/assets/tamagotchi.png",
			description: "This is a Tamagotchi clone on the web",
		},
		{
			link: "https://r.cephas.monster",
			src: "/assets/rick_gen.png",
			description:
				"This is a rick roll generator on links and even QR code. 🤜🤛",
		},
		{
			link: "https://gamedle.cephas.monster",
			src: "/assets/gamedle.png",
			description:
				"Gamedle is a game title guessing game. Inspire by wordle",
		},
		{
			link: "https://sky.cephas.monster",
			src: "/assets/skyblock.png",
			description: "Skyblock info. Currently unmaintained. 🚧",
		},
	];
</script>

<svelte:window bind:scrollY={y} />

<main>
	<div class="toptitle"><Fontart /></div>
	<div class="textmoving">
		<p style="transform: translateX({y * -0.1}px)">
			DEV SVELTE CSS JAVASCRIPT GIT HTML PYTHON PROGRAMMING DEV SVELTE CSS
			JAVASCRIPT
		</p>
	</div>
	<div class="textmoving">
		<p style="transform: translateX(calc({y * 0.1}px - 100px))">
			CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS
		</p>
	</div>
	<div class="textmoving">
		<p style="transform: translateX({y * -0.1}px)">
			YOU'RE DEFINITELY NOT IN A CRAZY DUMPSTER FIRE!!! YOU'RE DEFINITELY
		</p>
	</div>
	<div class="center normalfont" />
	<div class="center normalfont">
		Hello <div class="wavehand">👋</div>
	</div>
	<div class="center normalfont">
		I learn programming, Linux and so much more by myself.
	</div>
	<div class="center normalfont">I would like to learn more!</div>
	<div class="center normalfont">
		Got question? <a href="mailto:cephas@cephas.monster">Contact me</a>
	</div>
	<br /><br />
	<div class="center normalfont">Project:</div>
	<div class="lefttwobox">
		{#each projectlist as proj}
			<WebCom
				link={proj.link}
				src={proj.src}
				description={proj.description}
			/>
		{/each}
	</div>
	<div class="legacyproject center normalfont">
		<span>List of my legacy project:</span><br />
		<a class="leglink" href="https://covid.cephas.monster">Covid tracker</a
		><br />
		<a class="leglink" href="https://2022.cephas.monster">2022 Website</a>
	</div>
	<span class="normalfont center">social:</span>
	<div class="normalfont center">
		<a href="https://github.com/seabass6969/"
			><img
				src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"
				alt="github icon"
			/></a
		>
		<a href="https://discord.com/users/665915259848228884">
			<img
				class=""
				src="https://img.shields.io/badge/Discord-100000?style=for-the-badge&logo=discord&logoColor=white"
				alt="Discord logo"
			/>
		</a>
	</div>
</main>
<FloatArrow />

<style lang="scss">
	@import url("https://fonts.googleapis.com/css2?family=Courier+Prime&family=Sacramento&display=swap");
	.toptitle {
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: "Sacramento", cursive;
		font-size: 8rem;
		height: 100vh;
		width: 100vw;
		background-color: black;
		color: white;
		user-select: none;
		@media (max-width: 600px) {
			font-size: 5rem;
		}
	}

	/*
.toptext{
    animation: red_line_across 1000ms alternate;
}
@keyframes red_line_across{
    from {
    filter: blur(10px);
    }
    to {
    filter: blur(0px);
    }
}
*/
	.lefttwobox {
		display: grid;
		justify-content: center;
		grid-template-columns: auto auto auto auto;
		grid-template-rows: auto;
		@media (max-width: 600px) {
			grid-template-columns: auto auto;
			grid-template-rows: auto auto;
		}
	}
	.textmoving p {
		font-family: "Courier Prime", monospace;
		font-size: 3rem;
		transform: translateX(-65px);
		width: 1000vw;
		overflow-x: hidden;
		user-select: none;
		text-shadow: 5px 6px 7px rgba(0, 0, 0, 0.25);
		@media (max-width: 600px) {
			font-size: 2rem;
		}
	}
	.center {
		width: 100vw;
		display: grid;
		justify-content: center;
		padding: 1px;
		grid-template-columns: auto auto;
	}
	.normalfont {
		font-family: "Courier Prime", monospace;
		font-size: 1.5rem;
		user-select: none;
	}
	.wavehand {
		animation: infinite wavehand 5000ms;
	}
	@keyframes wavehand {
		0% {
			transform: rotate(0deg);
		}
		5% {
			transform: rotate(20deg);
		}
		10% {
			transform: rotate(0deg);
		}
		15% {
			transform: rotate(20deg);
		}
		20% {
			transform: rotate(0deg);
		}
		100% {
			transform: rotate(0deg);
		}
	}
	a.leglink {
		color: grey;
	}
</style>
