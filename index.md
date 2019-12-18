## Responsive pricing list using Flexbox

### HTML


```
<!DOCTYPE html>
<html>
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" type="text/css" href="flexbox.css">
</head>
<body>
	<h2 style="text-align:center">Responsive Pricing Tables</h2>
	<p style="text-align:center">Resize the browser window to see the effect.</p>
	<div id="pricing-container">
		<div class="columns">
			<ul class="price">
				<li class="header">TRIAL</li>
				<li class="grey">free!</li>
				<li>10GB Storage</li>
				<li>10 Emails</li>
				<li>10 Domains</li>
				<li>1GB Bandwidth</li>
				<li><a href="#" class="button">Sign Up</a></li>
			</ul>
		</div>
		
		<div class="columns">
			<ul class="price">
				<li class="header">BASIC</li>
				<li class="grey">$ 24.99 / year</li>
				<li>25GB Storage</li>
				<li>25 Emails</li>
				<li>25 Domains</li>
				<li>2GB Bandwidth</li>
				<li><a href="#" class="button">Sign Up</a></li>
			</ul>
		</div>
		
		<div class="columns">
			<ul class="price">
				<li class="header">PRO</li>
				<li class="grey">$ 49.99 / year</li>
				<li>50GB Storage</li>
				<li>50 Emails</li>
				<li>50 Domains</li>
				<li>5GB Bandwidth</li>
				<li><a href="#" class="button">Sign Up</a></li>
			</ul>
		</div>
	</div>
</body>
</html>
```

### CSS
```
@import url('https://fonts.googleapis.com/css?family=Roboto');

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box; /* rwd */
}

body {
	color: #444;
	font-family: Roboto;
	padding: 50px;
	height: 100vh;
}

/* rwd */
@media only screen and (max-width: 600px) {
	#pricing-container {
		display: flex;
		flex: 1;
		flex-direction: column;
	}
}

#pricing-container {
	display: flex;
	flex: 1;
	justify-content: center;
}

.columns {
	margin: 25px;
}

.price {
	list-style-type: none;
	border: 1px solid #eee;
	margin: 0;
	padding: 0;
	-webkit-transition: 0.3s;
	transition: 0.3s;
}

/* Add shadows on hover */
.price:hover {
	box-shadow: 0 8px 12px 0 rgba(0,0,0,0.2)
}

.price .header {
	background-color: #618685;
	color: white;
	font-size: 25px;
  }
  
.price li {
	border-bottom: 0px solid #eee;
	padding: 20px;
	text-align: center;
  }

/* Grey list item */
.price .grey {
	background-color: #eee;
	font-size: 20px;
}

.button {
background-color: #36486b;
border: none;
color: white;
padding: 10px 25px;
text-align: center;
text-decoration: none;
font-size: 18px;
}

.button:hover {
    background:#173b67;
}
```

For more details see [Codepen](https://codepen.io/shindry/pen/vYEKwRQ).
