 


# javascript-on-markdown
testing if I can do some javascript with markdown on github

##### version 0.2.2-34

Demo of this Github Markdown can be viewed at this GitPages site

[https://hpssjellis.github.io/javascript-on-markdown/](https://hpssjellis.github.io/javascript-on-markdown/)


This Github Repository

[https://github.com/hpssjellis/javascript-on-markdown](https://github.com/hpssjellis/javascript-on-markdown)


Number of Links: <input type="text" id="myCountLinks" size="7" value="4" >

Seconds per link: <input type="text" id="myCountMax" size="7" value="15" >

  <div id="myNumSlides" style=" position:sticky; top:0px; "> ...</div>  <br>

  

<script>
 let myIndex = 1;
 let myLooper = 0;
 let myCounting = 0;
 let myMainNum = 20;   
 let myCountUp = 0;
 let xSlide = 3;
;
function carousel() {
  clearInterval(myCounting);
  myCountUp = -1;
  var i;
;
  for (i = 0; i < xSlide; i++) {
   // xSlide[i].style.display = 'none';  
  }
  myIndex++;
  if (myIndex > xSlide) {myIndex = xSlide};    
 // xSlide[myIndex-1].style.display = 'block';
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
     document.getElementById("myNumSlides").innerHTML = ` Slide ${myIndex} of ${xSlide} slides. ALL DONE`;
     clearInterval(myCounting);             
     clearInterval(myLooper);  
  }
  else {    
     document.getElementById("myNumSlides").innerHTML = ` Slide ${myIndex} of ${xSlide} slides. ${myMainNum-myCountUp} seconds remaining`;
  }
}
;
function myNext(){                         
  clearInterval(myLooper) ; 
  carousel();  
}  
  ;
// document.getElementsByClassName('mySlides')[0].style.display = 'block';
 ; 
</script>  







# Note when looking at the markdown none of the javascript buttons appear, you must go to the gitPages demo link!


 <input type=button value="Start-No-Sound" onclick="{
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;                                               
   myIndex = 0;  
   clearInterval(myLooper);  
   carousel();  
}">

#### 0
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
#### 1
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

just some markdown

[
https://github.com/hpssjellis](https://github.com/hpssjellis)


#### 2
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<input type="button" value="Go to 5" onclick="{
  alert('wow'); 
  window.location.href='#5';                                                   
;
  /*   ignore this line only */ ;  
;           
  alert(); 
}">





more markdown this time of an image

![image](https://user-images.githubusercontent.com/5605614/175780835-2b0d64a4-0ba8-4c90-9f05-fb4e89cd6980.png)

 
 
 
#### 3
 <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br>
Try the image with html

<img src="https://user-images.githubusercontent.com/5605614/175780835-2b0d64a4-0ba8-4c90-9f05-fb4e89cd6980.png" width=700 />


#### 4


.



.



.





.




.





.







.





#### 5


<input type="button" value="go to 2" onclick="{
   window.location.href='#2';
}">

.


.


.



.


.


.



.


.


.


.

####  6

<input type="button" value="go to 4" onclick="{ window.location.href='#4';   }">


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>



