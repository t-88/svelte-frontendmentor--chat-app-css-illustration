<main id="app">
	<div class="left">
		<img class="background-img" src="../assets/background.svg" alt="phone">
		<img class="app-img" src="../assets/phone.svg" alt="phone">
	</div>
	<div class="right">
		<h1>Simple booking</h1>
		<p>
			Stay in touch with our dog walkers through the chat interface. This makes it easy to 
			discuss arrangements and make bookings. Once the walk has been completed you can rate 
			your walker and book again all through the chat.
		</p>
	</div>
</main>

<script>
</script>

<style type="text/scss">
	@import "./shared";
	#app {
		padding-bottom: 40px;
		display: flex;
		.left {
			position: relative;
			.background-img {
				position: absolute;
				top: 0;
				left: -110px;
			}
			.app-img {
				position: relative;
				z-index: 1;
			}
		}
		.right {
			height: fit-content;
			align-self: center;
			display: flex;
			flex-direction: column;
			h1 {
				color: hsl(271, 36%, 24%);
    			font-weight: 500;
			}
			p {
				color: hsl(270, 7%, 64%);
				line-height: 1.8;
			}
		}
	}
	@include media(">=769px") {
		#app {
			$max-w: 1823;
			$min-w: 769;
			padding-right: applyMath(50,10,$max-w,$min-w);
			gap: applyMath(200,40,$max-w,$min-w);
			.left {
				width: applyMath(810,870,$max-w,$min-w);
				height: applyMath(820,420,$max-w,$min-w);
				.background-img {
					width: applyMath(650,400,$max-w,$min-w);
				}
				.app-img {
					top: applyMath(100,40,$max-w,$min-w);
					left: applyMath(420,210,$max-w,$min-w);
					width: applyMath(440,290,$max-w,$min-w);
				}
			}
			.right {
				width: applyMath(550,500,$max-w,$min-w);;
				gap: applyMath(30,15,$max-w,$min-w);

				h1 {
					font-size: applyMath(45,27,$max-w,$min-w);

				}
				p {
					font-size: applyMath(20,12,$max-w,$min-w);
				}
			}
		}
	}
	@include media("<=768px") {
		#app {
			flex-direction: column;
			.left {
				.app-img {
					top: 40px;
				}
			}
			.right {
				text-align: center;
				align-items: center;
				gap: 20px;
			}
		}	
	}
	@include media("<=768px",">=320px") {
		$max-w: 768;
		$min-w: 320;
		#app {
			gap: applyMath(20,40,$max-w,$min-w);
			.left {
				.background-img {
    				top: applyMath(-310,-80,$max-w,$min-w);
    				left: applyMath(-370,-240,$max-w,$min-w);
    				width: applyMath(700,410,$max-w,$min-w);
				}
				.app-img {
    				width: applyMath(380,290,$max-w,$min-w);
					left: applyMath(160,30,$max-w,$min-w);
				}
			}
			.right {
				width: applyMath(500,320,$max-w,$min-w);
				h1 {
    				font-size: applyMath(40,30,$max-w,$min-w);
				}
				p {
					width: applyMath(450,260,$max-w,$min-w);
					font-size: applyMath(17,14,$max-w,$min-w);
				}
			}
		}
	}
	@include media("<320px") {
		#app {
			gap: 40px;
			.left {
				.background-img {
    				top: -80px;
    				left: -240px;
    				width: 410px;
				}
				.app-img {
    				width: 290px;
					left: 30px;
				}
			}
			.right {
				width: 320px;
				h1 {
    				font-size: 30px;
				}
				p {
					width: 260px;
					font-size: 14px;
				}
			}
		}
	}
</style>