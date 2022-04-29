<template lang="">
  <div>
    <footer class="footer">
      <div class="container text-center">
					<SocialMediaLinks/>
      </div>
      <div class="h4 title text-center">Eason Chen</div>
      <div class="text-center text-muted">
        <p>&copy; 2021 - {{currentYear}} Eason Chen All Rights Reserved.<br>
        The source code of this CV is at <a href="https://github.com/EasonC13/CV_Academic" target="_blank">this GitHub Repo</a>. Feel free to fork and create one for yourself with CC Eason Chen at the footer.</p>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  computed:{
    currentYear: function(){
      let now = new Date();
      return now.getFullYear()
    }
  }
}
</script>
<style lang="">
  
</style>