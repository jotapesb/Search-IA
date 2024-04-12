# Introdução

Vamos imaginar que você trabalha para a Fourth Coffee, uma rede nacional de cafés. Você foi solicitado a ajudar a criar uma solução de mineração de conhecimento que facilite a busca de insights sobre as experiências dos clientes. Você decide criar um índice do Azure AI Search usando dados extraídos de avaliações de clientes.

# PASSO 1

Na página inicial do Azure vá na lupa e procure search, logo em seguida irá aparecer 'Pesquisa de IA'

![ai1](https://github.com/jotapesb/Search-IA/assets/147784947/7c930bb1-4233-43c0-9d29-29ff82672736)

Comece criando seu serviço no botão 'Criar serviço Pesquisa'

![ai2](https://github.com/jotapesb/Search-IA/assets/147784947/6a510da5-bce3-4ff1-95e7-84185c1f0d8c)

Preencha os campos e em Camada de preços selecione o Gratuito/Free para não ser cobrado.

![ai3](https://github.com/jotapesb/Search-IA/assets/147784947/53d9b645-27a0-4a66-983b-543f2b8ca024)

Após criar sua implantação estará concluída com sucesso. 

![ai4](https://github.com/jotapesb/Search-IA/assets/147784947/ef09713a-c93e-4756-9bf0-98cde5b66a57)

# Passo 2

Após implantação concluída, vá em 'criar um recurso'.

![ai5](https://github.com/jotapesb/Search-IA/assets/147784947/802d73ce-8ce8-46d2-8434-66423598671d)

Em Categorias vá em 'IA + Machine Learning', procure 'Serviços Cognitivos' e clique em Criar.

![ai 6](https://github.com/jotapesb/Search-IA/assets/147784947/14ea3982-8781-4a95-852e-71e950c0d65c)

Preencha novamente e clique em 'Examinar + Criar'.

![ai7](https://github.com/jotapesb/Search-IA/assets/147784947/d5e1c4e4-d977-4892-a373-9e12e3a79aa5)

Aguarde alguns segundos e a implantação de Serviços Cognitivos foi concluída.

![ai8](https://github.com/jotapesb/Search-IA/assets/147784947/00fbe5a7-ce2b-42a9-9673-cf5d6c5a0e57)

# Passo 3

Agora é necessário criar uma conta de armazenamento.

Procure Contas de armazenamento.

![ai9](https://github.com/jotapesb/Search-IA/assets/147784947/7d708dfe-c73d-465b-8a64-a3dfc48717c3)

Vá em criar conta de armazenamento.

![AI10](https://github.com/jotapesb/Search-IA/assets/147784947/1a3fce6c-c1d2-4052-9f30-8a96da2afa68)

Preencha tudo novamente e deixe selecionado o desempenho em 'Stardard' e a redundancia em 'LRS'. A redundancia são modelos de replica dos dados que vamos inserir dentro da conta de armazenamento. Após preencher, clique em 'Revisar + criar' e novamente em criar.

![ai11](https://github.com/jotapesb/Search-IA/assets/147784947/3fd822af-b413-4bf1-8430-f4e8b9d033fb)

Aguarde alguns segundos e a implantação de Contas de armazenamento foi concluída.

Clique em 'Ir em recursos'.

![ai12](https://github.com/jotapesb/Search-IA/assets/147784947/835a469c-e0bc-4d35-981a-011cd18ac5c0)

Na barra a esquerda procure e selecione Configurações > Configuração.

Em Permitir acesso anônimo ao Blob vai estar marcado em desabilitado como padrão, altere para 'Habilitado' e clique em 'Salvar'.

![ai13](https://github.com/jotapesb/Search-IA/assets/147784947/6155fba6-c733-41f3-8f3c-dc9f9e6cfbbc)

Vá em Armazenamento de dados > Contêiners , + Contêiner para criar e preencha os campos. Em Nível de acesso anônimo terá uma nova opção chamada Contêiner, podendo trazer arquivos do contêiner para armazenamento.

![ai14](https://github.com/jotapesb/Search-IA/assets/147784947/f635c4b9-bceb-4105-8f8a-75473c951a7c)

Após criar o container clique em coffereviews em baixo de $logs, vá em Carregar e faça o upload da pasta reviews descompactada.

![a15](https://github.com/jotapesb/Search-IA/assets/147784947/33f08e39-a0d7-410e-94c0-e59a16be9716)

# Passo 4

Após criar todos esses serviços volte em 'Pesquisa de IA', clique na implantação criada e faça a importação dos dados. 

![ai15](https://github.com/jotapesb/Search-IA/assets/147784947/056b1d74-486d-4008-ba1b-2ed3bbcd73b7)

Ao importar dados selecione em Fonte de Dados o campo Armazenamento de Blob do Azure, preencha os campos necessários e em Cadeia de conexão selecione aquela conta de armazenamento criada anteriormente.

![ai16](https://github.com/jotapesb/Search-IA/assets/147784947/4ded05a3-c20e-4c69-93ea-087f972f43f6)

Agora na aba 'Gerenciador de pesquisa' vamos realizar uma busca search=location:Chicago , mostrando todas as avaliações na cidade de Chicago.

![ai17](https://github.com/jotapesb/Search-IA/assets/147784947/b2f1bfa4-2a20-497a-a60c-689abd59ef75)


