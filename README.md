# CLIMA
<div id="app"></div>

<div class="title">Cadastro de Regiões</div>
<div class="title">Cadastro do Clima</div>

<form [formGroup]="estadoForm">

  <div class="row mt-10">
    <div class="col-2">
      <label for="uf">UF</label>
    </div>
    <div class="col">
      <input formControlName="uf" type="select" />
    </div>
  </div>

  <div class="row mt-10">
    <div class="col-2">
      <label for="regiao">Região</label>
    </div>
    <div class="col">
      <input formControlName="regiao" type="text" />
    </div>
  </div>

  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
  </div>
</form>
  <label for="uf">UF</label>
    </div>
    <div class="col">
      <input formControlName="uf" type="select" />
    </div>
  </div>
<div class="row mt-10">
    <div class="col-2">
      <label for="regiao">Clima</label>
    </div>
    <div class="col">
      <input formControlName="regiao" type="text" />
    </div>
  </div>


  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
  </div>
</form>

<table class="table">
  <thead>
    <tr>
      <th>UF</th>
      <th>Região</th>
      <th>Situacão</th>
      <th class="text-center">Ações</th>
    </tr>
  </thead>
  <tbody>
    <tr *ngFor="let estado of estados">
  <th> &#8451</th>
  <th>Região &#8451</th>
  <th>Situacão&#8451</th>
  <th class="text-center">Ações</th>
</tr>
</thead>
<tbody>
    <tr *ngFor="let estado of estados">
      <td>{{estado.uf}}</td>
      <td>{{estado.regiao}}</td>
      <td>{{estado.situacao}}</td>
      <td class="text-center">
        <button>Editar</button>
        <button (click)="excluirEstado(estado)">Excluir</button>
      </td>
    </tr>
  </tbody>
</table>

  <td>{{clima local.&#8451;}}</td>
  
  <td>{{clima.regiao&#8451; }}</td>
  <td>{{clima.situacao &#8451;}}</td>
  <td class="text-center">
    <button>Editar</button>
    <button (click)="excluirEstado(estado)">Excluir</button>
  </td>
  </tr>
</tbody>
</table>
  <tbody>
<th>UF</th>
      <th>minimo e maximo &#8451;</th>
      <th>Situacão minimo e maximo &#8451;</th>
      <th class="text-center">Ações</th>
    </tr>
  </thead>
  <tbody>
    <tr *ngFor="let estado of estados">
      <td>{{minimo e maximo.uf &#8451;}}</td>
      <td>{{minimo e maximo.regiao &#8451;}}</td>
      <td>{{minimo e maximo.situacao &#8451;}}</td>
      <td class="text-center">
        <button>Editar</button>
        <button (click)="excluirminimoemaximo(estado)">Excluir</button>
      </td>
    </tr>
  </tbody>
  <div class="row mt-10">
    <div class="col-2">
      <label for="regiao">localidade-cidade</label>
    </div>
    
    <div class="col">
      <input formControlName="localidade-cidade" type="text" />
    </div>
  </div>


  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
</form>
<div class="previsao">
	<p class="localidade">
		<span class="localidade-cidade"></span>
		/
		<span class="localidade-uf"></span>
    <div class="row mt-10">
    <div class="col-2">
      <label for="regiao">maxima &#8451;</label>
    </div>
    
    <div class="col">
      <input formControlName="maxima" type="text" />
    </div>
  </div>


  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
</form>
<div class="row mt-10">
    <div class="col-2">
      <label for="regiao">minima &#8451;</label>
    </div>
    
    <div class="col">
      <input formControlName="minima" type="text" />
    </div>
  </div>


  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
</form>
    
	</p>
	<div class="card-tempo">
		<p class="card-tempo-hoje"></p>
		<div class="card-tempo-bloco">
			<p class="card-tempo-temperatura"><span class="card-tempo-temperatura-temp"></span></p>
			<p class="card-tempo-condicao"></p>
		</div>
		<div class="card-tempo-caracteristicas">
			<p class="card-tempo-caracteristica card-tempo-caracteristicas-umidade">
				<span class="card-tempo-caracteristica-label">Sensação Termica: </span>
        <span class="localidade-uf"></span>
    <div class="row mt-10">
    <div class="col-2">
      <label for="regiao">maxima umidade&#8451;</label>
    </div>
    <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
      
     
    
  </div>
    <div class="col">
      <input formControlName="maxima umidade" type="text" />
    </div>
  </div>


  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
</form>
<div class="row mt-10">
    <div class="col-2">
      <label for="regiao">minima umidade &#8451;</label>
    </div>
    <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
    
    <div class="col">
      <input formControlName="minima umidade" type="text" />
    </div>
  </div>
  <span class="localidade-uf"></span>
    <div class="row mt-10">
    <div class="col-2">
      <label for="regiao">maxima vento &#8451;</label>
    </div>
    <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
    <div class="col">
      <input formControlName="maxima" type="text" />
    </div>
  </div>


  <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
</form>
<div class="row mt-10">
    <div class="col-2">
      <label for="regiao">minima vento &#8451;</label>
    </div>
    <div class="mt-10">
    <button (click)="salvarEstado()">Inserir</button>
    
    
  </div>
    <div class="col">
      <input formControlName="minima" type="text" />
    </div>
  </div>
      
				
<div class="informacoes-projeto">
	<div class="informacoes-painel">
		<h2 class="informacoes-painel-titulo">Informações do Projeto</h2>
		<p class="informacoes-painel-descricao">O projeto foi desenvolvido por Guilherme Ramos para fins de estudo sobre API.</p>
		<h3 class="informacoes-painel-subtitulo">Descrição</h3>
		<p class="informacoes-painel-paragrafo">O projeto funciona da seguinte forma:</p>
		<ol class="informacoes-painel-lista informacoes-painel-passos-projeto">
			<li class="painel-lista-item informacoes-painel-passos-item">O usuário insere o CEP e clica em "Pesquisar" (ícone da lupa);</li>
			<li class="painel-lista-item informacoes-painel-passos-item">O site faz uma requisição ajax para a API da <a href="https://viacep.com.br/" b="blank">ViaCep</a> (viacep.com.br/ws/CEP-INSERIDO/json). A API retorna alguns dados sobre o CEP (se encontrado). Desses dados, pegaremos somente a Cidade e o Estado (UF);</li>
			<li class="painel-lista-item informacoes-painel-passos-item">Envimos a Cidade/UF para outra função, que fará uma requisição à primeira API da ClimaTempo. Essa API retorna o ID da cidade em questão;</li>
			<li class="painel-lista-item informacoes-painel-passos-item">Com o ID da cidade em mãos, faremos outra requisição. Dessa vez, à API da ClimaTempo que retorna, propriamente os dados sobre o a condição climática da cidade informada;</li>
			<li class="painel-lista-item informacoes-painel-passos-item">Por fim, pasta extrair cada dado do JSON retornado e inseri-lo no espaço destinado a ele.</li>
		</ol>
		<h3 class="informacoes-painel-subtitulo">Mais sobre o desenvolvedor</h3>
		<p class="informacoes-painel-paragrafo">Saiba onde me encontrar:</p>
		<ul class="informacoes-painel-lista informacoes-painel-desenvolvedor">
			href="https://github.com/ramosht" target="blank">GitHub</a></li>
			</div>
	<button class="informacoes-btn">
		<i class="fas fa-info"></i>
	</button>
</div>
