# Buscas-Cognitivas-Azure-IA

1. Acesse a página inicial da azure no link: https://portal.azure.com, pesquise por "Azure AI Search" no buscador e clique em "Pesquisa de IA".
![Página Inicial da Azure](images/img-1.jpg)

<br>

2. Na nova aba clique em "Criar" no menu de opções, para criar um novo recurso de pesquisa.
![Menu lateral da Azure](images/img-2.jpg)

<br>

3. Em "Grupo de recursos" escolha um já criado ou crie um novo no botão abaixo "Criar novo". Dê um nome ao serviço, utilize a já indicada pela Azure e clique em "Alterar o Tipo de Preço".
![Detalhes do projeto](images/img-3.jpg)

<br>

4. Clique na opção "Basico" e depois clique em "Selecionar".
![Detalhes da instância](images/img-4.jpg)

<br>

5. Após ser redirecionado, deve aparecer um card de exito. Volte a tela de serviços..
![Botão Examinar + Criar](images/img-5.jpg)

<br>

6. Clique no serviço de pesquisa. 
![Botão Examinar + Criar](images/img-6.jpg)

<br>

7.Clique em "Criar um recurso".
![Tela Examinar + Criar](images/img-7.jpg)

<br>

8. No menu de opções na lateral esquerda, clicar em "IA + Machine Learning".
![Tela de implantação concluida](images/img-8.jpg)

<br>

9. Clique em "Azure AI services" para cria o serviço.
![Página Inicial da Azure](images/img-9.jpg)

<br>

10. Em "Grupo de recursos" escolha um já criado ou crie um novo, dê um nome ao serviço, escolha Standard SO para o "Pricing tier", marque o checkbox em View full pricing details e clique no botão abaixo "Examinar e Criar".
![Menu lateral da Azure](images/img-10.jpg)

<br>

11. Confira tudo e clique em "Criar".
![Serviços Cognitivos da Azure](images/img-11.jpg)

<br>

12. Após ser redirecionado, deve aparecer um card de exito. Clique no botão "Ir para o recurso".
![Detalhes do projeto](images/img-12.jpg)

<br>

13. Pesquise por "Storage Account" no buscador e clique em "Contas de armazenamento".  
![Detalhes da instância](images/img-13.jpg)

<br>

14. Clique em "Criar" na aba de opções para criar uma nova conta de armazenamento.
![Botão Examinar + Criar](images/img-14.jpg)

<br>

15. Em "Grupo de recursos" escolha um já criado ou crie um novo no botão abaixo "Criar novo". Em detalhes da instância, coloque um nome. Utilize a região indicada pela Azure ou "East US". Em "Desempenho" selecione a opção "Standard", em "Redundância" esolha a opção "LRS". Por fim clique em "Examinar e Criar".
![Tela Examinar + Criar](images/img-15.jpg)

<br>

16. Examine tudo e clique em "Criar".
![Tela de implantação concluida](images/img-16.jpg)

17. Após ser redirecionado, deve aparecer um card de exito. Clique no botão "Ir para o recurso".
![Página Inicial da Azure](images/img-17.jpg)

<br>

18. Na barra de navegação lateral, encontre a opção "Configuração" e clique nela.
![Página Inicial da Azure](images/img-18.jpg)

<br>


19. Habilite a opção "Permitir acesso anônimo ao Blob" e clique em Salvar na barra de opções.
![Menu lateral da Azure](images/img-19.jpg)

<br>

20. Na barra de navegação lateral, encontre a opção "Contêineres" e clique nela.
![Menu lateral da Azure](images/img-20.jpg)

<br>

21. CLique em "Adicionar Contêiner" para criar um novo Contêiner. No campo "Nome", escolha um nome de sua preferência. No campo "Nível de acesso anônino" escolha a opção "Contêiner". E por fim clique em "Criar".
![Menu lateral da Azure](images/img-21.jpg)

<br>

