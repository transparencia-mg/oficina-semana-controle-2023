# roteiro oficina

## intro (máx. 10min)

- boas vindas, previsão de tempo e etapas da oficina, avisar da gravação

- início gravação

- apresentações pessoais

- contexto geral de ampliação da disponibilização de dados de interesse coletivo e geral
	- relançamento do PdA em 2020
	- Decreto Governo Digital de março de 2022
	- adesão em escala em 2023 após adaptações do PdA

- objetivo é instrumentalizar pessoas responsáveis por bases de dados, em algum nível (produção, manutenção, manipulação, compartilhamento, publicação, etc), para publicar dados no PdA/CKAN
	
	- vamos fazer, portanto, a simulação de um fluxo de publicação no CKAN

- CKAN é 
	- plataforma de dados abertos governamentais mais utilizada no mundo
	
	- ferramenta open source, 
	
	- baseada em postgress, solr, (python)
	
	- desenvolvida pela OKF e mantida pela comunidade (repo aberto no github),
	
	- sujeita a manutenções e evoluções periódicas
		- a última delas era prevista para out/22 e somente foi publicada em jan/23
	
	- vamos usar um ambiente básico da última versão 2.10 publicada em janeiro, acrescida de um plug-in específico desenvolvido recentemente para facilitar a publicação e uso dos dados
		
		- o plugin ainda é matéria de testes, e a oficina também serve para captar dúvidas e necessidades de ajustes

		- a oficina ficará gravada para consulta e prática

		- também temos uma versão em elaboração do Manual de Dados Abertos, para consulta e aberta para observações e sugestões

		- prevemos subir esse ambiente que vamos usar para o PdA em julho (?), juntamente com a agregação de dúvidas e observaçoes no Manual

	- a oficina é instrumental e visa mostrar as funcionalidades da ferramenta/plataforma, mas ela não exaure nossas responsabilidades de promoção de transparência enquanto agentes públicos (preparações e decisões são necessárias e variam conforme órgão e base de dado - i. e. processo de escolha das bases, limpeza, restrição de informações pessoais/sensíveis, atribuição de licenças e uso de formatos abertos - observações ao final da simulação de um fluxo de publicação no CKAN, correlacionando com os principais requisitos legais vigentes)

## fluxo publicação (50min)

- etapas do fluxo: 
	- escolha das bases, 
	- preparação (limpeza, anonimização, formato aberto), 
	- documentação (descrição dos metadados), 
	- validação (se dados estão de acordo com metadados)
	- publicação
	- uso, reuso, feedbacks (mecanismos de transparência passiva)
	- novas versões do conjunto

	- nessa oficina, vamos fazer as etapas de documentação, validação e publicação

- login

- navegação básica (menu superior e lateral)

- adicionar conjunto (30 nomes diferentes por turma - pensar na estratégia - sugestão é distribuir número por mesa para identificar, ex.: conjunto-teste-oficina-1, conjunto-teste-oficina-2)

	- níveis de agregação: recursos > conjunto

	- metadados obrigatórios do conjunto

		- nome legível por máquina

		- título legível em português

		- descrição

		- profile (datapackage ou package), segundo Frictionless Data

		- URL

		- organização (sugestão: criar uma organização específica para a oficina http://projetockan.cge.mg.gov.br/organization/oficina-semana-mineira-de-controle)

		- contatos do publicador/mantenedor

		- licença

		- frequência de atualização
		
		- palavras-chave
		- versão

- adicionar recurso

	- escolher arquivos salvos (link repo github: https://github.com/transparencia-mg/termos-parceria-contratos-gestao/tree/main/data)

	- metadados obrigatórios do recurso

		- nome legível por máquina

		- título legível em português

		- descrição

		- formato arquivo (inferido automaticamente pela ferramenta)

		- encoding arquivo (inferido automaticamente - recomendação forte de uso do utf-8, para leitura e parsemanto/interpretação por ferramentas de dados como pacotes do R e do python)

	- metadados obrigatórios das colunas (explicar o por que disso - dicionários de dados legíveis por pessoas e por máquina/json gerados automaticamente permitirão a interpretação do conteúdo sintático dos dados; na primeira vez, parece ser mais repetitivo e toma um trabalho a mais, mas com potenciais benefícios para auxiliar os usuários, que inclui colegas da adm, ou outros poderes, e tb reduzir demandas repetidas - foco na garantia de um padrão de qualidade, interpretação adequada e aumento da possibilidade de uso do dado)

		- nome legível por máquina

		- título legível em português

		- descrição

		- tipo

		- formato

		- adicionais (chaves primária e estrangeira; )

		- restrições (extensão, para strings; mínimo e máximo, para numerais; lista)

- verificar validação

	- identificar os erros

	- corrigir um erro de tipo de coluna

- inserir relacionamento entre tabelas

	- metadados de chave primária e estrangeira

	- verificar diagrama de entidade-relacionamento

	- simular e corrigir erro de relacionamento

- publicar dados

- visualizar dicionários de dados

	- legível por pessoa

	- legível por máquina: datapackage.json

	- (confirmar alcance de baixar e manipular dados com ferramentas CLI a partir do API show) 

- considerações

	- sobre atendimento aos requisitos legais:

https://andrelamor.github.io/manual-abertura-2023-3/0.1/1.%20Dados%20Abertos%2C%20contexto%20e%20pol%C3%ADticas/002_principios_diretrizes/#aplicacao-dos-pricipios-e-normativos-no-portal-de-dados-abertos-de-mgpda

		- o plugin ainda é matéria de testes, e a oficina também serve para captar dúvidas e necessidades de ajustes

		- a oficina ficará gravada para consulta e prática

		- também temos uma versão em elaboração do Manual de Dados Abertos, para consulta e aberta para observações e sugestões

		- prevemos subir esse ambiente que vamos usar para o PdA em julho (?), juntamente com a agregação de dúvidas e observaçoes no Manual

## tira-dúvidas (30min)