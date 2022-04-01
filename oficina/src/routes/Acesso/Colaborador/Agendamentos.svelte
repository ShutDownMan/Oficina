<script>
	let agendamentos = [
		{
			id: '000000000000000000',
			cliente: {
				nome: 'João da Silva'
			},
			veiculo: {
				marca: 'Honda',
				modelo: 'Fit',
				ano: '2014'
			},
			horario: '7:30'
		},
		{
			id: '000000000000000001',
			cliente: {
				nome: 'Pedro Souza Ferreira'
			},
			veiculo: {
				marca: 'Chevrolet',
				modelo: 'Cruze',
				ano: '2022'
			},
			horario: '8:00'
		}
	];

	let selected_agendamento = agendamentos[0];

	function getAgendamentoPorID(id) {
		/// para cada agendamento
		for (const agendamento of agendamentos) {
			/// procura se id do agendamento é igual
			if (agendamento.id === id) {
				return agendamento;
			}
		}

		return null;
	}
</script>

<nav>
	<a href="/">Início</a>
	<a href="/Acesso/Colaborador">Colaborador</a>
	<a href="/Acesso/Agendamentos" class="active">Agendamentos</a>
	<a href="/Acesso/Servicos">Serviços</a>
	<a href="/Acesso/Produtos">Produtos</a>
</nav>

<div class="container py-5">
	<div class="row justify-content-md-center">
		<div class="col-md-8">
			<div class="card card-default align-self-center">
				<div class="card-heading">
					<h3 class="display-4 card-title text-center">Agendamentos</h3>
				</div>
				<div class="card-body">
					<ul class="list-group">
						{#each agendamentos as agendamento}
							<a
								href="#"
								class="list-group-item list-group-item-action"
								data-toggle="modal"
								data-target="#agendamentoModal"
								on:click={() => {
									selected_agendamento = getAgendamentoPorID(agendamento.id);
								}}
							>
								<span class="float-right badge badge-success" style="font-size: 12px; width: 45px;">
									Hoje
									<br />
									{agendamento.horario}
								</span>
								<small>
									<strong>{agendamento.cliente.nome}</strong>
									<br />
									{agendamento.veiculo.marca}
									{agendamento.veiculo.modelo} ({agendamento.veiculo.ano})
								</small>
							</a>
						{/each}
					</ul>
				</div>
				<div class="text-center card-footer">
					<small>Lista de Agendamentos dos próximos 7 dias</small>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- Modal -->
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
				<h5 class="modal-title" id="agendamentoModalLabel">{selected_agendamento.cliente.nome}</h5>
				<button type="button" class="close" data-dismiss="modal" aria-label="Close">
					<span aria-hidden="true">&times;</span>
				</button>
			</div>
			<div class="modal-body">
				<span class="float-right badge badge-success" style="font-size: 12px; width: 45px;">
					Hoje
					<br />
					{selected_agendamento.horario}
				</span>
				<small>
					<strong>{selected_agendamento.cliente.nome}</strong>
					<br />
					{selected_agendamento.veiculo.marca}
					{selected_agendamento.veiculo.modelo} ({selected_agendamento.veiculo.ano})
				</small>
			</div>
			<div class="modal-footer">
				<button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
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
</style>
