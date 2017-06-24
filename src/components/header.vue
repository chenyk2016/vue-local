<template>
    <div class="header" :class="{home_header:addClass}">
        <div class="item"><slot></slot></div>
        <div class="item header_search" ><slot name="header_search"></slot></div>
        <div class="item header_mine"><slot name="header_mine"></slot></div>
    </div>
</template>


<script>

export default {
	props: {
		addClass:{
			default:false
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    .header{width: 100%; height: 5.4vh;background-color: #f7f7f7;position: fixed;top: 0;left: 0;padding-top: 4.6vh;z-index: 10;border-bottom: 1px solid #ccc;}
   	.home_header{background-color: #42C055;border: none;}
	.search{height:4.5vh;width: 84vw;border-radius: 5px;background-color: #fff;margin-left: 10px;text-align: left; }
	.search input{padding-left: 30px; height:4vh;width: 200px;border: none;background: url(../assets/images/ic_search.png) no-repeat 5px center;background-size:20px;padding-top: 4px; vertical-align:middle; outline: none;}

	h2{text-align: center;font-size: 16px;padding-top: 5px;}
	.header_search{position: absolute;top:4.6vh;right: 50px;  width: 4.6vh;height: 4.6vh; }
	.header_mine{position: absolute;top:4.6vh;right: 10px;  width: 4.6vh;height: 4.6vh;}
	.header_search img,
	.header_mine img{width: 100%;height: 100%;background-color: transparent;}
</style>
