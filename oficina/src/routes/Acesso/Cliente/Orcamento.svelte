<script>
	let orcamento_dados = {
		veiculo: {
			foto: 'https://picsum.photos/id/111/450',
			marca: '_marca_',
			modelo: '_modelo_',
			ano: '_ano_',
			cor: '_cor_',
			combustivel: '_combustivel_',
			placa: '_placa_'
		},
		cliente: {
			nome: 'João da Silva'
		},
		eta: '5 dias',
		custo: 'R$ 840,00'
	};
</script>

<nav>
	<a href="/">Início</a>
	<a href="/Acesso/Cliente">Cliente</a>
	<a href="/Acesso/Cliente/Agendamento">Agendamento</a>
	<a href="/Acesso/Cliente/Orcamento" class="active">Orçamento</a>
</nav>

<div class="body container">
	<div class="row my-3">
		<div class="col-md-5">
			<img
				src={orcamento_dados.veiculo.foto}
				class="rounded w-100 img-responsive"
				alt="Imagem do Veículo"
			/>
		</div>
		<div class="col-md-7">
			<div class="row">
				<div class="col-md-12">
					<h2>Orçamento do Veículo</h2>
				</div>
			</div>

			<div class="row">
				<div class="col-md-6 mt-3">
					<ul class="list-group">
						<li class="list-group-item"><bdi class="car-attr">Marca:</bdi> {orcamento_dados.veiculo.marca}</li>
						<li class="list-group-item"><bdi class="car-attr">Modelo:</bdi> {orcamento_dados.veiculo.modelo}</li>
						<li class="list-group-item"><bdi class="car-attr">Ano:</bdi> {orcamento_dados.veiculo.ano}</li>
						<li class="list-group-item"><bdi class="car-attr">Cor:</bdi> {orcamento_dados.veiculo.cor}</li>
						<li class="list-group-item"><bdi class="car-attr">Combustível:</bdi> {orcamento_dados.veiculo.combustivel}</li>
						<li class="list-group-item"><bdi class="car-attr">Placa:</bdi> {orcamento_dados.veiculo.placa}</li>
					</ul>
				</div>
				<div class="col-md-6 mt-3">
					<ul class="list-group">
						<li class="list-group-item"><bdi class="car-attr">Cliente:</bdi> {orcamento_dados.cliente.nome}</li>
						<li class="list-group-item"><bdi class="car-attr">Tempo de Entrega:</bdi> {orcamento_dados.eta}</li>
						<li class="list-group-item"><bdi class="car-attr">Custo do Serviço:</bdi> {orcamento_dados.custo}</li>
					</ul>
				</div>
			</div>
		</div>
	</div>

	<div class="row my-3 justify-content-center">
		<div class="col-md-11 details-body">
			<div class="row">
				<div class="col-md-12 mt-3">
					<h2>Detalhes do Orçamento</h2>
				</div>
			</div>

			<div class="row">
				<div class="col-md-12">
					<table class="table">
						<thead>
							<tr style="text-align: center">
								<th scope="col">#</th>
								<th scope="col">Serviço</th>
								<th scope="col">Mecânico Responsável</th>
								<th scope="col">Custo</th>
								<th scope="col">Confirmação</th>
								<th scope="col">Mais</th>
							</tr>
						</thead>
						<tbody>
							<tr style="text-align: center">
								<th scope="row">1</th>
								<td>Troca de Pneus</td>
								<td>Otto</td>
								<td>R$ 250,00</td>
								<td style="text-align: center"><input type="checkbox" name="confirm" id="" /></td>
								<td><a href="#"><i class="bi bi-plus" /></a></td>
							</tr>
							<tr style="text-align: center">
								<th scope="row">2</th>
								<td>Conserto de Parabrisa</td>
								<td>Otto</td>
								<td>R$ 530,00</td>
								<td style="text-align: center"><input type="checkbox" name="confirm" id="" /></td>
								<td><a href="#"><i class="bi bi-plus" /></a></td>
							</tr>
							<tr style="text-align: center">
								<th scope="row">3</th>
								<td>Troca de Óleo</td>
								<td>Otto</td>
								<td>R$ 60,00</td>
								<td style="text-align: center"><input type="checkbox" name="confirm" id="" /></td>
								<td><a href="#"><i class="bi bi-plus" /></a></td>
							</tr>
						</tbody>
					</table>
				</div>
			</div>
		</div>
	</div>

	<div class="row justify-content-end">
		<div class="form-group col-md-3">
			<a href="#"
				><button class="go" style="font-family: 'Encode Sans', sans-serif;"
					>Confirmar Orçamento</button
				></a
			>
		</div>
	</div>
</div>

<!-- Bootsrap css -->
<link
	rel="stylesheet"
	href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"
/>

<!-- Bootstrap icons -->
<link
	rel="stylesheet"
	href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.5.0/font/bootstrap-icons.css"
/>

<!-- Fonts -->
<link href="http://fonts.cdnfonts.com/css/aircruiser" rel="stylesheet" />
<link href="http://fonts.cdnfonts.com/css/encode-sans-2" rel="stylesheet" />

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

	.body {
		font-family: 'Source Sans Pro', sans-serif;
		color: #141414;
		font-size: 16px;
		margin: 2em auto;
		max-width: 1200px;
		padding: 1em;
		line-height: 1.4;
		text-align: justify;
		border-radius: 15px;
		background: #cecece;
	}

	.car-attr {
		font-family: 'Encode Sans', sans-serif;
		color: #000000;
	}

	.details-body {
		border-radius: 15px;
		color: #ffffff;
		background: #0f0f0f;
	}

	.go {
		color: #ffffff;
		border: none;
		text-align: center;
		cursor: pointer;
		background-color: #04aa6d;
		/* border-radius: 5px; */
		font-size: 23px;
		font-family: 'Source Sans Pro', sans-serif;
		padding: 6px 18px;
	}

	h2 {
		text-align: center;
		font-family: 'Aircruiser', sans-serif;
		font-size: 42px;
	}
</style>
