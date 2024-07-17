modern chair 
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="UTF8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=devicewidth, initialscale=1.0" />
	<title>Modern Chair Page</title>
	<link rel="shortcut icon" href="./images/favicon.ico" type="image/xicon" />

	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css" />
	<link rel="stylesheet" href="https://unicons.iconscout.com/release/v2.1.9/css/unicons.css" />
	<link rel="stylesheet" href="./styles.css" />
</head>

<body>
	<div class="wrapper">
		<div class="container">
			<div class="infoWrap mobMargin">
				<p class="titleUp">Modern chair</p>
				<h2>Telford Longue</h2>
				<h4>$254 <span>$530</span></h4>
				<div class="sectionFluid">
					<input class="descBtn" type="radio" id="desc1" name="descbtn" checked />
					<label for="desc1">Description</label>
					<input class="descBtn" type="radio" id="desc2" name="descbtn" />
					<label for="desc2">Details</label>
					<div class="sectionFluid descSec accor1">
						<p>
							Lorem ipsum dolor sit, amet consectetur adipisicing elit. Id totam tempora enim officia
							veritatis hic.
						</p>
					</div>
					<div class="sectionFluid descSec accor2">
						<div class="sectionInline">
							<p><span>80</span>cm<br />Length</p>
						</div>
						<div class="sectionInline">
							<p><span>65</span>cm<br />Width</p>
						</div>
						<div class="sectionInline">
							<p><span>90</span>cm<br />Height</p>
						</div>
						<div class="sectionInline">
							<p><span>17.6</span>lbs<br />Weight</p>
						</div>
					</div>
				</div>
				<h5>Choose Color:</h5>
			</div>
			<input class="colorBtn forColor1" type="radio" id="color1" name="colorbtn" checked />
			<label class="firstColor" for="color1"></label>
			<input class="colorBtn forColor2" type="radio" id="color2" name="colorbtn" />
			<label class="color2" for="color2"></label>
			<input class="colorBtn forColor3" type="radio" id="color3" name="colorbtn" />
			<label class="color3" for="color3"></label>
			<input class="colorBtn forColor4" type="radio" id="color4" name="colorbtn" />
			<label class="color4" for="color4"></label>
			<input class="colorBtn forColor5" type="radio" id="color5" name="colorbtn" />
			<label class="color5" for="color5"></label>
			<input class="colorBtn forColor6" type="radio" id="color6" name="colorbtn" />
			<label class="color6" for="color6"></label>
			<div class="infoWrap">
				<a href="#" class="btn"><i class="uil uilshoppingcart icon"></i> Add To Cart</a>
			</div>
			<div class="imgWrap chair1"></div>
			<div class="imgWrap chair2"></div>
			<div class="imgWrap chair3"></div>
			<div class="imgWrap chair4"></div>
			<div class="imgWrap chair5"></div>
			<div class="imgWrap chair6"></div>
			<div class="backColor"></div>
			<div class="backColor chair2"></div>
			<div class="backColor chair3"></div>
			<div class="backColor chair4"></div>
			<div class="backColor chair5"></div>
			<div class="backColor chair6"></div>
		</div>
	</div>

</body>

</html> 





css file --------------------->
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

p{
    font-weight: 400;
    font-size: 16px;
    line-height: 1.7;
    color: #fff;
    margin: 0;
}

#wrapper {
  width: 100%;
  height: 100vh;
  overflow-y: auto;
  overflow-x: hidden;
  font-family: "Poppins", sans-serif;

}

.container {
  position: relative;
  max-width: calc(100% - 40px);
  width: 860px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  padding: 100px 0;
}

.sectionFluid {
  position: relative;
  width: 100%;
  display: block;
}

[type="radio"]:checked,
[type="radio"]:not(:checked) {
  visibility: hidden;
  position: absolute;
}

.colorBtn:checked + label,
.colorBtn:not(:checked) + label {
  /* position: relative; */
  height: 40px;
  transition: all 200ms linear;
  border-radius: 4px;
  width: 40px;
  cursor: pointer;
  margin-right: 10px;
  box-shadow: 0 12px 35px 2px rgba(16, 39, 112, 0.25);
  z-index: 10;
  background-position: center;
  background-size: cover;
  border: 3px solid transparent;
}

label.firstColor {
  margin-left: 500px;
  background-image: url("./Images/color1.jpg");
}
label.color2 {
  background-image: url("./Images/color2.jpg");
}
label.color3 {
  background-image: url("./Images/color3.jpg");
}
label.color4 {
  background-image: url("./Images/color4.jpg");
}
label.color5 {
  background-image: url("./Images/color5.jpg");
}
label.color6 {
  background-image: url("./Images/color6.jpg");
}

.colorBtn:checked + label {
  border-color: #434343;
  transform: scale(1.1);
}

.imgWrap {
  height: 410px;
  width: 500px;
  background-image: url(./Images/chair1.png);
  position: absolute;
  top: 100px;
  left: 0;
  transition: all 550ms linear;
  transition-delay: 100ms;
  /* background-position: center top; */
  background-size: 100%;
  /* background-repeat: no-repeat; */
  display: inline-block;
  z-index: 9;
  opacity: 0;
}

