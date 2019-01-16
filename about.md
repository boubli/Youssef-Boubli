<style type="text/css">
	*{}
  body {
  text-align: center;
  background: #fff;
}
figure {
  position: relative;
  display: inline-block;
  overflow: hidden;
  width: 136px; height: 148px;
  margin-right: 30px;
  margin-top: 30px;
}

/** Hexagon Mask **/
figure:before {
  z-index: 3;
  position: absolute;
  display: block;
  content: '';
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: url(https://leadergamer.com.tr/wp-content/themes/lgm/images/team-mask-1.png) no-repeat;
  pointer-events: none;
}
figure img {
  display: block;
  width: auto; height: 100%;
}

/** Contact Links **/
figure .contact {
  z-index: 2;
  position: absolute;
  display: block;
  top: 0; left: 0; right: 0; bottom: 0;
}
.contact a {
  background-image: url(https://leadergamer.com.tr/wp-content/themes/lgm/images/level-1-c.png);
}
figure .contact a {
  position: absolute;
  display: block;
  width: 50%; height: 50%;
  background-repeat: no-repeat;
  transition: all .25s ease-in-out;
}
  figure .contact .tw {
    top: 0; left: 0;
    background-color: rgba(0, 172, 238, .7);
    background-position: 30px 32px;
    transform: translate(-100%, -100%);
  }
    figure .contact .tw:hover {
      background-color: rgba(0, 172, 238, 1);
    }
  figure .contact .fb {
    top: 0; right: 0;
    background-color: rgba(59, 89, 152, .7);
    background-position: -42px 32px;
    transform: translate(100%, -100%);
  }
    figure .contact .fb:hover {
      background-color: rgba(59, 89, 152, 1);
    }
  figure .contact .gp {
    bottom: 0; left: 0;
    background-color: rgba(221, 75, 57, .7);
    background-position: 30px -40px;
    transform: translate(-100%, 100%);
  }
    figure .contact .gp:hover {
      background-color: rgba(221, 75, 57, 1);
    }
  figure .contact .ma {
    bottom: 0; right: 0;
    background-color: rgba(153, 153, 153, .7);
    background-position: -42px -40px;
    transform: translate(100%, 100%);
  }
    figure .contact .ma:hover {
      background-color: rgba(153, 153, 153, 1);
    }
    figure:hover .contact a {
      transform: translate(0, 0);
    }
	#name:hover{color: #00a8ff}
	.drrT{ border: 1px solid #DDD; background: #2f3640; color: #dcdde1; padding: 5px}
	#AsA:hover{transform: rotate(1000deg); border: 1px #00a8ff}
	html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

.column {
  float: left;
  width: 33.3%;
  height: 310px ;
  padding: 0 8px;
}

@media screen and (max-width: 650px) {
  .column {
    width: 100%;
    display: block;
  }
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
}

.container {
  padding: 0 16px;
}

.container::after, .row::after {
  content: "";
  clear: both;
  display: table;
}

.title {
  color: grey;
}

.button {
  border: none;
  outline: 0;
  display: inline-block;
  padding: 8px;
  color: white;
  background-color: #00a8ff;
  text-align: center;
  cursor: pointer;
  width: 100%;
}

.button:hover {
  background-color: #0097e6;
}
</style>
<br />

<figure>
  <img src="https://avatars0.githubusercontent.com/u/26576840?s=460&v=4">
  <div class="contact">
    <a href="" class="tw"></a>
    <a href="" class="fb"></a>
    <a href="" class="gp"></a>
    <a href="" class="ma"></a>
  </div>
</figure>


<h2 id="name">YOUSSEF BOUBLI</h2>
<p>programmer & designer</p>
<br />

<div class="drrT">
	<p style="text-align: left;margin: 10px">Youssef Boubli 18 years old i was born in Geuilmim, i live in Agadir, Morocco, im programmer and designer i like Python language. <br /> 
		A mysterious character I like to be isolated and singled out people for this work friends call me a Matrix because I am like his actions and actions but the name I like and which I call myself Raymond is a fictional character but I love this name. <br />
		To learn programming through watching YouTube videos quickly I absorbed the lessons in a week I started to deepen the programming I did not study programming in institutes or colleges, but I think to study in the future in order to obtain a certificate. <br />
	</p>
</div>
</center>

<br />
<br />
<center><h1>MY FRIENDS</h1></center>
<br />
<div class="row">

  <div class="column">
    <div class="card">
      <img src="https://scontent-mrs1-1.xx.fbcdn.net/v/t1.0-9/46503623_887623011628525_1588566531430678528_n.jpg?_nc_cat=111&_nc_eui2=AeHr3zaxS291lxlA7DwWgiIz1iGCjLMfHw6VPAHQ3Iti0d2RppxIQKYKaT45p32DLepA0UsA02JrfpE3yhJVWRbq9EsmhUoTP2aBEP3vsdTuUQ&_nc_ht=scontent-mrs1-1.xx&oh=2b15e7ddb917367570bebdd74a8a5aaa&oe=5CB8BE55" alt="Jane" style="width:100%">
      <div class="container">
        <center><h4>Taib Kouriane</h4></center>
        <center><p class="title">BOULJNON</p></center><br />
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="https://scontent-mrs1-1.xx.fbcdn.net/v/t1.0-9/44379854_1922412427852139_494396228063199232_n.jpg?_nc_cat=110&_nc_ht=scontent-mrs1-1.xx&oh=3d3f468c39544d83a61d7dc663edb8e1&oe=5CB987B3" alt="Jane" style="width:100%">
      <div class="container">
        <center><h4>Yassin Raîs</h4></center>
        <center><p class="title">full stack developer</p></center><br />
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="https://scontent-mrs1-1.xx.fbcdn.net/v/t1.0-9/15073285_1633147050319373_8392762929674651387_n.jpg?_nc_cat=107&_nc_ht=scontent-mrs1-1.xx&oh=d8d5ebbffd30d5d5fc1e52ca6ec45752&oe=5CD619EF" alt="Jane" style="width:100%">
      <div class="container">
        <center><h4>Ayoub Rouida</h4></center>
        <center><p class="title">Expert Specialist</p></center><br />
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="https://scontent-mrs1-1.xx.fbcdn.net/v/t1.0-9/16807637_1289878277757554_7375736009296176677_n.jpg?_nc_cat=104&_nc_ht=scontent-mrs1-1.xx&oh=5758ee5d3be91deaf53750ea2423f82f&oe=5CB553D4" alt="Jane" style="width:100%">
      <div class="container">
        <center><h4>Adam Dihaj</h4></center>
        <center><p class="title">Circle of Science & Technologies</p></center><br />
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="https://scontent-mrs1-1.xx.fbcdn.net/v/t1.0-9/46914953_564720273949667_376399543568171008_n.jpg?_nc_cat=108&_nc_ht=scontent-mrs1-1.xx&oh=bb51002ba92b617b06dde485a0fa6582&oe=5CCE2CAC" alt="Jane" style="width:100%">
      <div class="container">
        <center><h4>Yassine Elkarfaoui</h4></center>
        <center><p class="title">podcaster</p></center><br />
      </div>
    </div>
  </div>

<br />
<br />
<br />
<br />
<br />
<br />
</div>
