## Owl Carosel StagePadding a.k.a next & previous slide half preview

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1663953448043/pFRAGCbFn.jpeg)

OwlCarousel StagePadding

Setup:

$('.owl-carousel').owlCarousel({       
stagePadding: 50,       
loop:**true**,       
margin:10,       
nav:**true**,       
responsive:{           
0:{               
items:1           
},           
600:{               
items:3           
},           
1000:{               
items:5           
}       
}   
})

HTML

<div class="owl-carousel owl-theme">       
  <div class="item"><h4>1</h4></div>       
  <div class="item"><h4>2</h4></div>       
  <div class="item"><h4>3</h4></div>       
  <div class="item"><h4>4</h4></div>       
  <div class="item"><h4>5</h4></div>       
  <div class="item"><h4>6</h4></div>       
  <div class="item"><h4>7</h4></div>       
  <div class="item"><h4>8</h4></div>       
  <div class="item"><h4>9</h4></div>       
  <div class="item"><h4>10</h4></div>       
  <div class="item"><h4>11</h4></div>       
  <div class="item"><h4>12</h4></div>   
</div>

Also check out this [official owlCarousel demo](https://owlcarousel2.github.io/OwlCarousel2/demos/stagepadding.html)