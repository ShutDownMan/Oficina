<script>
	let marca_selected = '';
	let marca_options = {
		Renault: {
			modelos: ['Captur', 'Duster', 'Zoe']
		},
		Ford: {
			modelos: ['AAAA', 'BBB', 'CCCC']
		},
		Audi: {
			modelos: ['DDD', 'EEE', 'FFF']
		}
	};

	let modelo_selected = '';

	// function updateValue() {
	// 	marca_selected = 'Renault';
	// }
</script>

<nav>
	<a href="/">Início</a>
	<a href="/Acesso/Cliente" class="active">Cliente</a>
	<!-- <a href="/Acesso/Cliente/Agendamento" class="active">Agendamento</a>
	<a href="/Acesso/Cliente/Orcamento">Orçamento</a> -->
</nav>

<div class="body card">
	<form>
		<div class="row mt-3">
			<div class="form-group col-md-12">
				<h2>Informações do Proprietário</h2>
			</div>
		</div>

		<div class="row">
			<div class="form-group col-md-12">
				<label for="nome"><span style="color: red"> * </span>Nome</label>
				<input type="text" class="form-control" id="nome" placeholder="Digite seu nome aqui" />
			</div>
		</div>

		<div class="row">
			<div class="form-group col-md-2">
				<label for="ddd"><span style="color: red"> * </span> DDD</label>
				<input type="text" class="form-control" name="ddd" placeholder="00" />
			</div>
			<div class="form-group col-md-3">
				<label for="tel"><span style="color: red"> * </span> Telefone</label>
				<input type="text" class="form-control" name="tel" placeholder="00000-0000" />
			</div>
		</div>

		<div class="row">
			<div class="form-group col-md-12">
				<label for="email">Email</label>
				<input type="text" class="form-control" name="email" placeholder="seu_email@exemplo.com" />
			</div>
		</div>

		<div class="row mt-3">
			<div class="form-group col-md-12">
				<h2>Informações do Veículo</h2>
			</div>
		</div>

		<div class="row">
			<div class="form-group col-md-6">
				<label for="marca">Marca</label>
				<select class="form-control" name="marca" bind:value={marca_selected}>
					{#each Object.keys(marca_options) as value}<option {value}
							>{value && value[0].toUpperCase() + value.slice(1)}</option
						>{/each}
				</select>
			</div>

			<div class="form-group col-md-6">
				<label for="modelo">Modelo</label>
				<select class="form-control" name="modelo" bind:value={modelo_selected}>
					{#each (marca_options[marca_selected] && marca_options[marca_selected].modelos) || [] as value}<option
							{value}>{value && value[0].toUpperCase() + value.slice(1)}</option
						>{/each}
				</select>
			</div>
		</div>

		<div class="row">
			<div class="form-group col-md-2">
				<label for="ano">Ano</label>
				<input type="number" class="form-control" name="ano" placeholder="2022" />
			</div>
		</div>

		<div class="row mt-3">
			<div class="form-group col-md-12">
				<h2>Informações da Visita</h2>
			</div>
		</div>
		<div class="row">
			<div class="form-group col-md-3">
				<label for="data">Data</label>
				<input type="date" class="form-control" name="data" />
			</div>
			<div class="form-group col-md-3">
				<label for="hora">Horário</label>
				<input type="time" class="form-control" name="hora" />
			</div>
		</div>

		<div class="form-group col-md-12" />

		<div class="row justify-content-end">
			<div class="form-group col-md-3">
				<input
					type="submit"
					value="AGENDAR"
					class="go"
					style="font-family: 'Encode Sans', sans-serif;"
				/>
			</div>
		</div>
	</form>
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
		color: #454545;
		font-size: 16px;
		margin: 2em auto;
		max-width: 800px;
		padding: 1em;
		line-height: 1.4;
		text-align: justify;
		border-radius: 15px;
		background: #cecece;
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

	label {
		font-family: 'Encode Sans', sans-serif;
	}
</style>