.forColor1:checked ~ .imgWrap.chair1 {
  opacity: 1;
  animation: shake 0.7s cubic-bezier(0.36, 0.07, 0.19, 0.97) both;
}
.imgWrap.chair2 {
  background-image: url("./Images/chair2.png");
}
.forColor2:checked ~ .imgWrap.chair2 {
  opacity: 1;
  animation: shake 0.7s cubic-bezier(0.36, 0.07, 0.19, 0.97) both;
}
.imgWrap.chair3 {
  background-image: url("./Images/chair3.png");
}
.forColor3:checked ~ .imgWrap.chair3 {
  opacity: 1;
  animation: shake 0.7s cubic-bezier(0.36, 0.07, 0.19, 0.97) both;
}
.imgWrap.chair4 {
  background-image: url("./Images/chair4.png");
}
.forColor4:checked ~ .imgWrap.chair4 {
  opacity: 1;
  animation: shake 0.7s cubic-bezier(0.36, 0.07, 0.19, 0.97) both;
}
.imgWrap.chair5 {
  background-image: url("./Images/chair5.png");
}
.forColor5:checked ~ .imgWrap.chair5 {
  opacity: 1;
  animation: shake 0.7s cubic-bezier(0.36, 0.07, 0.19, 0.97) both;
}
.imgWrap.chair6 {
  background-image: url("./Images/chair6.png");
}
.forColor6:checked ~ .imgWrap.chair6 {
  opacity: 1;
  animation: shake 0.7s cubic-bezier(0.36, 0.07, 0.19, 0.97) both;
}
@keyframes shake {
  10%,
  90% {
    transform: translate3d(-1px, 0, 0) rotate(-1deg);
  }
  20%,
  80% {
    transform: translate3d(2px, 0, 0) rotate(2deg);
  }
  30%,
  50%,
  70% {
    transform: translate3d(-3px, 0, 0) rotate(-3deg);
  }
  40%,
  60% {
    transform: translate3d(3px, 0, 0) rotate(3deg);
  }
}
.backColor {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: block;
  z-index: 1;
  background-image: linear-gradient(196deg, #f1a9a9, #e66767);
  transition: all 250ms linear;
  transition-delay: 300ms;
}
.infoWrap {
  position: relative;
  margin-left: 500px;
  z-index: 10;
  display: block;

  text-align: left;
}

.titleUp {
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-size: 13px;
  line-height: 1.2;
  color: #fff;
  margin-top: 0;
  margin-bottom: 10px;
}
h2 {
  font-weight: 800;
  font-size: 34px;
  line-height: 1.2;
  color: #fff;
  margin-top: 0;
  margin-bottom: 10px;
}
h4 {
  font-weight: 500;
  font-size: 26px;
  line-height: 1.2;
  color: #fff;
  margin-top: 0;
  margin-bottom: 30px;
}
h4 span {
  text-decoration: line-through;
  font-size: 20px;
  opacity: 0.6;
  padding-left: 15px;
}
h5 {
  font-weight: 600;
  font-size: 18px;
  line-height: 1.2;
  color: #fff;
  margin-top: 0;
  margin-bottom: 20px;
}


.descBtn:checked + label,
.descBtn:not(:checked) + label {
  position: relative;
  transition: all 200ms linear;
  display: inline-block;
  border: none;
  cursor: pointer;
  color: #ffeba7;

  font-weight: 600;
  font-size: 18px;
  line-height: 1.2;
  color: #fff;
  margin-right: 25px;
  opacity: 0.5;
}
.descBtn:checked + label {
  opacity: 1;
}
.descBtn:not(:checked) + label:hover {
  opacity: 0.8;
}

.descSec {
  padding-top: 20px;
  padding-bottom: 30px;
  transition: all 250ms linear;
  opacity: 0;
  overflow: hidden;
  pointer-events: none;
  transform: translateY(20px);
  color: #fff;
}
.descSec.accor2 {
  position: absolute;
  top: 25px;
  left: 0;
  width: 100%;
  z-index: 2;
}
#desc1:checked ~ .descSec.accor1 {
  opacity: 1;
  pointer-events: auto;
  transform: translateY(0);
}
#desc2:checked ~ .descSec.accor2 {
  opacity: 1;
  pointer-events: auto;
  transform: translateY(0);
}
.sectionInline {
  position: relative;
  display: inline-block;
  margin-right: 20px;
}
.sectionInline p span {
  font-size: 30px;
  line-height: 1.1;
}

.btn {
  position: relative;
  font-weight: 500;
  font-size: 14px;
  line-height: 2;
  height: 48px;
  border-radius: 4px;
  width: 210px;
  letter-spacing: 1px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: none;
  cursor: pointer;
  /* overflow: hidden; */
  /* background-color: transparent; */
  color: #fff;
  box-shadow: 0 6px 15px 0 rgba(16, 39, 112, 0.15);
  transition: all 250ms linear;
  text-decoration: none;
  margin-top: 50px;
}
.icon {
  padding-right: 7px;
  font-size: 20px;
}
.btn:before {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: "";
  z-index: -1;
  background-color: #944852;
  transition: background-color 250ms 300ms ease;
}
.btn:hover {
  box-shadow: 0 12px 35px 0 rgba(16, 39, 112, 0.25);
  background-color: #333;
}
.forColor2:checked ~ .infoWrap .btn:before {
  background-color: #1a1a1a;
}
.forColor3:checked ~ .infoWrap .btn:before {
  background-color: #40566e;
}
.forColor4:checked ~ .infoWrap .btn:before {
  background-color: #5e89b2;
}
.forColor5:checked ~ .infoWrap .btn:before {
  background-color: #8c7f76;
}
.forColor6:checked ~ .infoWrap .btn:before {
  background-color: #5d6160;
}

