# 📚 Projeto: Aplicativo de Estudo

  Projeto focado em um aplicativo de estudo. A aplicação permite aos usuários criar, editar e organizar seus cartões de estudo, além de realizar login e visualizar suas tarefas com prazos de vencimento, ajudando-os a manter o foco e a organização.

# 📦 Arquivos Principais

- **App.js:** Componente raiz da aplicação que configura a navegação entre as telas e define os provedores de contexto, garantindo o fluxo adequado de dados e estados ao longo do aplicativo.

- **firebaseConfig.js:** Contém a configuração e inicialização do Firebase. Aqui são definidos os parâmetros essenciais para conectar o app aos serviços de autenticação, banco de dados e outros recursos fornecidos pelo Firebase.

- **AuthContext.js:** Gerencia o estado de autenticação do usuário, utilizando o contexto para compartilhar informações de login/logout e controle de sessão em toda a aplicação.

- **CartoesEstudoContext.js:** Responsável pela gestão dos dados dos cartões de estudo, manipulando operações como criação, edição, remoção e organização dos cartões dentro do sistema de estudos.

- **screens/:** Diretório que contém todos os componentes de tela da aplicação. Cada arquivo dentro dessa pasta representa uma tela específica do app, responsável pela interface e lógica de uma determinada funcionalidade.


# 📖 Bibliotecas Utilizadas no Projeto

## Dependências 

- **react-native:** Framework utilizado para o desenvolvimento de aplicativos móveis nativos, permitindo a criação de interfaces de usuário ricas e altamente performáticas tanto para iOS quanto para Android.

- **expo:** Plataforma open-source que simplifica o desenvolvimento de aplicativos móveis com React Native. Ela fornece um conjunto robusto de ferramentas para testes, compilação e execução de apps em dispositivos reais ou simuladores.

- **firebase:** Conjunto de serviços backend fornecido pelo Google, que inclui autenticação, banco de dados em tempo real, hospedagem, notificações push, entre outros. Usado para gerenciar dados e autenticação de usuários de forma rápida e escalável.

## Principais componentes de Navegação

- @react-navigation/native: Container de navegação
- @react-navigation/native-stack
- @react-navigation/stack

## Componentes de UI

- react-native-vector-icons: Componentes de ícones
- @react-native-picker/picker: Componente de seleção
- react-native-modal-datetime-picker: Seletor de data/hora

## Gerenciamento das variáveis de ambiente

- react-native-dotenv: Gerenciamento de variáveis de ambiente

## Desenvolvimento

- babel-preset-expo: Configuração do Babel para Expo
- react-native-dotenv: Suporte a variáveis de ambiente

# Configuração do Ambiente

O projeto utiliza variáveis de ambiente para configuração do Firebase. Crie um arquivo .env com:

`FIREBASE_API_KEY=
FIREBASE_AUTH_DOMAIN=
FIREBASE_PROJECT_ID=
FIREBASE_STORAGE_BUCKET=
FIREBASE_MESSAGING_SENDER_ID=
FIREBASE_APP_ID=`

# Autenticação

O app utiliza Firebase Authentication para o gerenciamento de usuários. Com essa funcionalidade, os usuários podem:

- Registrar-se utilizando email e senha.
- Entrar na aplicação com suas credenciais existentes.
- Sair da conta a qualquer momento, garantindo o controle sobre a sessão.

# Modelo de Dados

Os cartões de estudo contêm as seguintes informações:

- Título
- Notas
- Status (backlog/in_progress/done)
- Data de vencimento
- ID do usuário (para a identificação dos cartões por usuário)
- Os dados são armazenados no Firebase Firestore com atualizações em tempo real.

# 🚀 Funcionalidades do Sistema

- **Autenticação de usuários:** Permite registro, login e controle de sessão.
- **Gerenciamento de cartões de estudo:** Suporta operações CRUD (criação, leitura, atualização e exclusão) dos cartões.
- **Status dos cartões:** Acompanhe o progresso e a conclusão dos cartões de estudo.
- Acompanhamento de datas de vencimento: Notifique os usuários sobre o prazo de vencimento dos cartões e tarefas.
- **Filtragem de tarefas por status:** Organize e visualize tarefas com base no seu status (pendente, concluído, etc.).
- **Visualização de tarefas próximas:** Exibe tarefas com vencimento nos próximos 15 dias, facilitando o planejamento.

# 🔎 Resumo de estruturação

- **assets/**  
  (Contém recursos estáticos como imagens, ícones e outros arquivos que são utilizados na interface do usuário.)

- **src/**  
  (Contém o código fonte da aplicação.)

  - **config/**  
    (Armazena arquivos de configuração e inicialização de bibliotecas e serviços.)

    - **firebaseConfig.js**  
      (Arquivo responsável pela configuração e inicialização do Firebase para usar serviços como autenticação, banco de dados, etc.)

  - **contexts/**  
    (Contém os provedores de Context do React, que gerenciam o estado global da aplicação.)

    - **AuthContext.js**  
      (Gerencia o estado de autenticação, como o login e logout do usuário.)

    - **CartoesEstudoContext.js**  
      (Gerencia o estado dos cartões de estudo, incluindo operações de adição, remoção e atualização.)

  - **screens/**  
    (Contém os componentes de tela, que representam as diferentes páginas da aplicação.)

    - **EdicaoCartaoScreen.js**  
      (Tela responsável pela edição de um cartão de estudo, permitindo ao usuário modificar seus conteúdos.)

    - **ListaCartaoScreen.js**  
      (Tela principal onde os cartões de estudo são listados e o usuário pode visualizar e interagir com eles.)

    - **LoginScreen.js**  
      (Tela de autenticação onde o usuário pode se logar utilizando credenciais.)

    - **RegistroScreen.js**  
      (Tela de registro onde o usuário pode criar uma nova conta.)

    - **TarefasVencimentoProximoScreen.js**  
      (Tela que exibe as tarefas ou cartões de estudo cujo vencimento está próximo.)

- **App.js**  
  (Componente principal da aplicação, que configura a navegação e os contextos globais.)

- **app.json**  
  (Arquivo de configuração da aplicação, utilizado por ferramentas como Expo para definir propriedades do projeto.)

- **babel.config.js**  
  (Configuração do Babel, ferramenta que transpila o código JavaScript para versões compatíveis com o navegador.)

- **package.json**  
  (Arquivo de configuração do projeto Node.js, contendo as dependências e scripts utilizados na aplicação.)

  # ⚙️ Inicialização do projeto ?

1. Intalação de dependências:

`npm install`

2. Inicialização do servidor de desenvolvimento:

`npm start`
