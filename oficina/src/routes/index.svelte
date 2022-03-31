<script>
</script>

<nav>
	<a href="/" class="active">Início</a>
	<div class="custom_dropdown">
		<button class="dropbtn"
			>Acesso
			<i class="fa fa-caret-down" />
		</button>
		<div class="custom_dropdown-content">
			<a href="/Acesso/Colaborador/">Colaborador</a>
			<a href="/Acesso/Cliente/">Cliente</a>
		</div>
	</div>
</nav>

<link
	rel="stylesheet"
	href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
/>

<style>
	/* Add a black background color to the top navigation */
	nav {
		font-family: 'Source Sans Pro', sans-serif;
		background-color: #333;
		overflow: hidden;
	}

	/* Style the links inside the navigation bar */
	nav a {
		float: left;
		color: #f2f2f2;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
		font-size: 17px;
	}

	/* Change the color of links on hover */
	nav a:hover {
		background-color: #ddd;
		color: black;
	}

	/* Add a color to the active/current link */
	nav a.active {
		background-color: #04aa6d;
		color: white;
	}

	/* The dropdown container */
	.custom_dropdown {
		float: left;
		overflow: hidden;
	}

	/* Dropdown button */
	.custom_dropdown .dropbtn {
		font-size: 16px;
		border: none;
		outline: none;
		color: white;
		padding: 14px 16px;
		background-color: inherit;
		font-family: inherit; /* Important for vertical align on mobile phones */
		margin: 0; /* Important for vertical align on mobile phones */
	}

	/* Dropdown content (hidden by default) */
	.custom_dropdown-content {
		display: none;
		position: absolute;
		background-color: #f9f9f9;
		min-width: 160px;
		box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
		z-index: 1;
	}

	/* Links inside the dropdown */
	.custom_dropdown-content a {
		float: none;
		color: black;
		padding: 12px 16px;
		text-decoration: none;
		display: block;
		text-align: left;
	}

	/* Add a grey background color to dropdown links on hover */
	.custom_dropdown-content a:hover {
		background-color: #ddd;
	}

	/* Show the dropdown menu on hover */
	.custom_dropdown:hover .custom_dropdown-content {
		display: block;
	}
</style>
