<script>
</script>

<nav>
	<a href="/">Início</a>
	<a href="/Acesso/Colaborador" class="active">Colaborador</a>
	<a href="/Acesso/Agendamentos">Agendamentos</a>
	<a href="/Acesso/Servicos">Serviços</a>
	<a href="/Acesso/Produtos">Produtos</a>
</nav>

<div class="row custom_row">
	<div class="col-md-5 m-3 card">
		<div class="card-body">
			<h5 class="card-title">Consultar Agendamos</h5>
			<h6 class="card-subtitle mb-2 text-muted">Gerenciar a lista de Agendamentos dos Clientes</h6>
			<p class="card-text">
				Aqui se encontram a lista de agendamentos realizados pelos clientes.
			</p>
			<a href="/Acesso/Colaborador/Agendamentos" class="align-self-end float-right"><button class="btn go">Consultar</button></a>
		</div>
	</div>
	<div class="col-md-5 m-3 card">
		<div class="card-body">
			<h5 class="card-title">Consultar Serviços</h5>
			<h6 class="card-subtitle mb-2 text-muted">Gerenciar a Lista de Serviços <br>_</h6>
			<p class="card-text">
				Aqui se encontram a lista de serviços disponibilizados pela oficina.
			</p>
			<a href="/Acesso/Colaborador/Agendamentos" class="align-self-end float-right"><button class="btn go">Consultar</button></a>
		</div>
	</div>

	<div class="col-md-5 m-3 card">
		<div class="card-body">
			<h5 class="card-title">Consultar Produtos</h5>
			<h6 class="card-subtitle mb-2 text-muted">Gerenciar a Lista de Produtos <br>_</h6>
			<p class="card-text">
				Aqui se encontram a lista de produtos necessários, utilizados nos serviços.
			</p>
			<a href="/Acesso/Colaborador/Produtos" class="align-self-end float-right"><button class="btn go">Consultar</button></a>
		</div>
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
