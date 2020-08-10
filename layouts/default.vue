<template>
	<v-app>
		<div class="default-temp">
			<v-container class="grey lighten-5">
				<v-row>
					<v-col no-gutters cols='5' lg='3' class="border text-center">
						<nuxt-link to="/">
							<v-img :src="myImg" aspect-ratio="2.5" width='150' class="mx-auto"></v-img>
						</nuxt-link>
						<ul>
							<li v-for="(item, i) in list" :key="i">
								<nuxt-link :to="item.to">{{item.name}}</nuxt-link>
							</li>
						</ul>
						<input type="search" placeholder='search...' class="search">
					</v-col>
					<v-col cols='7' lg='9' class="">
						<nuxt/>
					</v-col>
				</v-row>
			</v-container>
			<Footer/>
		</div>
	</v-app>
</template>

<script>
import Footer from '../components/footer'
export default {
	components:{Footer},
	data(){
		return{
			myImg: require('@/assets/logo.png'),
			list:[
				{name: 'Home', to: '/'},
				{name: 'Download ESET NOD32', to: '/download'},
				{name: 'Install ESET NOD32', to: '/install'},
				{name: 'Activate ESET NOD32', to: '/activate'},
				{name: 'About Me', to: '/about'},
				{name: 'Contact Me', to: '/contact'}
			]
		}
	}
}
</script>

<style lang='scss'>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');

	.default-temp{

		.container{
			
			.col-7{
				background-color: #fff;
			}
			.col-5{
				font-family: 'Montserrat', sans-serif;

				.v-image{
					margin-bottom: 30px;
					margin-top: 30px;
				}

				ul{
					list-style: none;

					li{
						
						a{
							text-align: left;
							display: block;
							padding: 15px 25px;
							color: #0096a1;
							transition: 0.25s;
							text-decoration: none;

							&:hover{
								background-color: #fff;
								cursor: pointer;
							}
						}

					}
				}

				.search{
					padding: 10px;
					margin-top: 50px;
					background-color: #fff;

				}

			}
		}
	}
</style>
