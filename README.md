 

##### version 1.0.0-69

Demo of this Github Markdown can be viewed at this GitPages site [https://hpssjellis.github.io/javascript-on-markdown/](https://hpssjellis.github.io/javascript-on-markdown/)


This Github Repository [https://github.com/hpssjellis/javascript-on-markdown](https://github.com/hpssjellis/javascript-on-markdown)


Number of Links: <input type="text" id="myCountLinks" size="7" value="15" >, Seconds per link: <input type="text" id="myCountMax" size="7" value="20" >

<div id="myNumSlides" style=" position:sticky; top:0px; left:20px; "> ...</div>  <br>

  

<div id="myStick"  style=" position:sticky; top:-20px;  ">
 
 <input type=button value="Start-No-Sound" onclick="{
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;    
   myAudio01.pause();
   myAudio01.currentTime = 0;  
   myIndex = 0;  
   clearInterval(myLooper);  
   myCountUp = -1;
   carousel();  
}">
 
<input type=button value="Start-Pre-Recorded" onclick="{   
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;  
   myAudio01.pause();
   myAudio01.currentTime = 0;                                                
   myAudio01 = new Audio('recorded-talk.m4a');
   myAudio01.play(); 
   myIndex = 0;  
   clearInterval(myLooper);  
   carousel();                                                
}">  
 
  <input type=button value="Stop" onclick="{
   myIndex = 0;  
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
}">   

 <input type=button value="-" onclick="{
   clearInterval(myLooper);
   clearInterval(myCounting);
   myIndex -= 1;    
   window.location.href='#'+myIndex;
}">   
  
<input type=button value="+" onclick="{
  clearInterval(myLooper);
  clearInterval(myCounting);
  myIndex += 1;  
  window.location.href='#'+myIndex;
}"> 
  
<input type=button value="Back" onclick="{
   myIndex = myIndex - 2;    
   if (myIndex <= 0){myIndex=0};                                      
   myNext();
}">   
  
<input type=button value="Next" onclick="{
   myNext();
}"> 
  
 <input id="myPause" type=button value="Pause" onclick="{ 
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (this.value == 'Pause'){                                                     
       this.value = 'Play / Pause'; 
       if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
   } else {    
     myIndex -= 1; 
     myCountUp += 1;
     carousel();                                                 
     this.value = 'Pause';  
     if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
         myAudio01.play();
      }                                                    
   }
}"> 
  <input type=button value="TOP" onclick="{ 
   window.location.href='#top'; 
}">  
  
 </div>

#### 1

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

just some markdown

[
https://github.com/hpssjellis](https://github.com/hpssjellis)


#### 2


Try the image with html

<img src="https://user-images.githubusercontent.com/5605614/175780835-2b0d64a4-0ba8-4c90-9f05-fb4e89cd6980.png" width=700 />
<hr>


#### 3

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 4

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 5

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 6

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 7

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 8

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 9

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 10

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 11

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 12

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 13

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 14

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 15

At 20 seconds per page and 15 slides this would be the end of a 5 min presentation
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 16

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 17

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 18

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 19

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 20

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>






<a href="#top">Top of page</a>

### By Jeremy Ellis Twitter @Rocksetta Use at your own Risk!
### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 



<script>
 let myIndex = 1;
 let myLooper = 0;
 let myCounting = 0;
 let myMainNum = 20;   
 let myCountUp = 0;
 let xSlide = 3;
 let myAudio01 = new Audio();
 
;
function carousel() {
  clearInterval(myCounting);
  myCountUp = -1;
  var i;
;
  myIndex++;
  if (myIndex > xSlide) {myIndex = xSlide};    
  window.location.href='#'+myIndex;
  myCountDown();
  myCounting = setInterval(myCountDown, 1000);
  myLooper = setTimeout(carousel, myMainNum*1000); 
}
  
function myCountDown(){
  myCountUp++;
  if (myCountUp >= myMainNum ) {
    myCountUp = myMainNum;                              
  }
  if (myIndex >= xSlide && myMainNum == myCountUp){ 
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ALL DONE`;
     clearInterval(myCounting);             
     clearInterval(myLooper);  
  }
  else {    
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ${myMainNum-myCountUp} seconds remaining`;
  }
}
;
function myNext(){   
  xSlide  = document.getElementById('myCountLinks').value; 
  myMainNum = document.getElementById('myCountMax').value;                        
  clearInterval(myLooper) ; 
  carousel();  
}  
;
</script>  


