<template>
  <div class="container">
    <nav aria-label="breadcrumb">
      <ol class="breadcrumb">
        <li class="breadcrumb-item active" aria-current="page">Sport</li>
      </ol>
    </nav>
    <div>
      <div class="row">
        <div class="col-8">
          <div class="card mb-3" style="max-width: 700px;">
            <div class="row no-gutters" v-for="berita in beritas" :key="berita.id">
              <div class="col-md-4">
                <img
                  src="https://akcdn.detik.net.id/community/media/visual/2019/12/12/3968ba26-1514-40d2-b7e4-36720f6f1abe_169.jpeg?w=700&q=80"
                  class="d-block w-100"
                  style="height:110px; width:50px;"
                />
              </div>
              <div class="col-md-8">
                <div class="card-body">
                  <h5 class="card-title">{{berita.title}}</h5>
                  <small class="text-muted">{{berita.author}}</small> |
                  <small class="text-muted">{{berita.tglPost}}</small>
                  <p
                    class="card-text"
                  >{{berita.isiBerita}}</p>
                  <p class="card-text">
                    <button class="btn btn-primary">Read More</button>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- get category in rest api -->
        <div class="col-4">
          <ul class="list-group" v-for="category in categorys" :key="category.id">
            <li class="list-group-item">{{ category.title }}</li>
          </ul>
        </div>
      </div>
    </div>
    <div>
      <footer>
        <div class="footer-bottom">
            <div class="container">
                <p class="text-center"> Copyright © 2019. All right reserved Mainankita </p>
            </div>
        </div>
        <!--/.footer-bottom--> 
      </footer>
    </div>
  </div>
</template>

<script>
import axios from 'axios'


export default {
  data(){
		const axios = require('axios')
    return{
      categorys : [],
      beritas: [],
    }
  },
  methods: {
    fetchData(){
			const getBreeds = async () => {
				try {
					return await axios.get('http://127.0.0.1:8001')
				} catch (error) {
					console.log(error)
				}
			}
		}
  },
  mounted(){
    this.getBreeds()
  }
};
</script>

<style scoped>
.container {
  margin-top: 5px;
}
.full {
    width: 100%;    
}
.gap {
	height: 30px;
	width: 100%;
	clear: both;
	display: block;
}
.footer {
	background: #EDEFF1;
	height: auto;
	padding-bottom: 30px;
	position: relative;
	width: 100%;
	border-bottom: 1px solid #CCCCCC;
	border-top: 1px solid #DDDDDD;
}
.footer p {
	margin: 0;
}
.footer img {
	max-width: 100%;
}
.footer h3 {
	border-bottom: 1px solid #BAC1C8;
	color: #54697E;
	font-size: 18px;
	font-weight: 600;
	line-height: 27px;
	padding: 40px 0 10px;
	text-transform: uppercase;
}
.footer ul {
	font-size: 13px;
	list-style-type: none;
	margin-left: 0;
	padding-left: 0;
	margin-top: 15px;
	color: #7F8C8D;
}
.footer ul li a {
	padding: 0 0 5px 0;
	display: block;
}
.footer a {
	color: #78828D
}
.supportLi h4 {
	font-size: 20px;
	font-weight: lighter;
	line-height: normal;
	margin-bottom: 0 !important;
	padding-bottom: 0;
}
.newsletter-box input#appendedInputButton {
	background: #FFFFFF;
	display: inline-block;
	float: left;
	height: 30px;
	clear: both;
	width: 100%;
}
.newsletter-box .btn {
	border: medium none;
	-webkit-border-radius: 3px;
	-moz-border-radius: 3px;
	-o-border-radius: 3px;
	-ms-border-radius: 3px;
	border-radius: 3px;
	display: inline-block;
	height: 40px;
	padding: 0;
	width: 100%;
	color: #fff;
}
.newsletter-box {
	overflow: hidden;
}
.bg-gray {
	background-image: -moz-linear-gradient(center bottom, #BBBBBB 0%, #F0F0F0 100%);
	box-shadow: 0 1px 0 #B4B3B3;
}
.social li {
	background: none repeat scroll 0 0 #B5B5B5;
	border: 2px solid #B5B5B5;
	-webkit-border-radius: 50%;
	-moz-border-radius: 50%;
	-o-border-radius: 50%;
	-ms-border-radius: 50%;
	border-radius: 50%;
	float: left;
	height: 36px;
	line-height: 36px;
	margin: 0 8px 0 0;
	padding: 0;
	text-align: center;
	width: 36px;
	transition: all 0.5s ease 0s;
	-moz-transition: all 0.5s ease 0s;
	-webkit-transition: all 0.5s ease 0s;
	-ms-transition: all 0.5s ease 0s;
	-o-transition: all 0.5s ease 0s;
}
.social li:hover {
	transform: scale(1.15) rotate(360deg);
	-webkit-transform: scale(1.1) rotate(360deg);
	-moz-transform: scale(1.1) rotate(360deg);
	-ms-transform: scale(1.1) rotate(360deg);
	-o-transform: scale(1.1) rotate(360deg);
}
.social li a {
	color: #EDEFF1;
}
.social li:hover {
	border: 2px solid #2c3e50;
	background: #2c3e50;
}
.social li a i {
	font-size: 16px;
	margin: 0 0 0 5px;
	color: #EDEFF1 !important;
}
.footer-bottom {
	background: #E3E3E3;
	border-top: 1px solid #DDDDDD;
	padding-top: 10px;
	padding-bottom: 10px;
}
.footer-bottom p.pull-left {
	padding-top: 6px;
}
.payments {
	font-size: 1.5em;	
}
</style>