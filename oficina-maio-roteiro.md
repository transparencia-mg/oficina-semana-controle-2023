# roteiro oficina

![image](https://user-images.githubusercontent.com/52294411/235708922-ea9682a8-5f30-41c9-b611-d1a5a6e5b9a9.png)

## intro (4 slides - máx. 10min)

1

- boas vindas, previsão de tempo (1h30) e etapas da oficina (3), avisar da gravação

- início gravação

- apresentações pessoais

- - - 

![image](https://user-images.githubusercontent.com/52294411/235705786-b506164d-08d3-40ba-aec2-e1cc85d51607.png)

- contexto geral de ampliação da disponibilização de dados de interesse coletivo e geral
	- relançamento do PdA em 2020
	- Decreto Governo Digital de março de 2022
	- adesão em escala em 2023 após adaptações do PdA

- objetivo é instrumentalizar pessoas responsáveis por bases de dados, em algum nível (produção, manutenção, manipulação, compartilhamento, publicação, etc), para publicar dados no PdA/CKAN
	
	- vamos fazer, portanto, a simulação de um fluxo de publicação no CKAN

- - - 
2
![image](https://user-images.githubusercontent.com/52294411/235702265-7da1c054-1d92-485f-b4ea-89279cec4057.png)

https://github.com/ckan/ckan

- CKAN é 
	- plataforma de dados abertos governamentais mais utilizada no mundo
	
	- ferramenta open source, 
	
	- baseada em postgreSQL, solr, (python)
	
	- desenvolvida pela OKF e mantida pela comunidade (repo aberto no GitHub),
	
- - - 
3
![image](https://user-images.githubusercontent.com/52294411/235703452-f20606ed-3db3-45cb-9248-3fc779d5a0c4.png)

https://ckan.org/blog/the-ckan-30-team-is-formed-welcome-to-dragan-and-svetozar

- sujeita a manutenções e evoluções periódicas
		
	- a última delas era prevista para out/22 e somente foi publicada em jan/23

- vamos usar um ambiente básico da última versão 2.10 publicada em janeiro, acrescida de um plug-in específico desenvolvido recentemente para facilitar a publicação e uso dos dados
		
	- o plugin ainda é matéria de testes, e a oficina também serve para captar dúvidas e necessidades de ajustes

	- a oficina ficará gravada para consulta e prática

	- também temos uma versão em elaboração do Manual de Dados Abertos, para consulta e aberta para observações e sugestões

	- PRAZO INTERNO prevemos subir esse ambiente que vamos usar para o PdA em julho (PRAZO A SER PACTUADO COM DTI), juntamente com a agregação de dúvidas e observaçoes no Manual EM https://transparencia-mg.github.io/manual-abertura/
	
- - - 
4
![image](https://user-images.githubusercontent.com/52294411/235704328-972bc2b7-bae7-43f2-aa09-31a6dd5f2378.png)

## fluxo publicação (1 slide + mão-na-massa - 50min)

- etapas do fluxo: 
	- escolha das bases, 
	- preparação (limpeza, anonimização, formato aberto), 
	- documentação (descrição dos metadados), 
	- validação (se dados estão de acordo com metadados)
	- publicação
	- uso, reuso, feedbacks (mecanismos de transparência passiva)
	- novas versões do conjunto

	- nessa oficina, vamos fazer as etapas de documentação, validação e publicação 
	- a oficina é instrumental e visa mostrar as funcionalidades da ferramenta/plataforma, mas ela não exaure nossas responsabilidades de promoção de transparência enquanto agentes públicos (preparações e decisões são necessárias e variam conforme órgão e base de dado - i. e. processo de escolha das bases, limpeza, restrição de informações pessoais/sensíveis, atribuição de licenças e uso de formatos abertos - observações ao final da simulação de um fluxo de publicação no CKAN, correlacionando com os principais requisitos legais vigentes)

- - -
5
- login - http://projetockan.cge.mg.gov.br/organization/oficina-semana-mineira-de-controle

- navegação básica (menu superior e lateral)

- adicionar conjunto (20 a 30 nomes diferentes por turma - sugestão é que cada um coloque primeiro nome e último sobrenome como título): telas e passo-a-passo em https://andrelamor.github.io/manual-abertura-2023-3/0.1/2.%20Ciclo%20de%20publica%C3%A7%C3%A3o%20de%20dados/008_conjunto/#criar-e-documentar-novo-conjunto-de-dados

	- níveis de agregação: recursos > conjunto

	- metadados obrigatórios do conjunto

		- nome legível por máquina(URL), derivado do título

		- título legível em português

		- descrição legível em português

		- organização (pré cadastrada pelo ADMIN)
		
		-  tipo (tabular ou not-tabular), segundo Frictionless Data

		- licença (RESSALVA DA LICENÇA REPETIDA)
		
		- source
		
		- versão 

		- contatos do publicador/autor/mantenedor (FORNECER EXEMPLO USUAL E DEIXAR LINK DA DOCUMENTAÇÃO)
		
		- frequência de atualização (resslava do idioma - vem da especificação, que visa interoperar com as ferramentas open source, como a maioria das ferramentas em SGBD)
		
		- palavras-chave
		
- se sair da página, clicar am ADMIN, no topo da página		

- adicionar recurso: telas e passo-a-passo em https://andrelamor.github.io/manual-abertura-2023-3/0.1/2.%20Ciclo%20de%20publica%C3%A7%C3%A3o%20de%20dados/009_recurso/

	- escolher arquivos salvos na pasta 'Oficina' dentro do Desktop de cada máquina (link repo github: https://github.com/transparencia-mg/termos-parceria-contratos-gestao/tree/main/data)

	- metadados obrigatórios do recurso

		- nome legível por máquina

		- título legível em português

		- descrição legível em português

		- formato arquivo (inferido automaticamente pela ferramenta)

		- tipo (tabular ou não tabular - inferido automaticamente pela ferramenta)

		- encoding arquivo (inferido automaticamente - recomendação forte de uso do utf-8, para leitura e decodificação/interpretação por ferramentas de dados como pacotes do R e do python)



- se sair da página de edição do recurso, clicar em admin > dataset[draft] ou dataset, clicar no recurso e então no botão MANAGE



	- metadados obrigatórios das colunas (explicar o por que disso - dicionários de dados legíveis por pessoas e por máquina/json gerados automaticamente permitirão a interpretação do conteúdo sintático dos dados; na primeira vez, parece ser mais repetitivo e toma um trabalho a mais, mas com potenciais benefícios para auxiliar os usuários, que inclui colegas da adm, ou outros poderes, e tb reduzir demandas repetidas - foco na garantia de um padrão de qualidade, interpretação adequada e aumento da possibilidade de uso do dado)


		- nome legível por máquina (já vem do arquivo)

		- título legível em português

		- descrição legivel em português

		- tipo (inferido automaticamente pela ferramenta)

		- formato (inferido automaticamente pela ferramenta)

		- required
		
		- chaves primária e estrangeira
		
		- unique 

		- extras/restrições (extensão, para strings; mínimo e máximo, para numerais; lista exaustiva)

- verificar validação

	- identificar os erros

	- corrigir um erro de tipo de coluna

- inserir relacionamento entre tabelas

	- metadados de chave primária e estrangeira (muito cuidado com nome da tabela e da coluna)

	- verificar diagrama de entidade-relacionamento

	- simular e corrigir erro de relacionamento

- publicar dados

- visualizar dicionários de dados

	- legível por pessoa

	- legível por máquina: datapackage.json

	- (confirmar alcance de baixar e manipular dados com ferramentas CLI a partir do API show) 

- - - 

## considerações (2 slides)

- em qual patamar estamos na escala de qualidade dos dados 

![image](https://user-images.githubusercontent.com/52294411/235706596-7d9b1db7-26e7-4d8e-afa1-1b89a3e561e6.png)

- - - 

- sobre atendimento aos requisitos legais:

![image](https://user-images.githubusercontent.com/52294411/235706961-51f46cf8-9c15-46b9-9be0-a50cead198c2.png)
https://andrelamor.github.io/manual-abertura-2023-3/0.1/1.%20Dados%20Abertos%2C%20contexto%20e%20pol%C3%ADticas/001_normas_legais/

- o plugin ainda é matéria de testes, e a oficina também serve para captar dúvidas e necessidades de ajustes

- a oficina ficará gravada para consulta e prática

- também temos uma versão em elaboração do Manual de Dados Abertos, para consulta e aberta para observações e sugestões

- prevemos subir esse ambiente que vamos usar para o PdA em julho (?), juntamente com a agregação de dúvidas e observaçoes no Manual

## tira-dúvidas (30min)
