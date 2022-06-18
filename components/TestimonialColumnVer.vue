<template lang="">
  <div class="container">
     <div class="accordion d-flex justify-content-center align-items-center height" id="accordionExample">
         <div class="row">
             <div class="col-md-6">  
               <div class="p-3">
                 <ul class="testimonial-list">
                   <li>
                      <div class="card p-3" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                        <div class="d-flex flex-row align-items-center">
                          <img src="https://i.imgur.com/G1pXs7D.jpg" width="50" class="rounded-circle">
                          <div class="d-flex flex-column ml-2">
                            <span class="font-weight-normal">Milton Austin</span>
                            <span>Sales Manager, Stack</span>
                          </div>
                        </div>
                      </div>   
                   </li>
                   <li>
                    <div class="card p-3" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                        <div class="d-flex flex-row align-items-center">

                          <img src="https://i.imgur.com/udGH5tO.jpg" width="50" class="rounded-circle">

                          <div class="d-flex flex-column ml-2">

                            <span class="font-weight-normal">John Reeves</span>
                            <span>Head of Sales, Asana</span>
                            
                          </div>
                          
                        </div>
                        
                      </div> 
                   </li>

                   <li>
                    <div class="card p-3" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">

                        <div class="d-flex flex-row align-items-center">

                          <img src="https://i.imgur.com/Uz4FjGZ.jpg" width="50" class="rounded-circle">

                          <div class="d-flex flex-column ml-2">

                            <span class="font-weight-normal">Luke Harper</span>
                            <span>Sales Team Lead,Sketch</span>
                            
                          </div>
                          
                        </div>
                        
                      </div> 
                   </li>

                 </ul>
                 </div>
             </div>

             <div class="col-md-6">
              <div class="p-3 testimonials-margin">
                 <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
                     <div class="card-body">
                         <h4>It was a great experience</h4>
                         <div class="ratings">

                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          
                           
                         </div>

                         <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
                     </div>
                 </div>

                 <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordionExample">
                     <div class="card-body">
                         <h4>Thanks for this great service</h4>
                         <div class="ratings">

                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                           
                         </div>

                         <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
                     </div>
                 </div>

                 <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordionExample">
                     <div class="card-body">
                         <h4>You all are awesome thanks alot</h4>
                         <div class="ratings">

                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                           
                         </div>

                         <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
                     </div>
                 </div>
                 </div>
             </div>
         </div>
     </div>
 </div>
</template>
<script>
export default {
  
}
</script>
<style scoped>
  .gradient-custom { background: radial-gradient(50% 123.47% at 50% 50%, #00FF94 0%, #720059
100%), linear-gradient(121.28deg, #669600 0%, #FF0000 100%), linear-gradient(360deg,
#0029FF 0%, #8FFF00 100%), radial-gradient(100% 164.72% at 100% 100%, #6100FF 0%, #00FF57
100%), radial-gradient(100% 148.07% at 0% 0%, #FFF500 0%, #51D500 100%);
background-blend-mode: screen, color-dodge, overlay, difference, normal; }
.carousel-indicators [data-mdb-target] { border-radius: 50%; width: 10px; height: 10px; }

</style>