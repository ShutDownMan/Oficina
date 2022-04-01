<script>
	let consultaOrcamento = undefined;

	function consultarOrcamento(e) {
		console.log(e);
		e.preventDefault();
		window.location.href = '/Acesso/Cliente/Orcamento?id=' + consultaOrcamento;
	}

	let consultaAgendamento = undefined;
	function consultarAgendamento(e) {}
</script>

<nav>
	<a href="/">Início</a>
	<a href="/Acesso/Cliente" class="active">Cliente</a>
	<!-- <a href="/Acesso/Cliente/Agendamento">Agendamento</a>
	<a href="/Acesso/Cliente/Orcamento">Orçamento</a> -->
</nav>

<div class="row custom-row">
	<div class="col-md-5 m-3 card">
		<div class="card-body">
			<div class="d-flex flex-column">
				<h5 class="card-title">Agendamentos</h5>
				<h6 class="card-subtitle mb-2 text-muted">_</h6>
				<p class="card-text">
					Marque ou consulte agora seu agendamento para realização do orçamento.
				</p>
				<div class="d-flex flex-row justify-content-around">
					<a
						href="#"
						class="btn btn-secondary"
						role="button"
						data-toggle="modal"
						data-target="#agendamentoModal">Consultar</a
					>
					<a href="/Acesso/Cliente/Agendamento" class="btn btn-success" role="button">Marcar</a>
				</div>
			</div>
		</div>
	</div>
	<div class="col-md-5 m-3 card align-self-baseline">
		<div class="card-body">
			<div class="d-flex flex-column">
				<h5 class="card-title">Consultar Orçamentos</h5>
				<h6 class="card-subtitle mb-2 text-muted">_</h6>
				<p class="card-text">Gerencie aqui todos os orçamentos realizados.<br />‎</p>
				<div class="d-flex flex-row justify-content-around">
					<a
						href="#"
						class="btn btn-success"
						role="button"
						data-toggle="modal"
						data-target="#orcamentoModal">Consultar</a
					>
				</div>
			</div>
		</div>
	</div>
</div>

<div class="container">
	<div class="card" />
</div>

<!-- Agendamento Modal -->
<div
	class="hidden modal fade"
	id="agendamentoModal"
	tabindex="-1"
	role="dialog"
	aria-labelledby="agendamentoModalLabel"
	aria-hidden="true"
>
	<div class="modal-dialog" role="document">
		<div class="modal-content">
			<div class="modal-header">
				<h5 class="modal-title" id="agendamentoModalLabel">Consultar Agendamento</h5>
				<button type="button" class="close" data-dismiss="modal" aria-label="Close">
					<span aria-hidden="true">&times;</span>
				</button>
			</div>
			<div class="modal-body">
				<form on:submit={consultaAgendamento}>
					<div class="row">
						<div class="form-group col-md-12">
							<label for="cpf">CPF</label>
							<input
								type="text"
								class="form-control"
								id="cpf"
								placeholder="000.000.000-00"
								bind:value={consultaAgendamento}
							/>
						</div>
						<div class="form-group col-md-12 align-items-center">
							<center>OU</center>
						</div>
						<div class="form-group col-md-12">
							<label for="rg">RG</label>
							<input
								type="text"
								class="form-control"
								id="rg"
								placeholder="00.000.000-00"
								bind:value={consultaAgendamento}
							/>
						</div>
						<div class="form-group col-md-12 align-items-center">
							<center>OU</center>
						</div>

						<div class="form-group col-md-12">
							<label for="placa">Placa do Veículo</label>
							<input
								type="text"
								class="form-control"
								id="placa"
								placeholder="XXX XXXX"
								bind:value={consultaAgendamento}
							/>
						</div>
					</div>
				</form>
			</div>
			<div class="modal-footer">
				<button type="button" class="btn btn-secondary" data-dismiss="modal">Fechar</button>
				<button
					type="button"
					class="btn btn-success"
					data-dismiss="modal"
					on:click={consultarAgendamento}>Consultar</button
				>
			</div>
		</div>
	</div>
</div>

<!-- Orçamento Modal -->
<div
	class="hidden modal fade"
	id="orcamentoModal"
	tabindex="-1"
	role="dialog"
	aria-labelledby="orcamentoModalLabel"
	aria-hidden="true"
>
	<div class="modal-dialog" role="document">
		<div class="modal-content">
			<div class="modal-header">
				<h5 class="modal-title" id="orcamentoModalLabel">Consultar Orçamento</h5>
				<button type="button" class="close" data-dismiss="modal" aria-label="Close">
					<span aria-hidden="true">&times;</span>
				</button>
			</div>
			<div class="modal-body">
				<form on:submit={consultarOrcamento}>
					<div class="row">
						<div class="form-group col-md-12">
							<label for="nome"><span style="color: red"> * </span>Código do Orçamento</label>
							<input
								type="text"
								class="form-control"
								id="codOrcamento"
								placeholder="000000000000"
								bind:value={consultaOrcamento}
							/>
						</div>
					</div>
				</form>
			</div>
			<div class="modal-footer">
				<button type="button" class="btn btn-secondary" data-dismiss="modal">Fechar</button>
				<button
					type="button"
					class="btn btn-success"
					data-dismiss="modal"
					on:click={consultarOrcamento}>Consultar</button
				>
			</div>
		</div>
	</div>
</div>

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
	.custom-row:after {
		content: '';
		display: table;
		clear: both;
	}

	.custom-row {
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
		border-radius: 5px;
		font-size: 17px;
		font-family: 'Source Sans Pro', sans-serif;
		padding: 6px 18px;
	}
</style>
