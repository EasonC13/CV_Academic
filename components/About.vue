<template lang="">
  <div class="mt-5">
		<div class="row mb-3">
			<div class="col">
				<h1>Eason Chen</h1>
			</div>
		</div>
		<div class="row">
			<div class="col-md-4 order-md-2">
				<img class="img-fluid rounded mb-2" src="/Eason_2022_cut.jpeg"
				 alt="Eason in a formal suit">
			</div>
			<div class="col-md-8 order-md-1">
				<div class="row container">
					<div class="order-md-2 text-center">
						<SocialMediaLinks/>
						<a class="btn btn-primary btn-icon" href="/Eason_CV.pdf" target="_blank" rel="tooltip" title="">Click here to view my CV (PDF)</a>
						<!-- <a class="ml-3 btn btn-primary btn-icon" href="public/Eason_CV.pdf" target="_blank" rel="tooltip" title="">中文版網頁</a> -->
						<hr class="d-md-none">
					</div>
					<div class="order-md-1">
						<p>Hi, I'm a senior at National Taiwan Normal University (NTNU). Eason is the same pronunciation as my Chinese name 怡升 (I-Sheng), which means moving onward and upward with a joyful mind.</p>
						<p>I am a passionate researcher. So far, I participated in several research projects in AI, Human-Computer Interaction and Blockchain, and published 7 papers.</p>
						<p>Moreover, I love to use my programming skills and creativity to solve problems. Currently, I served as Research Assistant at school and Blockchain R&D Engineer at Cohart.co.</p>
						<p>I plan to start my Phd at US or UK at 2023 Fall, now I'm looking for program, lab, professor, and scholarship. If you have potential opportunity, please contact me at <a  target="_blank" href = "mailto: eason.tw.chen@gmail.com">eason.tw.chen@gmail.com</a></p>	
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	data(){
		return {
			data: "HELLO"
		}
	},
	setup(){
		let a = 3
		console.log(a)
	}
}
</script>
<style>

</style>