Dashboard de Controle de Produção por CRT

🚀 Sobre o Projeto

Este é um dashboard avançado para o planejamento e controle de produção industrial, centrado em um indicador de produtividade chamado CRT (Carga de Trabalho Relativa). A ferramenta permite um gerenciamento granular do progresso de cada máquina, distribuindo o esforço de produção por setores e fornecendo uma visão clara do trabalho realizado versus o planejado.

Desenvolvido como uma aplicação de página única (standalone), o sistema utiliza o Firebase (Firestore) para armazenamento e sincronização de dados em tempo real, garantindo que toda a equipe tenha acesso às informações mais recentes.

🧠 O Conceito do CRT (Carga de Trabalho Relativa)
O CRT é o coração deste sistema. Ele não mede apenas o tempo, mas sim o esforço ou complexidade total para produzir um determinado modelo de máquina. O conceito funciona da seguinte forma:

CRT Total do Modelo: Cada modelo de máquina (ex: "SK 4+4", "CHILLER Carenado") possui um valor de CRT total, que representa 100% do esforço de produção.

Pesos por Setor: Esse CRT total é distribuído em percentuais (%) entre os diversos setores da fábrica (ex: Chassi, Compressor, Montagem Elétrica, Teste). A soma de todos os pesos de setor deve ser 100%.

Acompanhamento de Progresso: No dashboard, os operadores inserem o percentual de conclusão (0-100%) para cada setor de uma máquina específica.

Cálculo do CRT Realizado: O sistema calcula automaticamente o CRT Realizado da máquina, somando a contribuição de cada setor:

CRT Realizado = CRT_Total * (Σ (Peso_Setor_% * Progresso_Setor_%))

Isso permite uma medição muito mais precisa da produtividade, refletindo o valor do trabalho agregado em cada etapa do processo.

✨ Principais Funcionalidades
📊 Dashboard de Progresso: Tabela principal com status visual (atrasado, em atenção, em dia) que mostra o progresso percentual e o CRT Realizado de cada máquina em produção.

📝 Cadastro de Máquinas: Formulário completo para registrar novas ordens de produção, associando-as a um modelo, lote, obra e datas.

⚖️ Gestão de Pesos (CRT): Interface dedicada para cadastrar e editar os pesos percentuais de cada setor para um determinado modelo de máquina.

📈 Relatórios de Produtividade: Tabelas que sumarizam o total de CRT produzido por dia e por semana, permitindo análises de desempenho.

❗ Monitoramento de Atrasos: Uma seção específica calcula e exibe o CRT Faltante de todas as máquinas que já passaram da data de entrega planejada.

✅ Histórico de Concluídas: Tabela para consultar todas as máquinas que atingiram 100% de progresso, com o cálculo automático de dias úteis de produção.

🔒 Persistência de Dados: Integração total com o Firebase Firestore para salvar e carregar todos os dados de forma segura e em tempo real.

🛠️ Tecnologias Utilizadas
Frontend:

HTML5

Tailwind CSS para estilização moderna e responsiva.

JavaScript (ES6 Modules) para toda a lógica de cálculo, interatividade e comunicação com o backend.

Banco de Dados:

Google Firebase (Firestore) como backend NoSQL em tempo real.

Visualização de Dados:

Chart.js (dependência incluída, embora os gráficos tenham sido substituídos por tabelas de sumário na versão atual).

⚙️ Como Utilizar
Para rodar este projeto, você só precisa de um navegador web e uma conta no Firebase.

Clone o Repositório:

git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git

Configure o Firebase:

Crie um novo projeto no console do Firebase.

No seu projeto, crie um banco de dados Firestore.

Vá para as configurações do projeto (Project Settings) e, na aba General, adicione um novo aplicativo Web.

O Firebase fornecerá um objeto de configuração firebaseConfig. Copie este objeto.

Atualize o Código:

Abra o arquivo index.html.

Localize a seção de script no final do arquivo e cole o seu objeto firebaseConfig no local indicado.

Pronto!

Abra o arquivo index.html no seu navegador para começar a usar o dashboard. Os dados que você inserir serão salvos no seu projeto Firebase.

🖼️ Visualização
Aqui você pode adicionar um screenshot ou um GIF do seu dashboard em ação!

🤝 Contribuições
Contribuições são bem-vindas! Se você tem alguma ideia para melhorar este projeto, sinta-se à vontade para criar um fork e abrir um pull request.

Faça um Fork do projeto.

Crie uma nova Branch (git checkout -b feature/sua-feature).

Faça o Commit de suas mudanças (git commit -m 'Adiciona sua-feature').

Faça o Push para a Branch (git push origin feature/sua-feature).

Abra um Pull Request.

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
