# EXT-PDM202206-2024
Projeto de Extensão - UC PDM202206, 2024-2, IFSC Garopaba

# 1. Introdução
O sistema proposto é um aplicativo para gerenciamento de filas em reuniões presenciais, facilitando a organização e o controle do tempo de fala de cada participante. O aplicativo será integrado com o Firebase e permitirá login apenas por e-mails institucionais previamente definidos.

# 2. Requisitos funcionais
2.1. Autenticação e Acesso
RF1: O usuário deve ser capaz de fazer login com sua conta Google via Firebase.
RF2: Apenas e-mails institucionais da instituição especificada serão aceitos para login.

2.2. Gerenciamento de Salas
RF3: O usuário autenticado deve ser capaz de criar uma sala de reunião.
RF4: Os participantes da sala devem poder ingressar por meio de um código ou link de convite gerado pelo anfitrião.
RF5: O anfitrião deve ter acesso exclusivo à interface de controle da fila e cronômetro.

2.3. Gerenciamento da Fila
RF6: Os participantes devem poder apertar um botão para se inscreverem na fila de perguntas/observações.
RF7: O anfitrião deve ver a fila de inscritos em ordem de inscrição.
RF8: O anfitrião deve ser capaz de marcar o início da fala de um participante, iniciando um cronômetro.
RF09: O anfitrião deve ser capaz de finalizar a fala de um participante, salvando o tempo decorrido no relatório e passando automaticamente para o próximo participante da fila.
RF10: O anfitrião deve ser capaz de cadastrar manualmente que estejam sem acesso ao aplicativo, podendo adicioná-los facilmente na fila sem a necessidade de interromper o controle de fila no aplicativo.

2.4. Relatórios
RF11: O sistema deve gerar automaticamente um relatório da reunião contendo:
Tempo total da reunião
Nome ou identificação do participante.
Tempo total de fala de cada participante, ordenados, em formato de “ranking”.
RF12: O anfitrião deve ser capaz de exportar o relatório em formato PDF.

2.5. Usabilidade
RF13: O sistema deve permitir adicionar uma descrição opcional à reunião no momento da criação da sala.
