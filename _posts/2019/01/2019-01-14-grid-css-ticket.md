---
layout: article
title: Grid css train ticket
date: 2019-01-14 19:45:00+0200
coverPhoto: https://css-tricks.com/wp-content/uploads/2018/05/css-art.jpg
---


{::nomarkdown}
<script type="text/javascript">
	TweenMax.set('svg', {
  visibility: 'visible'
})
TweenLite.defaultEase = Linear.easeNone;

var leftTl = new TimelineMax({paused: false, repeat: -1}).timeScale(1.92);
leftTl.to('.boxesL path:first-child', 1, {
 y: 26
}).to('.boxesL path:first-child', 1, {
 rotation: 180,
 transformOrigin: '127% 0%'/* ,
 ease: Elastic.easeOut.config(0.1, 0.8) */
}, 0)
 .to('.boxesL path:nth-child(2)', 1, {
 y: -40
}, 0)
 .to('.boxesL path:nth-child(3)', 1, {
 y: -40
}, 0)

.to('.boxesM path:first-child', 1, {
 y: 40
}, 0)
 .to('.boxesM path:nth-child(2)', 1, {
 y: 40
}, 0)
.to('.boxesM path:nth-child(3)', 1, {
 rotation: 180,
 transformOrigin: '-27% 100%'/* ,
 ease: Elastic.easeOut.config(0.8, 0.8) */
}, 0)
.to('.boxesM path:nth-child(3)', 1, {
 y: -26
}, 0)

/* var nestedTl = new TimelineMax();
nestedTl.add(leftTl);

var mainTl = new TimelineMax({repeat: -1})
mainTl.to(nestedTl, 10, {
 time: 2, 
 ease: Elastic.easeOut.config(0.7, 0.16)
}) */
TweenMax.set('.whole', {
 rotation: 90,
 transformOrigin: '50% 50%'
})
</script>
<style type="text/css">
	body {
  background-color:#086788;
  overflow: hidden;
  text-align:center;
}

body,
html {
  height: 100%;
  width: 100%;
  margin: 0;
  padding: 0;
}


svg{
  width:100%;
  height:100%;
  visibility:hidden;
}


</style>
<svg viewBox="200 150 400 300" xmlns="http://www.w3.org/2000/svg">
 <defs>
      <path class="pathR" d="M400.5,245V356A19.5,19.5,0,0,0,420,375.5h0A19.5,19.5,0,0,0,439.5,356V245A19.5,19.5,0,0,0,420,225.5h0A19.5,19.5,0,0,0,400.5,245Z" fill="none" stroke="#000" stroke-miterlimit="10"/>
      <path class="pathL" d="M380.5,375.5h0a20.06,20.06,0,0,1-20-20v-110a20.06,20.06,0,0,1,20-20h0a20.06,20.06,0,0,1,20,20v110A20.06,20.06,0,0,1,380.5,375.5Z" fill="none" stroke="#000" stroke-miterlimit="10"/>  
  </defs>
   <g class="whole" fill="#FFF1D0">    
    <g class="boxesL" >
          <path d="M387,253v14H373V253h14m6-6H367v26h26V247Z"/>
          <path d="M387,293v14H373V293h14m6-6H367v26h26V287Z"/>
          <path d="M387,333v14H373V333h14m6-6H367v26h26V327Z"/>
        </g>
        <g class="boxesM" >
          <path d="M427,253v14H413V253h14m6-6H407v26h26V247Z"/>
          <path d="M427,293v14H413V293h14m6-6H407v26h26V287Z"/>
          <path d="M427,333v14H413V333h14m6-6H407v26h26V327Z"/>
        </g> 
 </g>
</svg>
{:/}