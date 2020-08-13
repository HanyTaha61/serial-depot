<template>
	<v-app>
		<div class="default-temp">
			<v-container class="grey lighten-5">
				<v-row>
					<v-col no-gutters cols='12' md='3' class="sidemenu border text-center d-none d-md-block">
						<nuxt-link to="/">
							<v-img :src="myImg" aspect-ratio="2.5" width='150' class="mx-auto"></v-img>
						</nuxt-link>
						<ul>
							<li v-for="(item, i) in list" :key="i">
								<nuxt-link :to="item.to">{{item.name}}</nuxt-link>
							</li>
						</ul>
						<div class="search_set">
							<input type="search" placeholder='search...' class="search">
							<v-btn icon>
								<v-icon>mdi-magnify</v-icon>
							</v-btn>
						</div>
					</v-col>
					<v-col cols='12' md='9' class="">
						<nuxt/>
					<Slide
					 :closeOnNavigation="true"
					class="d-md-none d-block">
						<a id="home" href="#">
							<nuxt-link to="/"><span>Home</span></nuxt-link>
							<nuxt-link to="/download"><span>download</span></nuxt-link>
							<nuxt-link to="/install"><span> install</span></nuxt-link>
							<nuxt-link to="/activate"><span> activate</span></nuxt-link>
							<nuxt-link to="/about"><span> about</span></nuxt-link>
							<nuxt-link to="/contact"><span> contact</span></nuxt-link>
							
						</a>

						<!-- Search functionality -->
						<!-------------------------->

						<!-- <div class="search_set">
							<input type="search" placeholder='search...' class="search">
							<v-btn icon>
								<v-icon>mdi-magnify</v-icon>
							</v-btn>
						</div> -->

					</Slide>
					</v-col>
				</v-row>
			</v-container>
			<Footer/>
		</div>
	</v-app>
</template>

<script>
import Footer from '../components/footer'
import { Slide } from 'vue-burger-menu'

export default {
	components:{Footer, Slide},
	data(){
		return{
			myImg: require('@/assets/logo.png'),
			list:[
				{name: 'Home', to: '/'},
				{name: 'Download ESET NOD32', to: '/download'},
				{name: 'Install ESET NOD32', to: '/install'},
				{name: 'Activate ESET NOD32', to: '/activate'},
				{name: 'About Us', to: '/about'},
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
			.sidemenu{
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
						a.nuxt-link-exact-active{
						background: teal;
						color: #fff;
						}

					}
				}
				.search_set{

					.search{
						padding: 10px;
						margin-top: 50px;
						background-color: #fff;
						width: 100%;
					}
					i{
						color: teal;
						position: relative;
						top: -35px;
						right: -110px;

						@media (max-width: 1263px) {
							right: -80px;
						
						}
					}
				}

			}
		}

		.v-card{

			.v-footer{

				.v-card{

					.v-card__text{

						.theme--dark.v-bottom-navigation{

							background-color: unset !important;
						}
					}
				}
			}
		}
	}

    .bm-burger-bars {
      background-color: #373a47;
    }
    .line-style {
    //   position: absolute;
      height: 20%;
      left: 0;
      right: 0;
    }
    .cross-style {
    //   position: absolute;
      top: 12px;
      right: 2px;
      cursor: pointer;
    }
	// Burger menu
	.bm-burger-button {
    //   position: fixed;
      width: 36px;
      height: 30px;
      left: 36px;
      top: 36px;
      cursor: pointer;
    }
    .bm-menu {
      height: 100%; /* 100% Full-height */
      width: 0; /* 0 width - change this with JavaScript */
      position: fixed; /* Stay in place */
      z-index: 1000; /* Stay on top */
      top: 0;
      left: 0;
      background-color: rgb(63, 63, 65); /* Black*/
      overflow-x: hidden; /* Disable horizontal scroll */
      padding-top: 60px; /* Place content 60px from the top */
      transition: 0.5s; /*0.5 second transition effect to slide in the sidenav*/
	
		.bm-cross-button {
			height: 24px;
			width: 24px;
		
				.bm-cross {
				background: #bdc3c7;
				}
		}
		.bm-item-list {
		color: #b8b7ad;
		margin-left: 10%;
		font-size: 20px;

			#home{
				display: flex;
				flex-direction: column;

				.search_set{

					.search{
						padding: 10px;
						margin-top: 50px;
						background-color: #fff;
						width: 100%;
					}
					i{
						color: teal;
						position: relative;
						top: -35px;
						right: -210px;

						@media (max-width: 1263px) {
							right: -80px;
						
						}
					}
				}

				a{
					text-decoration: none;
					color: #fff;
					margin-bottom: 5px;
					margin-left: -30px;
					padding-left: 10px;
					height: 50px;
					line-height: 50px;
					transition: 0.25s;

				&:hover{
					background-color: teal;
				}
					span{


					}
				}
			}
		}
    }

    .bm-overlay {
      background: rgba(0, 0, 0, 0.3);
    }
    .bm-item-list > * {
      display: flex;
      text-decoration: none;
      padding: 0.7em;
    }
    .bm-item-list > * > span {
    }


</style>
