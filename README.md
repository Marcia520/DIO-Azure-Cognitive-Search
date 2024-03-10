## [DIO - Azure Cognitive Search](https://www.dio.me/) 

### Utilizando AI Search para indexação e consulta de Dados

Neste Desafio da DIO, será construida uma solução de mineração de conhecimento que facilite a busca de insights sobre as experiências do cliente. Através de um índice de pesquisa de IA do Azure (UI) usando dados extraídos das avaliações de clientes.

Para criar o ÍNDICE foi utilizado o passo a passo que está no Tutorial retirado do site: https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html

### 1. Criar um recurso de pesquisa de IA do Azure

1.1. Inicie sessão no portal do Azure.

1.2. Clique no botão + Criar um recurso, procure a Pesquisa de IA do Azure e crie um recurso de Pesquisa de IA do Azure com as seguintes configurações:

        * Assinatura: Sua assinatura do Azure.
        * Grupo de recursos: Selecione ou crie um grupo de recursos com um nome exclusivo.
        * Nome do serviço: um nome único.
        * Localização : Escolha qualquer região disponível.
        * Nível de preços: Básico
        
![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/83b88f59-d5a4-4da8-84cc-729aa60d3cd5)

1.3. Selecione Revisão + criar e depois de ver a resposta Validação de Sucesso, selecione Criar.

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/12cf08db-a3c6-404b-8fc0-cbfa0e2e7123)

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/568acd93-aa42-437a-b9cb-3cea7fa87357)

1.4. Após a implantação ser concluída, selecione Ir para recurso. Na página de visão geral da Pesquisa de IA do Azure, você pode adicionar índices, dados de importação e índices criados por pesquisa.

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/2cbe0700-e8f0-4dfd-9d6c-ddaec1f56ee2)

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/04aef346-7aff-4805-822c-b403fded4496)

## 2. Criar um recurso de serviços de IA do Azure

2.1. Você precisará fornecer um recurso de serviços de IA do Azure que está no mesmo local que seu recurso de Pesquisa de IA do Azure. Sua solução de pesquisa usará esse recurso para enriquecer os dados no data store com insights gerados por IA.

2.2.  Voltar à página inicial do portal do Azure. Clique no +Criar um recurso botão e busca por Serviços de IA do Azure( , . e Selecione a Criar e Serviços de IA do Azure- Plano. 

2.3.  Você será levado a uma página para criar um recurso de serviços de IA do Azure. 

2.4. Configure-o com as seguintes configurações:

        * Assinatura: Sua assinatura do Azure.
        * Grupo de recursos: o mesmo grupo de recursos do seu recurso de Pesquisa de IA do Azure.
        * Região: O mesmo local do seu recurso de Pesquisa de IA do Azure.
        * Nome : Um nome único.
        * Nível de preços : Standard S0
        
2.5. Ao marcar esta caixa reconheço que li e entendi todos os termos abaixo : Selecionado

2.6. Selecione Revisão + criar. Depois de ver a resposta Validação Passada, selecione Criar.
    
2.7. Aguarde a conclusão da implantação e visualize os detalhes da implantação.

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/1466feeb-74ad-425b-9345-ffe634cd55b4)

## 3. Criar uma conta de armazenamento

3.1.Retorne à página inicial do portal do Azure e, em seguida, selecione o botão + Criar um recurso.
    
3.2.Pesquisar por conta de armazenamento, e criar a Conta de armazenamento recurso com as seguintes configurações:
        
        * Assinatura: Sua assinatura do Azure.
        * Grupo de recursos: o mesmo grupo de recursos da sua Pesquisa de IA do Azure e dos recursos de serviços de IA do Azure.
        * Nome da conta de armazenamento: um nome único.
        * Localização: Escolha qualquer local disponível.
        * Desempenho : Padrão
        * Redundância : Armazenamento redundante local (LRS)

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/a9f43468-b047-4230-89c0-c249f06c3b1a)

3.3. Clique em Revisar e, em seguida, clique em Criar. Aguarde a conclusão da implantação e, em seguida, vá para o recurso implantado.

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/ec08da72-c5b6-438a-bb3e-3eae7ea40574)

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/89080e1c-850f-40d0-bf5e-0c7f0cec0e6a)

3.4. Na conta Armazenamento do Azure que você criou, no painel de menus à esquerda, selecione Configuração (em Configurações).

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/9c3a163a-69ee-43dd-b24c-97e0734ef2b9)

3.5. Altere a configuração para permitir acesso anônimo de Blob a Habilitado e selecione Salvar.

![image](https://github.com/Marcia520/DIO-Azure-Cognitive-Search/assets/56965551/43fdda27-2947-4e8a-8666-02ea30b4bf05)

