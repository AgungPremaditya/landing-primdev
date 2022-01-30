<script setup lang="ts">
const isHiden = ref(true);
const isRotate = ref(false);

function toggle(): void {
	isHiden.value = !isHiden.value;
	isRotate.value = !isRotate.value;
}
</script>

<template>
	<header>
		<div class="container-brand">
			<NuxtLink to="/">
				<img src="~/assets/images/logo.png" alt="logo" height="70" />
				<h1>Primakara <span>Developer</span></h1>
			</NuxtLink>
		</div>
		<nav class="desktop-nav">
			<NuxtLink to="/">Home</NuxtLink>
			<NuxtLink to="/about">About</NuxtLink>
			<NuxtLink to="/our-team">Our Team</NuxtLink>
		</nav>
		<nav class="mobile-nav" :class="{ hide: isHiden }">
			<NuxtLink to="/">Home</NuxtLink>
			<NuxtLink to="/about">About</NuxtLink>
			<NuxtLink to="/our-team">Our Team</NuxtLink>
		</nav>
		<div @click="toggle" class="toggle-btn" :class="{ rotate: isRotate }">
			<svg
				width="25"
				xmlns="http://www.w3.org/2000/svg"
				class="h-6 w-6"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M4 6h16M4 12h16M4 18h16"
				/>
			</svg>
		</div>
	</header>
</template>

<style scoped lang="scss">
header {
	align-items: center;
	background-color: rgb(255, 255, 255); // ! this is a temporary color
	display: flex;
	justify-content: space-between;
	padding: 8px 100px;
	position: fixed; // ! This Combination to make fixed on top
	top: 0; // ! This Combination to make fixed on top
	width: 100%;

	.container-brand a {
		align-items: center;
		display: flex;
		gap: 2;
		text-decoration: none;

		h1 {
			color: var(--primary-gray);
			font-size: 25px;
			font-weight: 100;

			span {
				font-weight: 700;
			}
		}
	}

	.toggle-btn {
		display: none;
		background-color: transparent;
		border: none;

		svg {
			color: gray;
		}
	}

	.desktop-nav a {
		color: var(--secondary-gray);
		font-size: 14px;
		margin-left: 40px;
		text-decoration: none;
		transition: ease 0.5s all;
	}

	.desktop-nav a:hover {
		color: var(--primary-blue);
	}

	.mobile-nav {
		align-items: center;
		background-color: var(--secondary-blue);
		border-radius: 10px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		padding: 20px;
		position: absolute;
		top: 15vh;
		width: 75%;

		a {
			color: white;
			margin: 10px 0px;
			text-decoration: none;
		}
	}

	nav.hide {
		display: none;
	}
}

@media only screen and (max-width: 768px) {
	header {
		padding: 8px 50px;

		.container-brand a h1 {
			font-size: 18px;
		}

		.desktop-nav a {
			margin-left: 20px;
		}
	}
}

@media only screen and (max-width: 580px) {
	header {
		.desktop-nav {
			display: none;
		}

		.toggle-btn {
			display: block;
			transition: ease 0.5s all;
		}

		.rotate {
			transform: rotate(90deg);
		}
	}
}

@media only screen and (max-width: 380px) {
	header {
		padding: 8px 20px;
		.container-brand a {
			img {
				height: 55px;
			}
			h1 {
				font-size: 14px;
			}
		}
	}
}
</style>