22. Acesse a documentação oficial da Microsoft em: https://aka.ms/ai900-ai-search. Vá até a seção "Carregar documentos para o armazenamento do Azure" Encontre a seção 4 do tópico e aperte no link "avaliações de café compactadas", ele deve iniciar um download no seu navegador, abra a pasta após concluir o download no seu explorador de arquivos. Descompacte a pasta, volte a Azure e selecione o contêiner criado. Clique em "Carregar" e faça upload da pasta baixada.
![Menu lateral da Azure](images/img-22.jpg)

<br>

23. Volte ao mecânismo de busca criado anteriormente.
![Menu lateral da Azure](images/img-23.jpg)

<br>

24. Clique em "Importar dados".
![Menu lateral da Azure](images/img-24.jpg)

<br>

25. Ao abrir o import de dados selecione a opção "Armazenamento de Blob do Azure".
![Menu lateral da Azure](images/img-25.jpg)

<br>

26. Escolha o container que foi criado.
![Menu lateral da Azure](images/img-26.jpg)

<br>

27. Na seção "Conectar a seus dados", mantenha a "Fonte de Dados", dê um nome de sua escolha a fonte de dados, mantenha a opção "Contéudo e metadados" em "Dados para extrair", em "Modo de análise" mantenha o padrão e por fim clique em "Escolher uma conexão existente" para o campo "Cadeia de conexão". Ele deve exibir a cadeia criada anteriormente, selecione e clique em "Selecionar". Ele deve se autocompletar após selecionar o armazenamento criado. Continuando, em "Autenticação de identidade gerenciada" escolha "Nenhum", em "Nome do contêiner" escolha o contêiner criado, não é necessário preencher "Pasta de blobs" nem "Descrição" (Opcional). Por fim clique em "Próximo: Adicionar habilidades cognitivas (opcional)".
![Menu lateral da Azure](images/img-27.jpg)

<br>

28. Expanda a seção "Adicionar enriquecimentos". Defina um nome de sua escolha, habilite a checkbox para habilitar o OCR. Certique-se que a opção marcada para "Campos de dados de origem" esteja em "merged_content". E em "Nível de granulidade do enriquecimento" escolha a opção "Páginas (parte de caracteres de 5000)". Deixe "Habilitar o enriquecimento incremental" em branco.
![Menu lateral da Azure](images/img-28.jpg)

<br>

29. Continuando, em "Habilidades Cognitivas de Texto", assinale as opções: "Extrair nomes de localização", "Extrair frases-chave" e "Detectar sentimento". Em "Habilidades Cognitivas de Imagem", assinale todas as opções. Continue para a seção "Salvar os enriquecimentos em um repositório de conhecimento", escolha "Escolher uma conexão existente".
![Menu lateral da Azure](images/img-29.jpg)

<br>

30. Escolha uma conta de armazenamento existente.
![Menu lateral da Azure](images/img-30.jpg)

<br>

31. Selecione o contâiner criado.
![Menu lateral da Azure](images/img-31.jpg)

<br>

32. Assinale todas as opções (o nome do contêiner será preenchido automáticamente), por fim clique em "Próximo: Personalizar índice de destino".
![Menu lateral da Azure](images/img-32.jpg)

<br>

33. Na seção "Personalizar índice de destino", defina o nome de sua escolha, em "Chave" defina como "metadata_storage_path", deixe a opção "Nome do sugestor" em branco e deixe a opção "Modo de busca" como está. Abaixo, selecione todos os campos já selecionados como "Filtrável" e clique em "Próximo: Criar um indexador".
![Menu lateral da Azure](images/img-33.jpg)
![Menu lateral da Azure](images/img-34.jpg)

<br>

35. Na seção "Criar um indexador", defina um nome de sua preferência e em agenda escolha "Uma vez" e clique em "Enviar".
![Menu lateral da Azure](images/img-35.jpg)

<br>

36. Voltando no recurso do serviço de pesquisa, em "Explorador de pesquisa".
![Menu lateral da Azure](images/img-36.jpg)

<br>

37. Faça uma busca clique em "Pesquisar" e veja que na seção "Resultado", temos a resposta da pesquisa em um formato JSON.
![Menu lateral da Azure](images/img-37.jpg)

<br>
