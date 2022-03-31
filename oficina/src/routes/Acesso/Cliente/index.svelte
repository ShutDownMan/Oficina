<script>
	
</script>

<nav>
	<a href="/">Início</a>
	<a href="/Acesso/Cliente" class="active">Cliente</a>
	<a href="/Acesso/Cliente/Agendamento">Agendamento</a>
	<a href="/Acesso/Cliente/Orcamento">Orçamento</a>
</nav>

<div class="row custom_row">
	<div class="column">
		<h2>Fazer um Agendamento</h2>
		<p>Marque agora um agendamento para realização do orçamento.</p>
		<a href="/Acesso/Cliente/Agendamento"><button class="go">Agendar</button></a>
	</div>
	<div class="column">
		<h2>Consultar Orçamentos</h2>
		<p>Gerencie aqui todos os orçamentos realizados.</p>
		<a href="/Acesso/Cliente/Orcamento"><button class="go">Consultar</button></a>
	</div>
</div>

<!-- Bootsrap css -->
<link
	rel="stylesheet"
	href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"
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

	.column {
		float: left;
		width: 40%;
		padding: 1rem;
		/* text-align: justify; */
	}

	/* Clear floats after the columns */
	.custom_row:after {
		content: '';
		display: table;
		clear: both;
	}

	.custom_row {
		font-family: 'Source Sans Pro', sans-serif;
		color: #454545;
		font-size: 16px;
		margin: 2em auto;
		max-width: 800px;
		padding: 1em;
		line-height: 1.4;
		/* text-align: justify; */
	}

	.go {
		color: #ffffff;
		border: none;
		text-align: center;
		cursor: pointer;
		background-color: #04aa6d;
		/* border-radius: 5px; */
		font-size: 17px;
		font-family: 'Source Sans Pro', sans-serif;
		padding: 6px 18px;
	}
</style>
