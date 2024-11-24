# EXT-PDM202206-2024
Projeto de Extensão - UC PDM202206, 2024-2, IFSC Garopaba

# Me inscrevo ✋! Gerenciamento de Filas para Reuniões

Este repositório contém o projeto de um aplicativo para gerenciamento de filas em reuniões presenciais, facilitando a organização e o controle do tempo de fala de cada participante.

## 📁 Projeto

O código-fonte do projeto está disponível em: [EXT-PDM202206-2024](https://github.com/paes/EXT-PDM202206-2024)

---

## 📜 Introdução

O sistema proposto é um aplicativo para gerenciamento de filas em reuniões presenciais, facilitando a organização e o controle do tempo de fala de cada participante. O aplicativo será integrado com o Firebase e permitirá login apenas por e-mails institucionais previamente definidos.

---

## ⚙️ Requisitos Funcionais

### 2.1 Autenticação e Acesso
- **RF1:** O usuário deve ser capaz de fazer login com sua conta Google via Firebase.
- **RF2:** Apenas e-mails institucionais do IFSC serão aceitos para login.

### 2.2 Gerenciamento de Salas
- **RF3:** O usuário autenticado deve ser capaz de criar uma sala de reunião.
- **RF4:** Os participantes da sala devem poder ingressar por meio de um código ou link de convite gerado pelo anfitrião.
- **RF5:** O anfitrião deve ter acesso exclusivo à interface de controle da fila e cronômetro.
- **RF6:** O anfitrião deve poder passar a liderança da sala para outro participante.
- **RF7:** Anfitrião e participantes devem poder sair da sala.

### 2.3 Gerenciamento da Fila
- **RF8:** Os participantes devem poder apertar um botão para se inscreverem na fila de perguntas/observações.
- **RF9:** Os participantes devem poder apertar um botão para se desinscreverem da fila.
- **RF10:** O anfitrião deve ver a fila de inscritos em ordem de inscrição.
- **RF11:** O anfitrião deve ser capaz de marcar o início da fala de um participante, iniciando um cronômetro.
- **RF12:** O anfitrião deve poder ativar o "modo automático", onde ao passar para o próximo participante, o cronômetro é iniciado automaticamente.
- **RF13:** O anfitrião deve finalizar a fala de um participante, salvando o tempo decorrido no relatório e passando automaticamente para o próximo da fila.
- **RF14:** O anfitrião deve poder pausar/continuar o cronômetro de um participante.
- **RF15:** O anfitrião deve cadastrar manualmente participantes sem acesso ao aplicativo.

### 2.4 Relatórios
- **RF16:** O sistema deve gerar automaticamente um relatório contendo:
  - Tempo total da reunião.
  - Nome da sala.
  - Assunto.
  - Identificação dos participantes.
  - Tempo total de fala e métricas como:
    - **"Matraca"**: Participante com mais minutos cronometrados.
    - **"Teimoso/a"**: Participante com mais vezes na fila.
- **RF17:** O anfitrião deve poder exportar o relatório em PDF.

### 2.5 Usabilidade
- **RF18:** O sistema deve permitir adicionar uma descrição opcional à reunião ao criar uma sala.

---

## 📌 Requisitos Não Funcionais

### Compatibilidade
- O sistema deve ser desenvolvido em **Flutter**, garantindo compatibilidade com:
  - Dispositivos móveis Android (7.0 ou superior) e iOS (12.0 ou superior, se aplicável).
  - Ambientes desktop Linux e Windows.
  - Navegadores modernos (Chrome, Firefox, Edge, Safari).

### Performance
- Tempo de carregamento inicial: **< 3 segundos** em internet de 10 Mbps.
- Operações de autenticação via Firebase: **< 2 segundos**.
- Gerenciamento de filas e relatórios processados em **tempo real**.

### Segurança
- Apenas e-mails institucionais (`@ifsc.edu.br` ou `@aluno.ifsc.edu.br`) poderão acessar o sistema.
- Comunicação entre cliente e Firebase protegida por SSL/TLS.
- Regras de segurança no Firestore baseadas em papéis de usuário (anfitrião ou participante).

### Escalabilidade
- Suporte para até **30 usuários simultâneos por sala**.
- Configuração do Firebase para escalabilidade automática.

### Usabilidade
- Interface adaptativa para diferentes plataformas e resoluções.
- Funcionalidade intuitiva para novos usuários, sem necessidade de treinamento.
- Confirmação para evitar exclusões acidentais.

### Portabilidade
- Funcionalidade em processadores ARM e x86 para Android, Linux e Windows.
- Interface web funcional em navegadores modernos, sem instalação.

### Manutenção
- Código modular e documentado para facilitar novas implementações.
- Padrões de desenvolvimento seguidos conforme boas práticas do Flutter e Dart.

### Acessibilidade
- O sistema deve atender às diretrizes de acessibilidade da **WCAG 2.1**, garantindo:
  - Suporte a leitores de tela.
  - Navegação por teclado.
  - Contraste adequado.

### Integração
- O Firebase Firestore será usado como banco de dados principal.
- Integração futura com gravação de voz para geração de atas.
- Exportação de relatórios em PDF.

