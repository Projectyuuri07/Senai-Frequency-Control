# Senai-Frequency-Control

## <span style="color: #8000FF;">Índice</span>

 **<span style="color: #9A2EFE;">1. Introdução</span>**
   - [Sobre a documentação](#sobre-a-documentação)
   - [Problemática](#problemática)
   - [Objetivos](#objetivos)
   - [Justificativa](#justificativa)
   - [Observação](#observação)

 **<span style="color: #9A2EFE;">2. Metodologia</span>**
   - [Ferramentas utilizadas](#ferramentas-utilizadas)
   - [Linguagens de programação](#linguagens-de-programação)
   - [Linguagens de marcação](#linguagens-de-marcação)
   - [Linguagens de estilo](#linguagens-de-estilo)
   - [Frameworks](#frameworks)
   - [Bibliotecas](#bibliotecas)
   - [Banco de dados](#banco-de-dados)
   - [Outras ferramentas](#outras-ferramentas)
   - [Todas as Dependências](#todas-as-dependências)
   - [Metodologia para Desenvolvimento](#metodologia-para-desenvolvimento)

 **<span style="color: #9A2EFE;">3. Levantamento de Requisitos</span>**
   - [Requisitos Funcionais](#requisitos-funcionais)
   - [Requisitos Não Funcionais](#requisitos-não-funcionais)

 **<span style="color: #9A2EFE;">4. Arquitetura do Sistema</span>**
   - [Diagrama Model-Template-View (MTV)](#diagrama-mtv)
   - [Diagrama de Classes](#diagrama-de-classes)
   - [Diagrama de Entidade e Relacionamento](#diagrama-er)
   - [Diagrama de Casos de Uso](#diagrama-casos-de-uso)
   - [Fluxograma](#fluxograma)

 **<span style="color: #9A2EFE;">5. Visual das Interfaces</span>**
   - [Interface Inicial](#interface-homepage)
   - [Interface de Login](#interface-login)
   - [Interface de Cursos](#interface-cursos)
   - [Interface de Alunos](#interface-alunos)
   - [Interface de Cadastro](#interface-cadastro)
   - [Interface de Relatórios](#interface-relatórios)
   - [Interface de Notificações](#interface-notificações)
   - [Interface de Adição de Alunos, Cursos e Frequências](#interface-adição-de-alunos-cursos-e-frequência)

 **<span style="color: #9A2EFE;">6. Implementação</span>**
   - [v0.0 - Configuração do Ambiente de Desenvolvimento](#v00-configuração-do-ambiente-de-desenvolvimento)
   - [v0.1 - Configuração do Ambiente do Selenium](#v01-configuração-do-ambiente-do-selenium)
   - [v0.2 - Criação do Aplicativo](#v02-criação-do-aplicativo)
   - [v0.3 - Criação das URLs, Views e Models](#v03-criação-das-urls-e-views)
   - [v0.4 - Desenvolvimento das Páginas](#v04-desenvolvimento-das-páginas)
   - [Importações e Arquivos CSS globais](#importações-e-arquivos-css-globais)
   - [Temas claro e escuro](#temas-claro-e-escuro)
   - [Elaboração das classes](#elaboração-das-classes)

 **<span style="color: #9A2EFE;">7. Lógicas</span>**
   - [Lógica das Views](#lógica-das-views)
   - [Lógica do JavaScript](#lógica-do-javascript)
   - [Lógica de Automação com o Selenium, PyAutoGUI e Agendador de Tarefas](#lógica-de-automação)

 **<span style="color: #9A2EFE;">8. Testes de Software</span>**
   - [Testes Automatizados](#testes-automatizados)
   - [Testes Unitários](#testes-unitários)
   - [Testes Manuais](#testes-manuais)

---

## **<span style="color: #8000FF;">Introdução</span>**

### **<span style="color: #9A2EFE;">Sobre a documentação</span>**
A presente documentação, realizada pelo grupo 03 do Curso Técnico de Desenvolvimento de Sistemas, da instituição SENAI Conde Alexandre Siciliano, da cidade de Jundiaí, visa explicar o funcionamento do Trabalho de Conclusão de Curso “Gestão de Frequência Automatizada: Simplificando a Rotina Administrativa”.

### **<span style="color: #9A2EFE;">Problemática</span>**
No cenário atual da instituição SENAI Conde Alexandre Siciliano, por exemplo, a gestão dos atrasos dos alunos é, sem dúvida, exaustivo e representa um desperdício de tempo e esforço devido a processos manuais em sua averiguação. Atualmente, quando um aluno chega após o horário tolerável, recebe um papel de autorização, que deve ser assinado por um membro da gestão escolar para permitir sua entrada em sala. Ao adentrar, o aluno entrega o papel ao professor, que o armazena por um tempo.
A automação de processos consiste em realizar ou apoiar um fluxo de tarefas cotidianas por meio de recursos tecnológicos. Com isso, a implantação de ferramentas automatizadas nas escolas vai além de uma simples modernização, pois representa uma evolução da própria dinâmica educacional e administrativa, permitindo que coordenadores, professores e alunos estejam integrados em um sistema mais ágil e eficiente.

### **<span style="color: #9A2EFE;">Objetivos</span>**
**Gerais**

Diante desses pontos, a automação desse processo não é apenas benéfica, mas necessária. O objetivo é automatizar o gerenciamento dos atrasos, reduzindo o tempo gasto pelos profissionais da instituição.
Ademais, o sistema notificará de forma automática os coordenadores após um estudante acumular três atrasos superiores a 10 minutos do horário da ingressão do aluno à instituição, permitindo que intervenham e tomem as medidas necessárias.

**Específicos**

O primeiro passo para o desenvolvimento do projeto será focar em pesquisas relacionadas à geração de relatórios, integração do sistema com a catraca e levantamento de requisitos de modo a desenvolver a etapa de design com segurança e clareza. Além do gerenciamento de atrasos, a plataforma incluirá uma lógica para controlar a frequência dos alunos, utilizando dados de entrada e saída para fornecer uma visão mais precisa do desempenho acadêmico.
Para a etapa de implementação, a meta principal será automatizar a coleta de dados da catraca e armazená-los no banco de dados, exibindo-os de forma visual e simplificada para o usuário. Todavia, devido às restrições impostas pela Lei Geral de Proteção de Dados (LGPD - Lei 13.709/2018), que tem como objetivo proteger os direitos fundamentais de liberdade, privacidade e o livre desenvolvimento da personalidade da pessoa natural, não foi possível o acesso a essas informações, impactando assim, com o cronograma dos desenvolvedores, tendo sido necessário o replanejamento do roteiro de desenvolvimento. Outro alvo que se planeja desenvolver com maestria é colocar em prática as regras de negócio relacionadas à frequência, sendo a segunda maior prioridade do projeto.

### **<span style="color: #9A2EFE;">Justificativa</span>**
A falta de controle da frequência dos alunos tem sido uma preocupação recorrente relatada por professores e coordenadores do SENAI. Muitos alunos chegam atrasados e entram no meio das aulas com um papel assinado pela coordenação, interrompendo as aulas e causando transtornos, sendo um problema que não só prejudica a concentração dos estudantes e o andamento das aulas, como também gera uma carga administrativa excessiva para os coordenadores, que precisam lidar com uma grande quantidade de papéis e autorizações manuais.

Ademais, as consequências da situação atual provocam vários problemas como a falta de disciplina por parte dos estudantes, uma vez que a ausência de um sistema de controle eficaz incentiva tal comportamento por não enfrentarem consequências significativas por seus atrasos frequentes; a dificuldade de monitorar e registrar manualmente todas as ocorrências de atraso; e uma comunicação ineficiente com os responsáveis e alunos, que não são informados sobre a frequência de atrasos, o que dificulta o acompanhamento e ações necessárias para corrigir o comportamento dos estudantes.

Portanto, este sistema permitirá que a gestão monitore os atrasos e a frequência dos alunos de maneira mais eficaz, diminuindo esforços manuais e simplificando a rotina administrativa, melhorando assim, a comunicação interna e a solução de problemas de forma eficiente.

### **<span style="color: #9A2EFE;">Observação</span>**
Durante as primeiras etapas de desenvolvimento, os desenvolvedores passaram por uma mudança de planos inesperada e fora de seu controle, vinda de um esclarecimento sobre o projeto com a Analista de Qualidade de Vida. O referido processo evidenciou as limitações organizacionais concernentes ao acesso e processamento dos dados referentes à movimentação dos estudantes no sistema de controle de acesso. Consequentemente, houve a reposição estratégica para dar continuidade ao projeto, fundamentando a abordagem nas modificações identificadas.

---

## **<span style="color: #8000FF;">Metodologia</span>**

### **<span style="color: #9A2EFE;">Ferramentas utilizadas</span>**
- **<span style="color: #4682B4;">Trello:</span>**  é um aplicativo de gerenciamento de projeto baseado na web. Foi utilizado para gerenciar o Product Backlog, distribuição de tasks para cada desenvolvedor do grupo e melhor organização para a produção e desenvolvimento;
- **<span style="color: #4682B4;">Visual Studio Code:</span>**  é um editor de código-fonte desenvolvido pela Microsoft para Windows, Linux e macOS. Ele inclui suporte para depuração, controle de versionamento Git incorporado, realce de sintaxe, complementação inteligente de código, snippets e refatoração de código. No desenvolvimento do sistema, foi utilizada a versão 1.91.1-x64;
- **<span style="color: #4682B4;">Git:</span>**  é um sistema de controle de versões distribuído, usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo. No desenvolvimento do sistema, foi utilizada a versão 2.46.0-x64;
- **<span style="color: #4682B4;">Figma:</span>** é um editor gráfico de vetor e prototipagem de projetos de design baseado principalmente no navegador web, com ferramentas offline adicionais para aplicações desktop para GNU/Linux, macOS e Windows. Foi utilizado para realizar a prototipagem do sistema em relação às páginas.

### **<span style="color: #9A2EFE;">Linguagens de Programação</span>**

### **<span style="color: #9A2EFE;">Python v3.12.3</span>**
Python é uma linguagem de programação versátil, conhecida por sua simplicidade e facilidade de aprendizado. Ela é interpretada, ou seja, o código é executado linha por linha, o que facilita o teste e a depuração do código. Além disso, a linguagem é orientada a objetos, o que permite uma melhor organização do código em estruturas reutilizáveis. 

A linguagem é uma das mais populares do mundo e é amplamente utilizada em diversos setores, como desenvolvimento web, ciência de dados e inteligência artificial, garantindo uma variedade de recursos — incluindo documentação, tutoriais e fóruns — que ajudam a aprimorar as habilidades dos desenvolvedores.

No sistema, o Python foi essencial para construir o back-end (parte interna de uma aplicação) utilizando Django, um framework que facilitou o desenvolvimento das lógicas de cadastro e login de coordenadores, uploads de dados de frequência, alunos e dos cursos fornecidos pela instituição, bem como a implementação das funcionalidades de notificação automática. Além disso, a linguagem foi utilizada para a coleta de informações do banco de dados para a listagem dos alunos e cursos, por exemplo, nas páginas de visualização.

### **<span style="color: #9A2EFE;">JavaScript ECMAScript 5.1</span>**
JavaScript é uma linguagem de programação interpretada e orientada a objetos, frequentemente usada para desenvolver interatividade em páginas web. Ela permite que os desenvolvedores controlem o comportamento dos elementos na tela, respondendo a eventos como cliques e movimentos do mouse. Suas capacidades dinâmicas incluem a criação de objetos em tempo real e a manipulação de funções.
A linguagem é executada no cliente web ou pode ser usada para projetar e/ou programar o comportamento de páginas web quando ocorrem eventos.
Neste projeto, o JavaScript foi utilizado para implementar mudanças de estado, como a alternância entre temas claro e escuro, amostragem e ocultação de senhas em formulários, e a funcionalidade da barra de pesquisa, proporcionando uma experiência mais interativa e conversacional ao usuário.

### **<span style="color: #9A2EFE;">Linguagens de Marcação</span>**

#### **<span style="color: #AC58FA;">HTML 5</span>**
A Linguagem de Marcação de Hipertexto (HTML) é uma linguagem utilizada na construção de páginas na web, podendo ser interpretada por navegadores. O HTML não é considerado uma linguagem de programação, já que ele não pode criar funcionalidades dinâmicas. Ao invés disso, com o HTML, os usuários podem criar e estruturar seções, parágrafos e links usando elementos, tags e atributos. No projeto, essa linguagem foi utilizada em todo o front-end (parte visual de um sistema) para a estruturação das páginas web.

### **<span style="color: #9A2EFE;">Linguagens de Estilo</span>**

#### **<span style="color: #AC58FA;">CSS 3</span>**
Cascading Style Sheets ou Folhas de Estilo em Cascata (CSS), é um mecanismo para adicionar estilos a uma página web, aplicado diretamente nas tags HTML ou contido dentro das tags style. Também é possível adicionar estilos adicionando um link para um arquivo CSS que contém os estilos. O CSS foi utilizado para toda a estilização de cada página do nosso sistema, juntamente com o framework Bootstrap.

### **<span style="color: #9A2EFE;">Frameworks</span>**

#### **<span style="color: #AC58FA;">Bootstrap v5.3.3</span>**
O Bootstrap é um framework front-end e de código-fonte aberto, que disponibiliza componentes prontos para utilização, ganhando muita produtividade no desenvolvimento. Ele oferece uma coleção de elementos prontos, como botões, tabelas e formulários, que podem ser facilmente utilizados e personalizados. O framework segue os princípios de usabilidade e tendências de design para interfaces. Além disso, sua padronização permite que os sites obtenham uma aparência atraente e de boa visualização.

#### **<span style="color: #AC58FA;">Django 5.1.3</span>**
O Django é um framework web Python de código aberto, no qual destaca-se por oferecer um ambiente simplificado para a criação de soluções web escaláveis, além de proporcionar ferramentas robustas e eficientes aos desenvolvedores, dispensando a necessidade de reescrever códigos comuns a todos os projetos web em Python. Ele disponibiliza, portanto, uma estrutura pré-configurada e bibliotecas com código pronto, melhorando a produtividade e organização do desenvolvimento.

O framework utiliza a arquitetura  MVT *(Model-View-Template)*, representando, respectivamente, a lógica de negócios, a lógica de renderização e a de exibição da interface do usuário, facilitando a criação de aplicações e promovendo a separação das atividades e reutilização de partes do código. Essa abordagem é uma variação do tradicional padrão MVC *(Model-View-Controller)*, amplamente adotada em diversos frameworks e sistemas.
Além disso, essa estrutura prioriza a segurança, oferecendo recursos projetados para impedir ameaças como CSRF, XSS e SQL Injections. Também conta com proteções como validação automática de formulários e gerenciamento de autenticação, entre outros serviços.

Com a implementação do mapeamento “Objeto-Relacional”, o Django permite a interação do banco de dados através de classes e objetos Python, eliminando a necessidade de escrita SQL direta. Isso não apenas simplifica o acesso aos dados, mas também reduz os riscos de segurança e, ao mesmo tempo, melhora a legibilidade do código. Além disso, a estrutura facilita o mapeamento de URLs, vinculando *URLs* específicas às suas *View* correspondentes. Essa abordagem organizada direciona as solicitações do usuário para as seções apropriadas do código e agiliza a criação de URLs que são semânticas e fáceis de usar, melhorando, em última análise, a experiência do usuário e otimizando o desempenho do mecanismo de pesquisa.
O Django disponibiliza um painel administrativo pronto para uso, facilitando o gerenciamento de dados da aplicação, sendo gerado de forma automática a partir dos modelos definidos no projeto, além de vários outros recursos, sendo um framework completo sem a necessidade de recorrer a soluções externas.

### **<span style="color: #9A2EFE;">Bibliotecas</span>**

#### **<span style="color: #AC58FA;">Selenium v4.0</span>**
O Selenium é uma ferramenta para automatizar navegadores, usada especialmente para testes e aplicações web, permitindo a simulação de interações de usuários, como cliques e preenchimento de formulários, garantindo que funcionalidades atuem corretamente em diferentes navegadores e plataformas.

A biblioteca facilita a execução de testes repetitivos e de regressão, garantindo que novas alterações não afetem funcionalidades existentes.
Neste sistema, a biblioteca foi utilizada para o desenvolvimento da lógica para automatização da extração dos dados da catraca para serem salvos no banco de dados PostgreSQL, evitando erros manuais e economizando tempo.

#### **<span style="color: #AC58FA;">PyAutoGUI v0.9.54</span>**
O PyAutoGUI é uma biblioteca Python que permite automatizar a interação com a Graphical User Interface, ou Interface Gráfica do Usuário (GUI), do seu computador, podendo controlar o mouse, teclado, entre outros elementos visuais da tela, diferente do Selenium, que é focado exclusivamente em navegadores web.

O Selenium e o PyAutoGUI foram utilizados em conjunto para automatizar a coleta de dados da catraca e armazená-los no banco de dados PostgreSQL. Enquanto o Selenium foca na extração automatizada de dados por meio de navegação web, o PyAutoGUI foi essencial para interagir com a interface gráfica da máquina, controlando elementos visuais fora do navegador, como ações que não poderiam ser realizadas apenas via web. Essa combinação permitiu uma integração completa, eliminando erros manuais e garantindo a precisão dos dados coletados e armazenados.

#### **<span style="color: #AC58FA;">ReportLab v4.2.5</span>**
ReportLab é uma biblioteca para softwares que permite criar e gerar relatórios no formato desenvolvido pela empresa Adobe Incorporated conhecido como PDF (Portable Document Format). A biblioteca foi planejada para ser executada especialmente na linguagem Python, usando as fontes disponibilizadas pelas Fontes TrueType, disponibilizadas pela Apple Computer, em parceria com a Microsoft.

O uso da biblioteca ReportLab foi de extrema importância para a lógica de geração de relatórios referentes aos maiores atrasos e faltas do sistema, uma vez que disponibiliza diversas funções para estilização e estruturação de documentos em PDF.

#### **<span style="color: #AC58FA;">Schedule v1.2.2</span>**
Schedule é uma biblioteca para Python que possibilita executar códigos em horários específicos. Esta ferramenta foi utilizada para definir os horários de execução do código que automatiza a coleta de dados das catracas.

#### **<span style="color: #AC58FA;">Pandas v2.2.3</span>**
Pandas é uma biblioteca de manipulação e análise de dados, criada especialmente para Python, e foi utilizada para manipular os Arquivos de Texto (TXT) e Comma Separated Values (CSV) que armazenam os dados obtidos referentes às frequências.


### **<span style="color: #9A2EFE;">Banco de dados</span>**

#### **<span style="color: #AC58FA;">PostgreSQL</span>**
Escolher o PostgreSQL como banco de dados para este sistema de gerenciamento de atrasos e frequência traz diversas vantagens que garantem a eficiência e a robustez do projeto.

Primeiramente, o PostgreSQL é conhecido por seu alto desempenho e escalabilidade, o que é essencial para lidar com o grande volume de dados gerados pelo sistema, incluindo registros de entrada e saída dos alunos, onde o banco de dados cresce juntamente com o aumento da quantidade de alunos ou de informações armazenadas, sem comprometer a performance.

Além disso, o PostgreSQL oferece suporte a uma ampla gama de tipos de dados, o que permite a realização de consultas complexas, possibilitando a criação de relatórios detalhados e análises aprofundadas do comportamento dos alunos, algo crucial para o acompanhamento de frequência e atrasos.

Outro ponto forte é a conformidade do PostgreSQL com o modelo ACID (Atomicidade, Consistência, Isolamento, Durabilidade), garantindo a integridade e segurança dos dados, protegendo informações sensíveis.

Por fim, a integração nativa com Django, o framework utilizado no desenvolvimento do projeto, facilita a implementação do PostgreSQL, aproveitando ao máximo suas funcionalidades avançadas.

Essas características fazem do PostgreSQL uma escolha sólida e eficiente para o sistema de gerenciamento de atrasos, oferecendo uma base confiável e segura para o projeto.

### **<span style="color: #9A2EFE;">Outras Ferramentas</span>**

#### **<span style="color: #AC58FA;">Agendador de Tarefas V1.0</span>**
O Agendador de Tarefas é um programa disponibilizado pelo Windows que permite automatizar atividades repetitivas, bem como executar ações em um horário previamente especificado.
Para realizar o agendamento automático para executar o código que obterá o arquivo contendo os dados extraídos das catracas, optou-se pela utilização do Agendador de Tarefas do Windows, que, ao criar a tarefa, define informações básicas como nome, com qual condição será iniciada a tarefa e sua data de início, horário e dia específicos que ela será executada.

#### **<span style="color: #AC58FA;">Todas as Dependências</span>**

```python
attrs==24.2.0
certifi==2024.8.30
cffi==1.17.1
decouple==0.0.7
h11==0.14.0
idna==3.10
MouseInfo==0.1.3
outcome==1.3.0.post0
psycopg2==2.9.10
PyAutoGUI==0.9.54
pycparser==2.22
PyGetWindow==0.0.9
PyMsgBox==1.0.9
pyperclip==1.9.0
PyRect==0.2.0
PyScreeze==1.0.1
PySocks==1.7.1
python-dotenv==1.0.1
pytweening==1.2.0
schedule==1.2.2
selenium==4.25.0
sniffio==1.3.1
sortedcontainers==2.4.0
trio==0.27.0
trio-websocket==0.11.1
typing_extensions==4.12.2
urllib3==2.2.3
websocket-client==1.8.0
wsproto==1.2.0
```

### **<span style="color: #9A2EFE;">Metodologia para Desenvolvimento</span>**

Traduzido do inglês, Scrum é uma estrutura ágil de colaboração em equipe comumente usada no desenvolvimento de software e em outros setores. O Scrum prescreve que as equipes dividam o trabalho em metas a serem concluídas dentro de iterações com limite de tempo, chamadas sprints. Para desenvolver o projeto, fizemos a utilização da metodologia ágil Scrum, que nos permitiu organizar o trabalho em sprints curtos e interativos, garantindo entregas contínuas e adaptáveis.

---

## **<span style="color: #9A2EFE;">Levantamento de Requisitos</span>**

### **<span style="color: #AC58FA;">Requisitos Funcionais</span>**
- **<span style="color: #8000FF;"> [RF001] - Acesso ao software onde constam os dados de cada catraca**</span> 
    (informações de saída e entrada de alunos, data, horário e identificador único da carteirinha).
    - **Prioridade:** Alta.
    - **Descrição:** Permitir que os usuários autorizados acessem os dados das catracas, que registram as entradas e saídas dos alunos, com informações como data, horário e identificador único da carteirinha.
    - **Regras de Negócio:** O acesso deve ser restrito a usuários autorizados.
    - **Restrições Tecnológicas:** Deve ser compatível com o sistema de catracas existente.
    
- **<span style="color: #8000FF;">[RF002] - Exportação automática dos dados em horários determinados e unificação em um único banco de dados.**</span>
    - **Prioridade:** Alta.
    - **Descrição:** O sistema deve exportar automaticamente os dados das catracas em horários pré-definidos e consolidá-los em um banco de dados.
    - **Regras de Negócio:** A exportação deve ocorrer sem intervenção manual.
    - **Restrições Tecnológicas:** O sistema deve suportar agendamento de tarefas automáticas.
    
- **<span style="color: #8000FF;"> [RF003] - (Requisito descontinuado em 10/09) Acesso às informações da carteirinha de cada aluno para verificação de presença.** </span>
    - **Prioridade:** Alta.
    - **Descrição:** Permitir que os dados das carteirinhas dos alunos sejam utilizados
    para verificar a presença com base nos registros das catracas.
    - **Regras de Negócio:** A verificação deve ser precisa e em tempo real.
    - **Restrições Tecnológicas:** Integração com o sistema de gestão de carteirinhas.

- **<span style="color: #8000FF;">[RF004] - Notificação à gestão em caso de aluno com mais de 3 atrasos.**</span>
    - **Prioridade:** Alta.
    - **Descrição:** O sistema deve enviar notificações automáticas à gestão se algum aluno acumular mais de três atrasos.
    - **Regras de Negócio:** A notificação deve ser enviada de forma automática e
    imediata.
    - **Restrições Tecnológicas:** O sistema deve ser capaz de gerar e enviar
    notificações automáticas.

- **<span style="color: #8000FF;"> [RF005] - Geração de relatórios sobre atrasos.**</span>
    - **Prioridade:** Média.
    - **Descrição:** O sistema deve gerar relatórios que indiquem os alunos com mais e menos atrasos e faltas, além da porcentagem em um período determinado.
    - **Regras de Negócio:** Os relatórios devem ser precisos e acessíveis à gestão.
    - **Restrições Tecnológicas:** Deve permitir a exportação dos relatórios em formato
    PDF.
    
- **<span style="color: #8000FF;"> [RF006] - Ferramenta de busca de salas de aula e alunos.**</span>
    - **Prioridade:** Média.
    - **Descrição:** O sistema deve permitir a busca eficiente por salas de aula e alunos, exibindo dados relevantes como nome do estudante, instrutor responsável e quantidade de atrasos.
    - **Regras de Negócio:** A ferramenta de busca deve ser rápida e responsiva.
    - **Restrições Tecnológicas:** Integração com o banco de dados.
    
- **<span style="color: #8000FF;"> [RF007] - Lógica de autenticação e permissões.**</span>
    - **Prioridade:** Alta.
    - **Descrição:** Implementar uma lógica robusta de autenticação e autorização, permitindo que coordenadores adicionem, atualizem e excluam salas de aula e alunos.
    - **Regras de Negócio:** Apenas usuários autorizados podem realizar alterações.
    - **Restrições Tecnológicas:** Deve usar protocolos de segurança modernos.
    
- **<span style="color: #8000FF;"> [RF008] - Acesso às informações da carteirinha dos alunos do Grupo 03 (desenvolvedores) para demonstração de verificação de presença.**</span>
    - **Prioridade:** Alta
    - **Descrição:** Permitir que os dados das carteirinhas dos alunos sejam utilizados para verificar a presença com base nos registros das catracas.
    - **Regras de Negócio:** A verificação deve ser precisa e em tempo real.
    - **Restrições Tecnológicas:** Integração com o sistema de gestão de carteirinhas.
    

### **<span style="color: #9A2EFE;">Requisitos Não Funcionais</span>**

- **<span style="color: #8000FF;"> [RNF001] - Acesso restrito à rede ADM (catraca).**</span>
    - **Prioridade:** Alta
    - **Descrição:** O sistema deve ser acessível apenas pela rede interna da instituição para garantir segurança e integridade dos dados.
    - **Regras de Negócio:** O acesso fora da rede ADM deve ser bloqueado.
    - **Restrições Tecnológicas:** Implementação de firewall e restrições de rede.

- **<span style="color: #8000FF;"> [RNF002] - Segurança contra invasões e vazamento de dados.**</span>
    - **Prioridade:** Alta
    - **Descrição:** Implementar medidas de segurança avançadas para proteger o sistema contra-ataques e vazamentos de dados.
    - **Regras de Negócio:** A segurança deve ser auditada regularmente.
    - **Restrições Tecnológicas:** Implementação de criptografia de dados e monitoramento de segurança.

- **<span style="color: #8000FF;"> [RNF003] - Design interativo e organizado.**</span>
    - **Prioridade:** Média
    - **Descrição:** O sistema deve ter uma interface amigável, com design interativo e bem-organizado, facilitando a navegação e uso pelos usuários.
    - **Regras de Negócio:** O design deve seguir as diretrizes de usabilidade.
    - **Restrições Tecnológicas:** Compatibilidade com diferentes dispositivos e navegadores.
    
- **<span style="color: #8000FF;"> [RNF004] - Código comentado e documentação.**</span>
    - **Prioridade:** Média
    - **Descrição:** O código do sistema deve ser bem comentado e acompanhado de documentação clara, facilitando a manutenção e futuras atualizações.
    - **Regras de Negócio:** A documentação deve ser mantida atualizada com as mudanças no sistema.
    - **Restrições Tecnológicas:** A documentação deve ser acessível a todos os
    membros da equipe de desenvolvimento.


## **<span style="color: #9A2EFE;">Arquitetura do Sistema</span>**

### <span style="color: #9A2EFE;">**Diagrama Model-Template-View (MTV)**</span>

A arquitetura MTV significa Model-Template-View, e é um padrão de design de software para projetos que utilizam o framework Django. A seguir, o diagrama representa visualmente o funcionamento da arquitetura deste framework:

![alt text](img/Diagrama_MTV.png)

A seguir, está uma descrição de cada camada que estão presentes na arquitetura MTV:
- **Model:** responsável pelo mapeamento do banco de dados, que possui uma comunicação direta com ele. As Models estão contidas no arquivo *models.py*.
- **Template:** pasta que conterá os arquivos .html para as páginas do sistema. Receberá das Views os dados que aparecerão no front-end do sistema.
- **View:** onde é feita a lógica de negócio. Receberá os dados do app da Model e mandará para os Templates. As Views são as funções presentes no arquivo *views.py*.
As setas sólidas representam uma relação direta entre os componentes do diagrama, enquanto a seta pontilhada representa uma relação menos direta. Duas setas presentes no diagrama possuem duas pontas, o que significa uma comunicação entre os dois componentes.

---

### <span style="color: #9A2EFE;">**Diagrama de Classes**</span>

Um Diagrama de Classes é uma representação gráfica amplamente utilizada na engenharia de software para descrever a estrutura estática de um sistema, representando suas classes, atributos, métodos e os relacionamentos entre elas. Este tipo de diagrama segue o padrão UML (Unified Modeling Language ou Linguagem de Modelagem Unificada), que é amplamente utilizado para a padronização de modelagem e documentação de sistemas de software. A seguir, o diagrama representa visualmente o funcionamento da estrutura do sistema:

![alt text](img/Diagrama_de_Classes.png)

No Diagrama de Classes apresentado, estão representadas as entidades fundamentais do sistema, destacando seus atributos, métodos e os tipos de relacionamento entre as classes, como associação, agregação, composição e herança.
As classes são os elementos básicos de um Diagrama de Classes, representando abstrações de objetos do mundo real ou conceitos relacionados ao sistema. Cada classe é descrita com seus atributos (dados que ela armazena) e métodos (operações que ela realiza). A seguir, está uma descrição das classes presentes no diagrama:
- **Usuario:** representa os usuários que possuem acesso ao sistema, como coordenadores e administradores. Inclui atributos como nome, sobrenome, username e cargo.
- **Aluno:** representa os estudantes registrados no sistema. Seus atributos incluem informações como nome, id_carteirinha e id_curso.
- **Frequencia:** representa a classe responsável por armazenar os registros vindos da catraca, com atributos como id, id_aluno, data, hora e identificador (1 ou 2, entrada ou saída, respectivamente).
- **Curso:** representa os cursos disponíveis na instituição. Contém atributos como turma, nome_curso, horario_entrada, horario_saida, carga_horaria, responsavel, dias_funcionamento, data_inicio, data_fim, carga_horaria_intervalo e dias_letivos.

Os relacionamentos entre classes em um Diagrama de Classes são fundamentais para entender a estrutura e as interações do sistema. Os principais tipos de relacionamentos presentes incluem:
- **Relacionamento entre Aluno e Curso:** cada aluno está vinculado a apenas um curso, utilizando a chave estrangeira id_curso na classe Aluno para referenciar a classe Curso. Por outro lado, um curso pode estar associado a vários alunos (0..* para Aluno e 1 para Curso).
- **Relacionamento entre Aluno e Frequência:** um aluno pode ter vários registros de frequência, mas cada registro está associado a um único aluno, representado pela chave estrangeira id_aluno na classe Frequência (1 para Aluno e 0..* para Frequência).

---

### <span style="color: #9A2EFE;">**Diagrama de Entidade e Relacionamento**</span>

O Diagrama de Entidade-Relacionamento (DER) é uma representação gráfica amplamente utilizada para descrever a estrutura lógica de um banco de dados, representando suas entidades, atributos e os relacionamentos entre elas. Ele é essencial para planejar e visualizar como os dados são organizados e como as diferentes entidades do sistema interagem.

![alt text](img/Diagrama_ER.webp)

**Relacionamentos e Simbologias das Entidades do Sistema:**

- ***auth_user*** e ***web_usuario*:** cada usuário em auth_user possui uma associação obrigatória e única com um registro em web_usuario. Isso indica um relacionamento 1:1.
    - **Representação:**
        - Traços duplos indicam que o relacionamento é obrigatório e único.
        - Cada registro em auth_user está associado diretamente a um registro correspondente em web_usuario.
    - **Implementação no Banco de Dados:**
        - A tabela web_usuario possui um campo username, que é a chave primária e uma chave estrangeira que referencia o campo username de auth_user, respectivamente.

- ***web_aluno*** e ***web_frequencia*:** um aluno em web_aluno pode estar associado a várias frequências registradas em web_frequencia. O relacionamento é do tipo 1:N.
    - **Representação:**
        - No lado de web_aluno, os dois traços verticais indicam que uma frequência está obrigatoriamente vinculada a um aluno.
        - No lado de web_frequencia, o pé de galinha indica que um aluno pode ter várias frequências registradas.
    - **Implementação no Banco de Dados:**
        - A tabela web_frequencia possui o campo id_aluno_id como chave estrangeira, que referencia o campo id_carteirinha da tabela web_aluno.

- ***web_aluno*** e ***web_curso*:** um aluno em web_aluno está associado a exatamente um curso em web_curso. O relacionamento é do tipo N:1, onde vários alunos podem estar vinculados a um único curso.
    - **Representação:**
        - No lado de web_aluno, o pé de galinha indica que vários alunos podem estar associados ao mesmo curso.
        - No lado de web_curso, os dois traços verticais indicam que o relacionamento é obrigatório e único para cada aluno.
    - **Implementação no Banco de Dados:**
        - A tabela web_aluno possui o campo id_curso como chave estrangeira, que referencia o campo turma da tabela web_curso.

---

### <span style="color: #9A2EFE;">**Diagrama de Casos de Uso**</span>

![alt text](img/Diagrama_de_Casos_de_Uso.webp)

No Diagrama de Caso de Uso apresentado, são representadas as interações entre diferentes atores (usuários do sistema) e as funcionalidades disponíveis no projeto desenvolvido, destacando a relação entre ações e dependências. A seguir, está uma descrição detalhada de cada elemento.

### <span style="color: #AC58FA;">**Atores**</span>

Os atores são os usuários que interagem com o sistema, podendo ser uma pessoa, uma organização ou um sistema externo que interage com seu aplicativo ou sistema. Eles devem ser objetos externos que produzam ou consumam dados. A seguir, está uma descrição dos atores presentes no Modelo de Caso de Uso.
- **Coordenador:** Responsável por gerenciar usuários e realizar atividades relacionadas à frequência e atrasos dos alunos.
- **Administrador:** Atua na administração geral do sistema, incluindo a criação e manutenção de usuários, cursos e alunos.
- **Catraca (Sistema Automatizado):** Representa o sistema que fornece registros de entrada e saída dos alunos. Integra ferramentas como Selenium e Pandas para automação de processos.

### <span style="color: #AC58FA;">**Relacionamentos**</span>

Em um Diagrama de Casos de Uso, tanto a inclusão quanto a extensão e associação, são relacionamentos que descrevem como diferentes casos de uso interagem ou se relacionam entre si. A seguir, está a explicação de como cada interação funciona:
- **Inclusão (include):** a inclusão é usada para mostrar que um caso de uso sempre incorpora ou "inclui" o comportamento de outro caso de uso. É como se o caso de uso principal delegasse parte de seu comportamento a um caso de uso incluído.
- **Extensão (extend):** a extensão é usada para mostrar que um caso de uso estende o comportamento de outro caso de uso sob certas condições. Isso significa que o comportamento do caso de uso original pode ser expandido por outro caso de uso opcional, dependendo de uma condição específica.
- **Associação:** uma associação é um relacionamento entre um ator e um caso de uso de negócios. Indica que um ator pode usar a funcionalidade do sistema de negócios. Ela é uma é representada como uma linha que liga os elementos a serem relacionados.

### <span style="color: #AC58FA;">**Casos de Uso**</span>

Os casos de uso, sendo apresentados de forma visual pelo formato oval na horizontal, representam os diferentes usos que um usuário pode ter, ou seja, são as funcionalidades do sistema. A seguir, será fornecida uma explicação de cada caso de uso, citando também quais usuários podem acessá-los:

### <span style="color: #AC58FA;">**Casos de Uso do Coordenador e Administrador:**</span>

- **Login:** permite que tanto o coordenador quanto o administrador acessem o sistema. O caso de uso possui uma relação de inclusão com o caso de uso “verificar a existência do usuário”, onde as credenciais fornecidas são verificadas. Se as credenciais corresponderem a um usuário cadastrado, o acesso é concedido; caso contrário, uma mensagem de erro é exibida.
- **Criar, Editar e Excluir Curso ou Aluno:** tanto o coordenador quanto o administrador podem adicionar novos cursos e alunos ao sistema. Contudo, as funcionalidades de edição e exclusão é exclusiva ao administrador, podendo apenas ele, gerenciar tais funções, a fim de garantir um maior controle sobre as modificações.
Além disso vale destacar que, para executar os processos mencionados, é realizada uma verificação prévia da existência do curso ou aluno em questão. Essa validação é feita pelos casos de uso “verificar se o curso já existe” e “verificar se o aluno já existe”.
- **Visualizar Cursos:** tanto o coordenador quanto o administrador podem visualizar uma lista completa de todos os cursos cadastrados, contendo informações de nome, código da turma e responsável. Esse caso de uso, tem relações de extensão com os casos de visualização dos alunos, onde é apresentada as informações de cada um, e o de filtragem de resultados, sendo uma ferramenta de busca.
- **Filtrar Resultados:** permite que tanto o coordenador quanto o administrador, filtrem a visualização de informações, sendo uma ferramenta de busca para pesquisar um determinado curso.
- **Visualizar Informações dos Alunos:** apresenta ao coordenador uma lista detalhada de informações sobre os alunos, incluindo frequência, faltas e atrasos registrados, com base no caso de uso “calcular frequência, faltas e atrasos do aluno” e “filtrar os alunos por curso”, tendo uma relação de inclusão entre ambos.
- **Calcular Frequência, Faltas e Atrasos:** é uma consulta no banco de dados para efetuar os cálculos relacionados ao desempenho de frequência dos alunos, baseando-se nos registros de entrada e saída e nas regras definidas para atrasos e faltas. Tal caso de uso tem um relacionamento do tipo extensão com o caso de uso de “notificações”, que notifica o coordenador e o administrador caso um aluno exceda a quantidade limite de atrasos.
Além disso, ele tem uma relação de inclusão com os casos de uso de “visualização das informações dos alunos” e de “geração de relatório”, pois ambas as funcionalidades exigem o cálculo do desempenho acadêmico do estudante.
- **Notificação:** envia alertas automáticos tanto ao coordenador quanto ao administrador quando um aluno excede o limite de atrasos. Esse recurso é um caso de uso opcional, sendo o relacionamento extensão, acionado em situações específicas.
- **Filtrar os Alunos por Curso:** é uma funcionalidade cuja responsabilidade é de “filtrar os alunos por turma”.
- **Gerar Relatórios:** tanto o coordenador quanto o administrador podem gerar documentos em formato PDF com informações sobre frequência, atrasos e faltas dos alunos com pior desempenho. Os relatórios são uma ferramenta essencial para as análises.
- **Criar, Editar e Excluir Usuário:** somente o administrador possui acesso a essas funcionalidades, que ao efetuar alguma, ocorre a verificação se o usuário já existe ou não.
Ademais, é importante destacar que a edição de informações só pode ser realizada através da rota “/admin”, pois o sistema não conta com uma lógica específica para permitir esse tipo de modificação. Além disso, para todos os casos de uso explicados anteriormente, é necessária a autenticação do usuário no sistema.

### <span style="color: #AC58FA;">**Casos de Uso do Sistema Automatizado (Catraca):**</span>

- **Criação de Registro de Entrada e Saída:** a integração com a catraca permite capturar registros de entrada e saída de alunos de forma automática. Isso inclui o uso de ferramentas como Selenium e PyAutoGUI para processar os dados rapidamente.
- **Validação de Registros:** antes de armazenar as informações capturadas, o sistema valida os registros para garantir que estão completos e corretos. Essa validação previne erros que possam impactar relatórios ou cálculos. Além do mais, esse caso de uso está incluído ao de criação de registro de entrada e saída do estudante.

Com o detalhamento do Diagrama de Caso de Uso apresentado, torna-se mais fácil a compreensão de como o sistema funciona de forma geral, proporcionando uma visão mais clara de suas funcionalidades e interações.

---

### <span style="color: #AC58FA;">**Fluxograma**</span>

![alt text](img/Fluxograma.jpg)

#### <span style="color: #AC58FA;">**Seção Usuário**</span>

- **Realiza Logout**: O usuário pode sair do sistema, encerrando a sessão e sendo redirecionado à Página Inicial, protegendo a privacidade dos dados.  
- **Acessa Página Inicial**: Página de entrada do sistema, exibida inicialmente para usuários não autenticados, com informações básicas e opções de navegação.  
- **Tenta Login**: Caso não esteja autenticado, o usuário é direcionado à Página de Login para inserir suas credenciais.  
- **Insere Credenciais**: O usuário preenche o formulário com nome de usuário e senha, e os dados são enviados para validação.  
- **Verifica Autenticação**:  
  - **Se autenticado**: O sistema identifica o grupo de acesso e redireciona:  
    - **Coordenação**: Página de Cursos.  
    - **Administração**: Página de Cursos com acesso a funcionalidades administrativas.  
  - **Se não autenticado**: Exibe mensagem de erro e redireciona à Página de Login.  
- **Acessa Página de Cursos**: Usuários da Coordenação podem gerenciar cursos, com funcionalidades como exibição de notificações, busca por cursos e visualização de detalhes das turmas.  
- **Acessa Página de Alunos**: Permite gerenciar alunos vinculados a um curso, incluindo visualização da lista, detalhes individuais e exclusão de registros.

#### <span style="color: #AC58FA;">**Seção Sistema**</span>  

- **Gerenciamento de Cursos e Alunos**: Centraliza o controle de dados para atualizações diretas no banco.  
- **Retorna à Página Inicial**: Usuários não autenticados ou em logout são redirecionados à Página Inicial.  
- **Exibe Resultados da Pesquisa**: Mostra resultados com base nos critérios definidos pelo usuário, otimizando a navegação.  
- **Gera uma Notificação**: Alerta eventos importantes, como mais de três atrasos de um aluno.  
- **Atualiza a Lista de Alunos**: Mantém a lista sincronizada após adições ou exclusões de alunos.  

#### <span style="color: #AC58FA;">**Seção Administrativa**</span> 

- **Ações Administrativas**: Usuários administrativos podem:  
  - Cadastrar ou excluir alunos e cursos.  
  - Processar dados do site.  
  - Gerar relatórios detalhados.  
- **Recebe e Visualiza Relatórios**: Relatórios de frequência, atrasos e cursos ajudam na tomada de decisões estratégicas.  

#### <span style="color: #AC58FA;">**Seção Automação**</span>  

- **Coleta Dados da Catraca**: Registra automaticamente a passagem do aluno na catraca, iniciando o controle de frequência.  
- **Verifica Registro de Presença**: Analisa a situação do aluno:  
  - **Falta**: Sem registro nos horários esperados.  
  - **Atraso**:  
    - **Mais de 10 minutos**: Marcado como atrasado.  
    - **Menos de 10 minutos**: Dados armazenados sem penalização.  

#### <span style="color: #AC58FA;">**Seção Banco de Dados**</sp>  

- **Insere Dados no Banco**: Registra automaticamente informações coletadas pela catraca.  
- **Armazena Dados de Frequência**: Mantém histórico detalhado de presença dos alunos.  
- **Visualiza Dados Salvos**: Permite consultar registros de frequência e informações dos alunos.  
- **Atualiza Dados no Banco**: Reflete alterações como inclusão ou exclusão de alunos e cursos.  

#### <span style="color: #AC58FA;">**Seção Catraca**</span>  

- **Aluno Passa pela Catraca**: O registro da catraca inicia a automação para análise e controle da frequência.  

---

## <span style="color: #9A2EFE;">**Visual das Interfaces**</span>
### <span style="color: #AC58FA;">**Interface Inicial**</span>

A página inicial conta com uma barra de navegação localizada no topo, onde a logo do SENAI está posicionada no lado esquerdo e, no lado direito, encontra-se um componente padrão: um botão para troca de tema, permitindo a alternância da coloração da página entre os temas claro e escuro. No conteúdo principal, há um texto com o título da página e um botão que redireciona o usuário para a página de Login.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/home- white.webp" alt="Homepage - white" width="45%">
  <img src="img/paginas/home- dark.webp" alt="Homepage - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Login**</span>

Após o redirecionamento para a página de Login, o usuário deve inserir seus dados, como username e senha. Ao lado do campo de senha, há um ícone que permite exibir ou ocultar a senha, alterando sua aparência de acordo com a ação: um olho riscado quando a senha está visível e um olho aberto quando ela está oculta. Caso os dados sejam inseridos corretamente e o botão de Login seja clicado, o usuário será redirecionado para a página de Cursos. No entanto, se houver erro nos dados fornecidos, será exibida a mensagem: “Nome de usuário ou senha incorretos”.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/login- white.webp" alt="Login - white" width="45%">
  <img src="img/paginas/login- dark.webp" alt="Login - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Cursos**</span>

Após a realização do Login, o usuário é redirecionado para a página de Cursos. A barra de navegação, presente em todas as páginas, passa a ser exibida. Após o Login, uma mensagem no formato “Olá, usuário”, onde o nome do usuário correspondente é mostrado. Além disso, é adicionado um novo componente que abre um Offcanvas, um elemento do Bootstrap que exibe uma barra lateral. Essa barra contém opções para Logout (saída), redirecionamento para as página de Cadastro, Criar Alunos, Criar Cursos e de Importação de Frequência. Os componentes de Cadastro, Aluno, Curso e Frequência são exibidos de forma exclusiva para o Administrador.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/offcanvas- white.webp" alt="Offcanvas - white" width="45%">
  <img src="img/paginas/offcanvas- dark.webp" alt="Offcanvas - dark" width="45%">
</p>
A interface da página de Cursos apresenta, de forma centralizada, um texto com o nome da página. Logo abaixo, são exibidos ícones alinhados da esquerda para a direita: relatórios, que redireciona o usuário para a página de Relatórios; notificações, que leva à página de Notificações; e uma lupa de pesquisa, que é exibida uma barra onde o usuário pode realizar busca dos cursos. Para que a pesquisa funcione corretamente, é necessário digitar o nome do curso com as devidas acentuações. Após clicar no botão de pesquisa, serão exibidos apenas os cursos correspondentes ao nome buscado.
No conteúdo principal da página, os cursos são listados em linhas, apresentando as seguintes informações de forma organizada: o nome do curso, o código (identificador único) da turma e o responsável pela turma.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/cursos- white.webp" alt="Cursos - white" width="45%">
  <img src="img/paginas/cursos- dark.webp" alt="Cursos - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Alunos**</span>

Na página de Cursos, ao clicar em qualquer um dos cursos listados no conteúdo principal, o usuário é redirecionado para a página de Alunos, onde são exibidos os alunos específicos do curso selecionado.
No topo, no canto esquerdo, há um componente que permite retornar à página anterior (página de Cursos).
No conteúdo da página de Alunos, é exibido uma lista dos alunos, onde é informado dados sobre eles, como: nome do aluno, quantidade de atrasos, porcentagem de frequência e quantidade de faltas. Vale ressaltar que, acessando pelo perfil de Administrador, é exibido uma opção de excluir o aluno, utilizada em casos de desistência.
Ao lado da lista de alunos, é exibido informações sobre o curso, como: o responsável pela turma, código do curso e o seu horário de funcionamento. Adicionalmente, para o perfil de Administrador, há um botão que permite excluir o curso.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/alunos- white.webp" alt="alunos - white" width="45%">
  <img src="img/paginas/alunos- dark.webp" alt="alunos - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Cadastro**</span>

No Offcanvas, ao clicar no componente de Cadastro, o usuário Administrador é redirecionado para a página de Cadastro. Na parte superior da página, no canto esquerdo, há um componente que permite retornar à página anterior (página de Cursos).
O conteúdo principal exibe um formulário destinado ao cadastro de um novo usuário. Esse formulário solicita as seguintes informações: nome, sobrenome, nome de usuário e senha.
É importante ressaltar que o novo usuário é salvo automaticamente como Coordenador ao concluir o cadastro de novo usuário.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/cadastro- white.webp" alt="cadastro - white" width="45%">
  <img src="img/paginas/cadastro- dark.webp" alt="cadastro - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Relatórios**</span>

Na página de Cursos, ao clicar no ícone de relatórios, o usuário é redirecionado para a página de Relatórios. No topo, no canto esquerdo, há um botão que permite retornar à página anterior (página de Cursos).
No centro da página, o conteúdo apresenta uma imagem ilustrativa e dois botões dispostos um abaixo do outro:
- O primeiro botão exibe o texto: “Gerar relatório em PDF”, ao clicar, será feito o *download* de um documento contendo tabelas com os dados dos alunos com mais atrasos e dos alunos com mais faltas.
- O segundo botão exibe uma modal na tela, ao clicar, abre-se uma *modal* que contém um texto curto informando ao usuário o que será feito ao clicar no botão acima e o objetivo para qual o documento baixado será utilizado.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/relatorio- white.webp" alt="relatorio - white" width="45%">
  <img src="img/paginas/relatorio- dark.webp" alt="relatorio - dark" width="45%">
</p>
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/sobre- white.webp" alt="sobre - white" width="45%">
  <img src="img/paginas/sobre- dark.webp" alt="sobre - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Notificações**</span>

Na página de Cursos, ao clicar no ícone de notificações, o usuário é redirecionado para a página de Notificações. No canto superior esquerdo, há um componente que permite retornar à página anterior (página de Cursos).
No centro do conteúdo, a página exibe o título Notificações e, logo abaixo, uma lista dos alunos com 3 ou mais atrasos. As informações apresentadas incluem: o nome do aluno, a quantidade de atrasos e sua turma correspondente. Caso nenhum aluno atenda a esse critério, a lista permanecerá vazia.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/notificacao- white.webp" alt="notificacao - white" width="45%">
  <img src="img/paginas/notificacao- dark.webp" alt="notificacao - dark" width="45%">
</p>

### <span style="color: #AC58FA;">**Interface de Adição de Alunos, Cursos e Frequências**</span>

Todas as páginas de adição seguem o mesmo layout, proporcionando uma experiência de usuário mais intuitiva. Nessa interface, o usuário pode carregar arquivos nos formatos apropriados para o sistema e realizar operações de cadastro ou atualização de dados. A página de criação de frequência foi desenvolvida especificamente para inserir dados fictícios dos alunos.
- **Botão "Escolher arquivo"**: permite selecionar um arquivo armazenado no dispositivo.
- **Indicação do nome do arquivo**: após a seleção, o nome do arquivo será exibido ao lado do botão.
- **Botão "Enviar"**: submete o arquivo selecionado para processamento.
Para o cadastro de alunos e cursos, o arquivo deve ser no formato CSV, enquanto para a criação de frequência, o arquivo deve ser no formato TXT.
Em conclusão, este manual visa facilitar o uso do sistema, proporcionando uma navegação simples e eficiente para o usuário. Com as funcionalidades de upload de arquivos, o processo de cadastro e atualização de dados se torna rápido e prático. Caso surjam dúvidas ou dificuldades, a equipe de suporte estará disponível para garantir que sua experiência seja a mais tranquila possível.
<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/paginas/adicionar- white.webp" alt="adicionar - white" width="45%">
  <img src="img/paginas/adicionar- dark.webp" alt="adicionar - dark" width="45%">
</p>


## <span style="color: #9A2EFE;">**Implementação**</span>
### <span style="color: #AC58FA;">**v0.0 - Configuração do Ambiente de Desenvolvimento**</span>

A preparação do ambiente de desenvolvimento é iniciada com a criação do ambiente virtual (*venv*), instalando as dependências Django e Pillow, criando o projeto. Em seguida, fez-se a instalação do PostgreSQL localmente, definindo-o como banco de dados do sistema, através dos seguintes passos:

Primeiramente, foi consultada a documentação oficial do [*PostgreSQL*](https://www.postgresql.org/download/) e, em seguida, para a página do instalador [*EDB*](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads), na sessão de downloads, é baixado a versão 16.4 para a arquitetura Windows x86-64. Posteriormente, iniciou-se a pré-instalação e, quando solicitado para escolher os componentes, foi desmarcada a opção *Stack Builder*.

Após isto, foi inserida a senha para o super usuário e foram aceitas as configurações padrão do instalador. Ao término da instalação, deu-se início à configuração do servidor.

Na barra de pesquisa do Windows, foi feita a busca por pgAdmin 4, que é uma aplicação instalada em conjunto com o PostgreSQL, permitindo a configuração e interação com o banco de dados com uma aparência interativa para o usuário.

Para registrar o servidor, foi escolhida a opção *Service* e foi clicado o botão direito sobre ela, selecionando, em seguida, a opção *Register* e *Server*.

Na aba *General*, na opção de nome, foi inserido o nome do servidor. Em seguida, na aba de *Connection*, no campo *Host name/address*, foi digitado o nome do host e, posteriormente, a senha definida na pré-instalação do PostgreSQL. Por fim, foi executada a opção chamada *Save password,* depois *Save*.

Para criar uma base de dados, foi selecionada a opção, com o botão direito, o nome do servidor e, depois, Create e Database. Na caixa de diálogo que é posteriormente aberta, inseriu-se o nome para o Banco de Dados, sendo salvo em seguida.  A base de dados já havia sido criada com as tabelas padrões do Django. Com ela criada, o último passo é configurar os arquivos do framework.

Com o ambiente de desenvolvimento criado e o ambiente virtual (venv) ativado, foram instalados os pacotes *psycopg2* e *python-decouple, através dos* seguintes comandos no terminal:

```python
pip install psycopg2
pip install python-decouple
```
No arquivo _[settings.py](http://settings.py)_, já incluído na pasta do projeto, importamos a configuração do pacote _double_ e nas configurações do banco de dados, substituímos as configurações padrão do SQLite.

```python
DATABASES = {
    'default': {
        "ENGINE": "django.db.backends.postgresql",
        "NAME": config('DB_NAME'),
        "USER": config('DB_USER'),
        "PASSWORD": config('DB_PASSWORD'),
        "HOST": config('DB_HOST'),
        "PORT": config('DB_PORT'),
    }
}
```

Em seguida, um arquivo .env foi criado, contendo as informações (nome, usuário, senha, host e porta) do banco de dados que não serão exibidas na documentação por motivos de segurança. Por fim, foram gravadas as configurações da base de dados, criando-se então o super usuário.

### <span style="color: #AC58FA;">v0.1 - Configuração do Ambiente do Selenium</span>

#### <span style="color: #AC58FA;"> 1. **Instale o Python**</span>

Se ainda não tiver o Python instalado:

- Acesse [python.org](https://www.python.org/downloads/) e baixe a versão mais recente.

---

#### <span style="color: #AC58FA;"> 2. **Crie um Ambiente Virtual (Recomendado)**</span>

Crie um ambiente virtual para isolar as dependências do projeto:

```bash
python -m venv selenium_env
```

Ative o ambiente:

- **Windows**:
    
    ```bash
    selenium_env\Scripts\activate.ps1
    ```
    
- **Linux/Mac**:
    
    ```bash
    source selenium_env/bin/activat
    ```
    
---

#### <span style="color: #AC58FA;"> 3. **Instale o Selenium**</span>

Instale o Selenium via pip:

```bash
pip install selenium
```

---

#### <span style="color: #AC58FA;"> 4. **Baixe o WebDriver**</span>

O Selenium usa um WebDriver para interagir com os navegadores. Escolhlla o WebDriver compatível com o navegador que deseja usar:

#### <span style="color: #AC58FA;">Navegadores comuns e seus WebDrivers:</span>

- **Google Chrome**: [ChromeDriver](https://chromedriver.storage.googleapis.com/index.html?path=114.0.5735.90/)
- **Mozilla Firefox**: [GeckoDriver](https://github.com/mozilla/geckodriver/releases)
- **Microsoft Edge**: [EdgeDriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
- **Safari**: O SafariDriver já vem integrado no macOS.

Certifique-se de:

- Baixar a versão do WebDriver compatível com a versão do navegador.
- Colocar o executável do WebDriver em uma pasta do PATH ou especificar seu caminho no código.

---

#### <span style="color: #AC58FA;"> 5. **Teste a Configuração**</span>

Crie um script básico para testar:

```python
python
Copiar código
from selenium import webdriver

# Substitua 'path_to_webdriver' pelo caminho do WebDriver baixado
driver = webdriver.Chrome(executable_path='path_to_webdriver')

driver.get('https://www.google.com')
print("Título da página:", driver.title)
driver.quit()

```


### <span style="color: #AC58FA;">v0.2 - Criação do Aplicativo</span>
Após a criação do projeto e as configurações iniciais do ambiente, foi criado o aplicativo (ou módulo) dentro do diretório do projeto.

#### <span style="color: #AC58FA;">**Um projeto em Django?**</span>

O projeto é a estrutura que comportará nossos módulos e todos os demais arquivos da aplicação.

#### <span style="color: #AC58FA;">**Um módulo em Django?**</span>

Pode-se facilmente exemplificar comparando-o com um e-commerce que tenha um blog. Um dos módulos seria o e-commerce e o outro o blog, sendo assim nesta estrutura um projeto e dois módulos. Em outras palavras, são aplicações que não interagem umas com as outras, mas fazem parte de um mesmo projeto.

Posteriormente, criamos as pastas Templates e Static, contendo os arquivos HTML e subpastas que terão os arquivos de imagem, estilização e JavaScript, respectivamente. A estrutura do projeto se encontra desta forma:

```python
frequency_management/
    frequency_management/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
    media/
    static/
	    img/
		css/
		js/
    templates/
    web/
		templates/
    manage.py
```

Com a estrutura pronta, deu-se início à criação das URLs e Views.

### <span style="color: #AC58FA;">v0.3 - Criação das URLs, Views e Models</span>

Com o módulo criado, houve a criação das *URLs*. Para isso, foram realizados alguns procedimentos para configurar o projeto com o novo aplicativo, a fim de deixá-lo apto a recebê-las. Primeiro, o grupo registrou o módulo no arquivo *settings.py*. É importante ressaltar que todo o aplicativo criado deve ser registrado para que a aplicação o reconheça.

No arquivo **`*frequency_management/settings.py*`**:

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'web',
]
```
No arquivo urls.py dentro da pasta “web”, os desenvolvedores inseriram o seguinte código:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.homepage, name='homepage'),
    path('login', views.login, name='login'),
    path('cadastro', views.cadastro, name='cadastro'),
    path('cursos', views.cursos, name='cursos'),
    path('alunos/<str:turma>', views.alunos, name='alunos'),
    path('relatorio', views.relatorio, name='relatorio'),
    path('notificacoes', views.notificacoes, name='notificacoes'),
    path('criar_curso', views.criar_cursos, name='criar_curso'),
    path('criar_aluno', views.criar_alunos, name='criar_aluno'),
    path('excluir_curso/<str:turma>', views.delete_curso, name='excluir_curso'),
    path('excluir_aluno/<str:turma>/<str:id_carteirinha>', views.delete_aluno, name='excluir_aluno'),
    path('logout', views.logout, name='logout'),
    path('freq', views.upload_frequencia, name='freq')
]

handler404 = 'django.views.defaults.page_not_found'

```
Neste arquivo conterá todas as *urls* do aplicativo. Nota-se que houve a importação de uma *view*, chamada homepage.

Logo após isso, no arquivo de *urls* principal, foram registradas as rotas do módulo criado.

No arquivo **`*frequency_management/web/urls.py*`**:

```python
from django.contrib import admin
from django.urls import path, include
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('web.urls')),

] + static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
```

Primeiramente, são importados alguns componentes:
- **<span style="color: #4682B4;">admin:</span>**  é uma interface de administração automática que fornece uma interface poderosa para produção para adicionar conteúdo ao site
- **<span style="color: #4682B4;">path:</span>** este método cria as _urls_, recebe parâmetros como o próprio path e a _view_ ou conjunto de _views_ que serão acessadas;
- **<span style="color: #4682B4;">include:</span>** serve para incluir um conjunto de views, como é feito nas do módulo;
- **<span style="color: #4682B4;">static:</span>** usado para lidar com arquivos estáticos e de mídia durante o desenvolvimento.

Este arquivo representa todas as _rotas_ do projeto (todas as criadas no módulo), onde serão importadas para o projeto a partir da linha:

```
path('', include('web.urls'))
```

A elaboração das classes foi realizada no arquivo models.py, conforme é solicitado na documentação do Django:

```python
from django.db import models
from django.contrib.postgres.fields import ArrayField


TIPO_USUARIOS = (
    ("COORDENACAO", "Coordenacao"),
    ("ADMINISTRAÇÃO", "Administração")
)

DIAS_DA_SEMANA = [
        ('SEG', 'Segunda-feira'),
        ('TER', 'Terça-feira'),
        ('QUA', 'Quarta-feira'),
        ('QUI', 'Quinta-feira'),
        ('SEX', 'Sexta-feira')
    ]


class Curso(models.Model):
    turma = models.CharField(max_length=100, primary_key=True)
    nome_curso = models.CharField(max_length=100)
    horario_entrada = models.TimeField()
    horario_saida = models.TimeField()
    carga_horaria = models.IntegerField(default=1200)
    responsavel = models.CharField(max_length=100)
    dias_funcionamento = ArrayField(
        models.CharField(max_length=3, choices=DIAS_DA_SEMANA),
        blank=True,
        default=list
    )
    data_inicio = models.DateField(default='2024-01-26')
    data_fim = models.DateField(default='2024-12-17')
    carga_horaria_intervalo = models.TimeField(default='02:00:00')
    dias_letivos = models.IntegerField(default='80')


    def __str__(self):
        return self.nome_curso


class Aluno(models.Model):
    nome = models.CharField(max_length=150)
    id_carteirinha = models.CharField(primary_key=True)
    id_curso = models.ForeignKey(Curso, on_delete=models.CASCADE)

    def __str__(self):
        return self.nome


class Frequencia(models.Model):
    id = models.AutoField(primary_key=True)
    id_aluno = models.ForeignKey(Aluno, on_delete=models.CASCADE)
    data = models.DateField()
    hora = models.TimeField()
    identificador = models.IntegerField()

    def __str__(self):
        return f"Frequência de {self.id_aluno} em {self.data}"

class Usuario(models.Model):
    nome = models.CharField(max_length=60)
    sobrenome = models.CharField(max_length=60)
    username = models.CharField(max_length=20, primary_key=True)
    cargo = models.CharField(max_length=15, choices=TIPO_USUARIOS)

    def __str__(self):
        return self.username
```
A seguir, está uma descrição de cada model:

#### **<span style="color: #AC58FA;">1. Curso</span>**
Representa as informações sobre um curso oferecido.
- **Atributos**:
    - `turma`: Identificação única do curso (chave primária).
    - `nome_curso`: Nome do curso.
    - `horario_entrada`: Horário de início das aulas.
    - `horario_saida`: Horário de término das aulas.
    - `carga_horaria`: Carga horária total do curso.
    - `responsavel`: Nome da pessoa responsável pelo curso.
    - `dias_funcionamento`: Lista de dias da semana em que o curso ocorre, utilizando o campo `ArrayField` para armazenar múltiplos valores.
    - `data_inicio`: Data de início do curso.
    - `data_fim`: Data de término do curso.
    - `carga_horaria_intervalo`: Carga horária total do intervalo;
    - `dias_letivos`: Número total de dias letivos no curso.
- **Método**:
    - `__str__`: Retorna o nome do curso como representação textual do objeto.

#### **<span style="color: #AC58FA;">2. Aluno</span>**
Representa os alunos matriculados em um curso.
- **Atributos**:
    - `nome`: Nome do aluno.
    - `id_carteirinha`: Identificador único do aluno (chave primária).
    - `id_curso`: Chave estrangeira referenciando um curso, indicando em qual curso o aluno está matriculado.
- **Método**:
    - `__str__`: Retorna o nome do aluno como representação textual do objeto.

#### **<span style="color: #AC58FA;">3. Frequência</span>**
Registra a frequência de um aluno.
- **Atributos**:
    - `id`: Identificador único da frequência (chave primária).
    - `id_aluno`: Chave estrangeira referenciando o aluno cuja frequência está sendo registrada.
    - `data`: Data do registro de frequência.
    - `hora`: Hora do registro de frequência.
    - `identificador`: Identificador que pode ser usado para marcar diferentes estados, como entrada (1) ou saída (2).
- **Método**:
    - `__str__`: Retorna uma descrição textual contendo o nome do aluno e a data do registro de frequência.

#### **<span style="color: #AC58FA;">4. Usuário</span>**
Representa um usuário do sistema (como administradores ou coordenadores).
- **Atributos**:
    - `nome`: Primeiro nome do usuário.
    - `sobrenome`: Sobrenome do usuário.
    - `username`: Nome de usuário único (chave primária).
    - `cargo`: Tipo de usuário, com valores possíveis definidos em `TIPO_USUARIOS` (ex.: "Coordenação" ou "Administração").

- **Método**:
    - `__str__`: Retorna o nome de usuário como representação textual do objeto.

Para finalizar, criam-se as views para dar início ao desenvolvimento das páginas e lógicas.

### <span style="color: #AC58FA;">v0.4 - Desenvolvimento das Páginas</span>
Inicialmente, desenvolvemos a estrutura base das páginas, incluindo os arquivos HTML, CSS e JavaScript.

#### **<span style="color: #AC58FA;">Estruturas Base</span>**
**index.html**

```html
{% load static %}
<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="keywords"
        content="controle de frequência escolar, sistema de gestão de atrasos, monitoramento de frequência estudantil, software para controle de presença, frequência de alunos em tempo real">
    <meta name="description"
        content="Sistema de gestão de frequência estudantil com controle de atrasos e faltas. Monitore a presença dos alunos em tempo real e gerencie informações de frequência escolar de forma prática e eficiente.">

    <link rel="icon" href="{% static 'img/icon.webp' %}">
    <title>Controle de Frequência</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <link
        href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="{% static 'css/styles.css' %}">
    <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap-icons/1.10.5/font/bootstrap-icons.min.css">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght,YOPQ@100..900,40..300&display=swap"
        rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Krona+One&display=swap" rel="stylesheet">
    <link rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
    <link rel="stylesheet" href="https://viewjs.netlify.app/animation.css">

    <title>
        {% block title %}

        {% endblock %}
    </title>

    {% block head %}

    {% endblock %}
</head>

<body>
    {% include 'navbar.html' %}

    {% block body %}

    {% endblock %}

    {% include 'footer.html' %}
    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"
        integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN"
        crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.12.9/dist/umd/popper.min.js"
        integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q"
        crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM"
        crossorigin="anonymous"></script>
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    <script src="{% static 'js/mostrar_senha.js' %}"></script>
    <script src="{% static 'js/script.js' %}"></script>
    <script src="{% static 'js/search_transicao.js' %}"></script>
    <script src="{% static 'js/msg_erro.js' %}"></script>

</body>

</html>
```
O código apresentado é um template HTML Django com estrutura organizada e extensível, contendo links para arquivos estáticos, bibliotecas externas e blocos personalizáveis. A seguir, está a descrição de suas partes:

#### **<span style="color: #AC58FA;">1. Cabeçalho (`head`)</span>**
Define as configurações gerais da página e inclui links para estilos e scripts externos.

- **Meta Tags**:
    - Define o conjunto de caracteres como UTF-8.
    - Configura a responsividade da página para dispositivos móveis.
    - Contém palavras-chave e descrição da página, otimizando para SEO.
- **Favicon**:
    - Especifica um ícone da página armazenado no diretório estático (`img/icon.webp`).
- **Estilos e Fontes**:
    - Usa o framework Bootstrap (várias versões incluídas) para estilização responsiva.
    - Importa **ícones** do Bootstrap e **fontes do Google** (como `Poppins`, `Kumbh Sans`, `Krona One`).
    - Link para um arquivo CSS personalizado (`css/styles.css`) no diretório estático.
    - Inclui uma biblioteca externa para animações (`viewjs`).
- **Blocos Django**:
    - `{% block title %}`: Permite que templates filhos personalizem o título da página.
    - `{% block head %}`: Permite que templates filhos adicionem conteúdo ao `<head>`.

#### **<span style="color: #AC58FA;">2. Corpo (`body`)</span>**
A estrutura principal da página com blocos e componentes reutilizáveis.

- **Componentes Reutilizáveis**:
    - `{% include 'navbar.html' %}`: Inclui o menu de navegação armazenado em outro template.
    - `{% include 'footer.html' %}`: Inclui o rodapé armazenado em outro template.
- **Bloco Personalizável**:
    - `{% block body %}`: Permite que templates filhos definam o conteúdo principal da página.

#### **<span style="color: #AC58FA;">3. Scripts</span>**
Inclui bibliotecas JavaScript externas e arquivos personalizados.

- **Bibliotecas Externas**:
    - **jQuery**: Facilita a manipulação do DOM e eventos.
    - **Popper.js**: Necessário para elementos interativos do Bootstrap (como dropdowns).
    - **Bootstrap JS**: Suporte para interatividade em componentes do Bootstrap.
- **Scripts Estáticos**:
    - Inclui diversos arquivos JavaScript personalizados:
        - `mostrar_senha.js`: Provavelmente usado para mostrar/ocultar senha em campos de entrada.
        - `script.js`, `search_transicao.js`, `msg_erro.js`: Scripts específicos para funcionalidades personalizadas.

#### **<span style="color: #AC58FA;">4. Uso do Django</span>**
O template utiliza recursos do Django Template Language.

- `{% load static %}`: Carrega a tag `static` para referenciar arquivos estáticos.
- Blocos (`{% block ... %}`): Permitem que templates filhos estendam e personalizem o layout.
- Inclusões (`{% include ... %}`): Reutilizam partes do layout, como navbar e footer.

O código apresentado é um componente de rodapé HTML com estilização inline, utilizado para exibir uma mensagem de direitos autorais. A seguir, está sua descrição de forma detalhada:

**footer.html**

```html
<footer style="color: var(--background-color);">
    <p style="color: var(--text-color); text-align: center; height: 30px; font-size: 15px">Copyright &copy; 2024 Todos
        os direitos reservados</p>
</footer>
```
O código apresentado é um componente de **rodapé HTML** com estilização inline, utilizado para exibir uma mensagem de direitos autorais. A seguir, está sua descrição de forma detalhada:

#### **<span style="color: #AC58FA;">Estrutura e Propósito</span>**

#### **<span style="color: #AC58FA;">1. Tag `<footer>`</span>**
- Representa semanticamente o rodapé da página.
- Geralmente contém informações como créditos, direitos autorais, links de política de privacidade, entre outros.

#### **<span style="color: #AC58FA;">2. Mensagem de Direitos Autorais</span>**
- O conteúdo textual informa: 
```html
  Copyright © 2024 Todos os direitos reservados
```
- Usa o símbolo © para marcar direitos autorais, seguido do ano e da mensagem.

#### **<span style="color: #AC58FA;">Estilização Inline</span>**

#### **<span style="color: #AC58FA;">1. Estilo no `<footer>`</span>**
- A cor do texto é definida pela variável CSS `-background-color`, permitindo personalização com o uso de **CSS Custom Properties**.

#### **<span style="color: #AC58FA;">2. Estilo no `<p>`</span>**
- **Propriedade `color`**: Define a cor do texto como `var(--text-color)`, permitindo que seja dinâmica.
- **`text-align: center`**: Centraliza o texto horizontalmente dentro do rodapé.
- **`height: 30px`**: Define a altura do parágrafo.
- **`font-size: 15px`**: Define o tamanho da fonte.

**navbar.html**

```html
{% load static %}

<style>
    .navbar {
        background-color: var(--navbar-bg-color);
        width: 100%;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 1000;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
    }

    .navbar-toggler {
        border: none;
        outline: none;
    }

    #theme-icon {
        color: white;
        transition: transform 0.7s ease, opacity 0.3s ease;
    }

    #theme-icon.changing {
        transform: rotate(180deg) scale(0);
        opacity: 0;
    }

    .navbar-toggler:focus,
    .navbar-toggler:hover {
        border: none;
        outline: none;
        box-shadow: none;
    }

    .navbar img.logo_senai {
        width: 42%;
        max-width: 100%;
        height: auto;
    }

    .navbar-nav .nav-link {
        color: #fff;
        transition: color 0.3s ease-in-out, transform 0.3s ease-in-out;
        padding: 0 15px;
    }

    .navbar-nav .nav-link:hover {
        color: #c70b0b;
        transform: scale(1.1);
    }

    .IconButton-homepage,
    .navbar-toggler {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        background-color: transparent;
        border: none;
        cursor: pointer;
        margin: 0 5px;
    }

    .material-symbols-outlined {
        font-size: 24px;
        color: #ffffff;
    }

    .btn-close {
        align-items: end;
        right: 0;
        background-color: transparent;
        border: none;
        cursor: pointer;
    }

    @media (max-width: 1200px) {
        .navbar-nav .nav-link {
            font-size: 14px;
        }
    }

    @media (max-width: 992px) {
        .navbar-nav .nav-link {
            font-size: 12px;
        }

        .navbar-nav .nav-link:hover {
            color: #fff;
            transform: scale(1);
        }
    }

    @media (max-width: 768px) {
        .logo {
            max-width: 400px;
        }
    }

    @media (max-width: 576px) {
        .logo {
            max-width: 330px;
        }
    }
</style>

<nav class="navbar">
    <div class="container-fluid">
        <a class="navbar-brand" href="" style="max-width: 40%;">
            <img class="logo_senai" src="{% static 'img/senai_logo.webp' %}" alt="Logo">
        </a>

        <div class="d-flex align-items-center">
            {% if user.is_authenticated %}
            <span class="navbar-text" style="color: #FFFAFB;">Olá, {{ user.username }}</span>
            {% endif %}
            <a id="theme-toggle" class="IconButton-homepage" aria-label="Alternar tema">
                <i id="theme-icon" class=""></i>
            </a>
            {% if user.is_authenticated %}
            <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar"
                aria-controls="offcanvasNavbar" aria-label="Toggle navigation menu"
                style="border: none; outline: none;">
                <i class="bi bi-list" style="color: #FFFAFB; font-size: 30px;"></i>
            </button>
            {% endif %}
        </div>

        <!-- Offcanvas Navbar -->
        <div class="container-fluid">
            <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar"
                style="background: var(--background); padding: 20px;" aria-labelledby="offcanvasNavbarLabel">

                <div class="offcanvas-header">
                    <div class="icon-container"
                        style="display: flex; justify-content: space-between; width: 300%; border-bottom: 1px solid rgb(228, 228, 228);">
                        <!-- Título e ícone à esquerda -->

                        {% if user.is_authenticated %}
                        <span class="navbar-text" style="color: #FFFAFB;">Olá, {{ user.username }}</span>
                        {% endif %}
                        <!-- Botão close à direita -->
                        <div data-bs-theme="dark">
                            <button type="button" class="btn-close" data-bs-dismiss="offcanvas"
                                aria-label="Fechar menu"></button>
                        </div>
                    </div>
                </div>

                <div class="offcanvas-body">
                    <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
                        <ul class="navbar-nav">
                            {% if user.is_superuser %}
                            <li class="nav-item">
                                <a class="nav-link" href="{% url 'cadastro' %}">
                                    <i class="bi bi-person-plus" style="font-size: 20px;"></i> Cadastro
                                </a>
                            </li>
                            {% endif %}
                            <li class="nav-item">
                                {% if user.is_authenticated %}
                            <li class="nav-item">
                                <a class="nav-link" href="{% url 'criar_aluno' %}">
                                    <i class="bi bi-file-earmark-plus" style="font-size: 20px;"></i> Aluno
                                </a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="{% url 'criar_curso' %}">
                                    <i class="bi bi-file-earmark-plus" style="font-size: 20px;"></i> Curso
                                </a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="{% url 'freq' %}">
                                    <i class="bi bi-file-earmark-plus" style="font-size: 20px;"></i> Frequência
                                </a>
                            </li>
                            <a class="nav-link" href="{% url 'logout' %}">
                                <i class="bi bi-box-arrow-right" style="font-size: 20px; margin: 2px;"></i> Sair
                            </a>
                            {% endif %}
                            </li>
                        </ul>
                    </ul>
                </div>

            </div>
        </div>
    </div>
</nav>
```
O código apresentado é uma **barra de navegação (`navbar`) dinâmica** implementada com **HTML**, **CSS**, **Django Template Language** e **JavaScript**. Ele inclui uma estrutura responsiva e funcionalidades avançadas, como alternância de tema e um menu lateral deslizante (offcanvas).

#### **<span style="color: #AC58FA;">Descrição por Seções</span>**

#### **<span style="color: #AC58FA;">1. CSS Inline (Estilo da Navbar)</span>**
Define a aparência e o comportamento da barra de navegação:

- **Estilo Geral**:
    - `background-color`: Usa a variável CSS `-navbar-bg-color`, permitindo personalização de temas.
    - `position: fixed`: Mantém a navbar fixa no topo da página.
    - `z-index: 1000`: Garante que a navbar fique acima de outros elementos.
- **Animações**:
    - O ícone de alternância de tema (`#theme-icon`) possui transições suaves para rotação e opacidade.
- **Responsividade**:
    - Utiliza **media queries** para ajustar o tamanho das fontes e elementos em diferentes larguras de tela.

#### **<span style="color: #AC58FA;">2. Navbar Principal</span>**
- Inclui a marca (logo), saudação ao usuário, botão de alternância de tema e botão para abrir o menu lateral (offcanvas).
- Exibe diferentes elementos dependendo do estado de autenticação do usuário:
    - **Usuário autenticado**:
        - Mostra o nome do usuário (`Olá, {{ user.username }}`).
        - Exibe o botão do menu lateral e permite logout.
    - **Usuário não autenticado**:
        - Oculta opções específicas de usuário.

#### **<span style="color: #AC58FA;">3. Offcanvas Navbar (Menu Lateral)</span>**
- **Estrutura**:
    - Exibido à direita da tela (`offcanvas-end`) com fundo dinâmico usando `var(--background)`.
    - Cabeçalho inclui a saudação ao usuário e um botão para fechar o menu.
    - Corpo exibe links de navegação, condicionais ao estado do usuário:
        - **Administrador (`is_superuser`)**:
            - Link para "Cadastro".
        - **Usuário autenticado**:
            - Links para criar aluno, curso e frequência.
            - Link para logout.
    - Ícones do Bootstrap adicionam representações visuais aos links.

#### **<span style="color: #AC58FA;">5. Recursos Django</span>**
- **Carregamento de Arquivos Estáticos**:
    - O logo (`img/senai_logo.webp`) é carregado com a tag `{% static %}`.
- **Links de URL**:
    - Usam `{% url 'nome_da_view' %}` para gerar URLs dinamicamente.
- **Blocos Condicionais**:
    - Verifica o estado de autenticação (`user.is_authenticated`) e privilégios (`user.is_superuser`) para exibir ou ocultar elementos.

#### **<span style="color: #AC58FA;">6. Melhores Práticas Implementadas</span>**
- **Responsividade**:
    - Adapta o layout para dispositivos menores.
- **Modularidade**:
    - Usa variáveis CSS e condicionalidade Django para facilitar manutenção e personalização.
- **Experiência do Usuário**:
    - Ícones e transições suaves melhoram a interação.


### <span style="color: #AC58FA;">Importações e arquivos CSS globais</span>
**Style.css**

```css
    @import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

    @import url(homepage.css);
    @import url(theme.css);
    @import url(global.css);
```
O código contém instruções para **importação de fontes e arquivos CSS**. A seguir,i está uma explicação detalhada sobre cada parte do código:

#### **<span style="color: #AC58FA;">1. Importação de Fontes do Google Fonts</span>**
```css
@import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
```

- **Função: Esse comando importa duas famílias de fontes do Google Fonts**:
    - Kumbh Sans: Uma fonte sans-serif com pesos de 100 a 900, permitindo uma ampla variação na espessura da fonte.
    - Poppins: Outra fonte sans-serif com variação de pesos e itálico, abrangendo uma faixa de 100 a 900 para pesos e 0, 100, 200, etc., para itálico.
- **Objetivo: Ao importar essas fontes, elas ficam disponíveis para uso em seu CSS, permitindo a utilização dessas fontes nas propriedades font-family em qualquer parte da página**.

#### **<span style="color: #AC58FA;">2. Importação de Arquivos CSS Locais</span>**

```css
@import url(homepage.css);    
@import url(theme.css);
@import url(global.css);
```
- **Função: Este trecho importa três arquivos CSS locais para o seu documento**:
    - homepage.css: Provavelmente contém estilos específicos para a página inicial do site.
    - theme.css: Geralmente, define as cores, fontes e variações do tema (como claro/escuro).
    - global.css: Arquivo com estilos globais aplicados a todas as páginas do site.
- **Objetivo: Ao importar esses arquivos CSS, as regras de estilo contidas neles serão aplicadas ao site**.

**Global.css**

```css
* {
    text-decoration: none;
    font-family: "Kumbh Sans";
}

.downUp-1 {
    animation: downUp 1s forwards;
}

.titulo {
    font-family: "Krona One";
    font-weight: 400;
    font-style: normal;
}

body {
    padding-top: 60px;
}
```
O código CSS aplica estilos gerais e específicos em elementos HTML.

#### **<span style="color: #AC58FA;">1. Estilo Global para Todos os Elementos</span>**

```css
* {
    text-decoration: none;
    font-family: "Kumbh Sans";
}
```
- **`` ``**: O seletor universal (`` ``) é utilizado para aplicar estilos a **todos os elementos** na página.
- **`text-decoration: none;`**: Remove qualquer decoração de texto, como sublinhado, de todos os elementos (por exemplo, links).
- **`font-family: "Kumbh Sans";`**: Define a fonte **"Kumbh Sans"** para todos os elementos, garantindo uma tipografia consistente. Se a fonte não estiver disponível, o navegador usará a fonte padrão.

#### **<span style="color: #AC58FA;">2. Classe `.downUp-1`</span>**
```css
.downUp-1 {
    animation: downUp 1s forwards;
}
```
- **`animation: downUp 1s forwards;`**: Aplica uma animação chamada **`downUp`** a elementos com a classe `.downUp-1`.
    - **`1s`**: Define a duração da animação como **1 segundo**.
    - **`forwards`**: Mantém o estado final da animação após sua conclusão (evita que o elemento volte ao seu estado original).

#### **<span style="color: #AC58FA;">3. Classe `.titulo`</span>**
```css
.titulo {
    font-family: "Krona One";
    font-weight: 400;
    font-style: normal;
}
```
- **`font-family: "Krona One";`**: Aplica a fonte **"Krona One"** aos elementos com a classe `.titulo`. Essa fonte é uma tipografia específica que será usada para títulos ou textos destacados.
- **`font-weight: 400;`**: Define o peso da fonte como **normal** (peso 400 é o valor padrão).
- **`font-style: normal;`**: Define o estilo da fonte como **normal**, o que significa que não será itálico ou oblíquo.

#### **<span style="color: #AC58FA;">4. Estilo do `body`</span>**
```css
body {
    padding-top: 60px;
}
```
- **`padding-top: 60px;`**: Adiciona um **preenchimento de 60 pixels** na parte superior do corpo da página. Isso é útil para evitar que o conteúdo do site fique muito próximo de elementos fixos no topo da página, como uma barra de navegação fixa.

### <span style="color: #AC58FA;">Temas claro e escuro</span>
Para a estilização dos temas claro e escuro, foram utilizadas as seguintes ferramentas:
- **<span style="color: #4682B4;">JavaScript</span>**;
- **<span style="color: #4682B4;">HTML</span>**;
- **<span style="color: #4682B4;">CSS</span>**;

**Themes.css**

```css
/* Definição das cores */
:root {
    --text-color: #FFFAFB;
    --title-color: #FFFAFB;
    --background-color: #260104;
    --button-gradient-start: #DF79A9;
    --button-gradient-middle: #CC5854;
    --button-gradient-end: #40010D;
    --navbar-bg-color: #260104;
    --list-bg-color: radial-gradient(circle at 20% 30%, #6A2D3F, #450D0F 50%, #390C0E 80%);
    --button-bg-color: #8C031C;
    --table-bg-color: rgba(79, 1, 13, 0.2);
    --background: radial-gradient(circle at 20% 30%, #6A2D3F, #450D0F 50%, #390C0E 80%);
    --input-bg: radial-gradient(circle at 20% 30%, #6A2D3F, #450D0F 50%, #390C0E 80%);
    --button-home: #FFFAFB;
}

[data-theme="light"] {
    --text-color: #260104;
    --title-color: #260104;
    --background-color: #FFFAFB;
    --button-gradient-start: #FFFAFB;
    --button-gradient-middle: #FFFAFB;
    --button-gradient-end: #FFFAFB;
    --navbar-bg-color: #7C0D1D;
    --list-bg-color: #FFECF0;
    --button-bg-color: #FFFAFB;
    --table-bg-color: rgba(255, 236, 240, 0.7);
    --background: #7C0D1D;
    --input-bg: radial-gradient(circle at 20% 30%, #821B2A, #872634 50%, #892D3A 80%);
    --button-home: #7C0D1D;
}

body {
    color: var(--text-color);
    background-color: var(--background-color);
    line-height: 1.7;
    transition: background-color 0.5s ease, color 0.5s ease;
}

.navbar {
    background-color: var(--navbar-bg-color);
    transition: background-color 0.5s ease, color 0.5s ease;
}

.bg_Home {
    background-color: var(--background-color);
    transition: background-color 0.5s ease, color 0.5s ease;
}

.btn-custom {
    background: linear-gradient(145deg, var(--button-gradient-start), var(--button-gradient-middle) 20%, var(--button-gradient-end));
    color: var(--text-color);
    transition: background 0.5s ease, color 0.5s ease;
}

.button {
    width: 200px;
    padding: 5px;
    height: 40px;
    border: none;
    border-radius: 10px;
    font-family: inherit;
    cursor: pointer;
    background-color: var(--button-bg-color);
    color: var(--text-color);
    font-size: 16px;
    font-weight: 400;
    text-transform: capitalize;
    transition: background-color 0.5s ease, color 0.5s ease;
}
```
**Scripts.js**
```jsx
document.addEventListener("DOMContentLoaded", function () {
    const themeToggleBtn = document.getElementById("theme-toggle");
    const themeIcon = document.getElementById("theme-icon");
    let currentTheme = localStorage.getItem("theme") || "light";

    document.documentElement.setAttribute("data-theme", currentTheme);
    themeIcon.classList.remove("bi-sun-fill", "bi-moon-fill");
    themeIcon.classList.add(currentTheme === "light" ? "bi-sun-fill" : "bi-moon-fill");

    themeToggleBtn.addEventListener("click", function () {
        currentTheme = currentTheme === "light" ? "dark" : "light";

      
        document.documentElement.setAttribute("data-theme", currentTheme);

        localStorage.setItem("theme", currentTheme);

        themeIcon.classList.remove("bi-sun-fill", "bi-moon-fill");
        themeIcon.classList.add(currentTheme === "light" ? "bi-sun-fill" : "bi-moon-fill");
    });
});
```
A lógica do código apresentado permite alternar entre **temas claro e escuro** em uma página web. Vamos entender seu funcionamento detalhadamente:

#### **<span style="color: #AC58FA;">1. Espera pelo Carregamento Completo do Documento</span>**
```jsx
document.addEventListener("DOMContentLoaded", function () {
```
- Este evento **escuta** o carregamento completo do **DOM** (Document Object Model), ou seja, a estrutura HTML da página.
- Quando o DOM estiver totalmente carregado, a função de callback será executada.

#### **<span style="color: #AC58FA;">2. Inicialização das Variáveis</span>**
```jsx
const themeToggleBtn = document.getElementById("theme-toggle");
const themeIcon = document.getElementById("theme-icon");
let currentTheme = localStorage.getItem("theme") || "light";
```
- `themeToggleBtn`: Acessa o botão que será clicado para alternar o tema (identificado pelo ID `theme-toggle`).
- `themeIcon`: Acessa o ícone do tema (identificado pelo ID `theme-icon`), que representará visualmente o tema atual (ícone de sol ou lua).
- `currentTheme`: Verifica se há um tema armazenado no `localStorage` (usando a chave `"theme"`). Se não houver, o tema padrão será `"light"` (claro).

#### **<span style="color: #AC58FA;">3. Configuração Inicial do Tema</span>**
```jsx
document.documentElement.setAttribute("data-theme", currentTheme);
themeIcon.classList.remove("bi-sun-fill", "bi-moon-fill");
themeIcon.classList.add(currentTheme === "light" ? "bi-sun-fill" : "bi-moon-fill");
```
- **Define o Tema Inicial**:
    - O atributo `data-theme` do elemento `<html>` é configurado com o valor de `currentTheme` (`light` ou `dark`). Este atributo pode ser usado no CSS para alterar o estilo da página (por exemplo, mudando cores de fundo, texto, etc.).
- **Configura o Ícone Inicial**:
    - As classes `bi-sun-fill` (ícone de sol) e `bi-moon-fill` (ícone de lua) são **removidas** para garantir que não haja classes anteriores conflitantes.
    - Em seguida, a classe do ícone é **adicionada** com base no tema atual:
        - Se o `currentTheme` for `"light"`, a classe `bi-sun-fill` é adicionada.
        - Se for `"dark"`, a classe `bi-moon-fill` é adicionada.

#### **<span style="color: #AC58FA;">4. Alternância de Tema</span>**
```jsx
themeToggleBtn.addEventListener("click", function () {
    currentTheme = currentTheme === "light" ? "dark" : "light";
```
- Adiciona um **listener de evento** para o **botão de alternância de tema** (`themeToggleBtn`).
- Ao clicar no botão, o valor de `currentTheme` alterna entre `"light"` e `"dark"` usando o operador ternário:
    - Se o tema atual for `"light"`, ele se torna `"dark"`.
    - Se o tema atual for `"dark"`, ele se torna `"light"`.

#### **<span style="color: #AC58FA;">5. Atualizando o Tema e Ícone</span>**
```jsx
document.documentElement.setAttribute("data-theme", currentTheme);

localStorage.setItem("theme", currentTheme);

themeIcon.classList.remove("bi-sun-fill", "bi-moon-fill");
themeIcon.classList.add(currentTheme === "light" ? "bi-sun-fill" : "bi-moon-fill");
```
- **Atualizando o Atributo `data-theme`**:
    - O atributo `data-theme` do `<html>` é atualizado para refletir o novo tema, aplicando as mudanças no layout através do CSS.
- **Armazenando o Novo Tema no `localStorage`**:
    - O tema atual é salvo no `localStorage` com a chave `"theme"`. Isso garante que a escolha do tema seja persistente mesmo quando o usuário recarregar a página ou voltar à página depois de algum tempo.
- **Atualizando o Ícone**:
    - As classes `bi-sun-fill` e `bi-moon-fill` são **removidas** novamente.
    - A classe correspondente ao novo tema é **adicionada**:
        - Se o tema for `"light"`, o ícone de sol (`bi-sun-fill`) é exibido.
        - Se o tema for `"dark"`, o ícone de lua (`bi-moon-fill`) é exibido.

### <span style="color: #AC58FA;">Página Inicial</span>

**Homepage.html**
```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Homepage
{% endblock %}

{% block head %}
{% endblock %}

{% block body %}
<div class="bg_Home animate downUp-1">
    <div class="main">
        <h2 class="titulo">Gestão de Atrasos</h2>
        <a href="{% url 'login' %}"
            style="display: inline-block; background-color: var(--button-home); color: var(--background-color); text-decoration: none; font-weight: 500; padding: 15px 25px; border-radius: 50px; text-align: center;"
            aria-label="Entrar na conta" accesskey="l">
            Login
        </a>
    </div>
    <div class="imag">
        <img src="{% static 'img/img_home.webp' %}" alt="Imagem de fundo" width="400" height="300">
    </div>
</div>
{% endblock %}
```
O código apresentado é um **template do Django** que extende um arquivo `index.html` e utiliza blocos para personalizar o conteúdo da página. Ele é utilizado para renderizar a página inicial (homepage) do sistema. Vamos analisar o código detalhadamente:

#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
```html
{% extends 'index.html' %}
```
- O template **herda** o conteúdo de `index.html`, o que significa que ele usará a estrutura básica (cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.

#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}

```
- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.


#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```
{% block title %}
Homepage
{% endblock %}

```
- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.


#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```
{% block head %}
{% endblock %}

```
- O bloco `head` está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag `<head>` do HTML (como links de CSS ou meta tags). Se você precisar adicionar algo específico a esse bloco, pode sobrescrevê-lo neste template ou em templates filhos.


#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```
{% block body %}
<div class="bg_Home animate downUp-1">
    <div class="main">
        <h2 class="titulo">Gestão de Atrasos</h2>
        <a href="{% url 'login' %}"
            style="display: inline-block; background-color: var(--button-home); color: var(--background-color); text-decoration: none; font-weight: 500; padding: 15px 25px; border-radius: 50px; text-align: center;"
            aria-label="Entrar na conta" accesskey="l">
            Login
        </a>
    </div>
    <div class="imag">
        <img src="{% static 'img/img_home.webp' %}" alt="Imagem de fundo" width="400" height="300">
    </div>
</div>
{% endblock %}

```
- **Estrutura do `body`**:
    - Este é o conteúdo principal da página, onde a seção do corpo é definida.
    - **Classe `bg_Home` e Animação**:
        - O `<div>` com a classe `bg_Home` serve como um **container** para o conteúdo da página.
        - A classe `animate downUp-1` indica que o conteúdo tem uma animação associada (provavelmente definida no CSS), fazendo com que ele tenha um efeito visual de **deslocamento** ao ser carregado.
    - **Seção Principal (`main`)**:
        - O título da página, **"Gestão de Atrasos"**, é exibido dentro de um `<h2>` com a classe `.titulo`. A fonte utilizada para o título pode ser a `Krona One`, conforme o CSS fornecido anteriormente.
        - O **link "Login"**:
            - Este é um botão de login estilizado com uma cor de fundo definida pela variável `var(--button-home)` e a cor do texto usando `var(--background-color)`.
            - O link aponta para a URL associada ao nome de view `'login'` no Django, gerado dinamicamente com `{% url 'login' %}`.
            - **Atributos**:
                - `aria-label="Entrar na conta"`: Melhora a acessibilidade, descrevendo a ação do botão.
                - `accesskey="l"`: Define uma tecla de atalho para acessar o link (neste caso, "L").
    - **Imagem de Fundo**:
        - Dentro de `<div class="imag">`, uma imagem de fundo é carregada com a tag `<img>`, utilizando o arquivo de imagem estática `img_home.webp` (com o caminho definido pelo `{% static 'img/img_home.webp' %}`).
        - A imagem tem largura de **400px** e altura de **300px**.

**Homepage.css**
```css
.bg_Home {

    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center center;
    background-size: cover;
    height: 100vh;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    align-items: center;
    color: var(--text-color);
    padding: 0 10%;
}

button {
    border: none;
    padding: 10px 20px;
    border-radius: 20px;
    margin-top: 20px;
}

button:hover {
    color: #000;
}

.main {
    text-align: center;
    width: 100%;
    max-width: 450px;
    margin-bottom: 20px;
    align-content: center;
}

.imag {
    width: 100%;
    max-width: 400px;
    padding: 10px;
}

.imag img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.titulo {
    color: var(--title-color);
    font-size: 2.5rem;
    font-weight: 400;
    margin-bottom: 20px;
}

@media (min-width: 768px) {
    .bg_Home {
        justify-content: space-between;
    }

    .main {
        text-align: left;
    }

    .titulo {
        font-size: 3rem;
    }
}

@media (min-width: 1024px) {
    .titulo {
        font-size: 4rem;
    }
}

.IconButton-homepage {
    text-decoration: none;
    color: var(--text-color);
    transition: color 0.3s ease, transform 0.3s ease;
    cursor: pointer;
    margin-right: 30px;
}

.IconButton-homepage:hover {
    color: #781010;
    cursor: pointer;
    transform: scale(1.1);
}
```
O código CSS apresentado aplica estilos a diversos elementos de uma página inicial, como a **fundo**, **botões**, **imagens** e **títulos**, com foco na **responsividade** e animações suaves. A seguir, está uma explicação detalhada de cada parte:

#### **<span style="color: #AC58FA;">1. Estilo para o Fundo da Página (.bg_Home)</span>**
```css
.bg_Home {
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center center;
    background-size: cover;
    height: 100vh;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    align-items: center;
    color: var(--text-color);
    padding: 0 10%;
}

```
- **Propriedades de Fundo**:
    - `background-repeat: no-repeat`: Impede que a imagem de fundo se repita.
    - `background-attachment: fixed`: Faz com que a imagem de fundo permaneça fixa enquanto o conteúdo da página rola.
    - `background-position: center center`: Posiciona a imagem de fundo no centro da tela.
    - `background-size: cover`: Faz a imagem de fundo cobrir toda a área da tela, mantendo as proporções.
- **Layout**:
    - `height: 100vh`: Define a altura da seção como 100% da altura da janela de visualização (viewport).
    - `display: flex`: Utiliza o modelo de layout flexbox para distribuir os itens dentro do `.bg_Home`.
    - `justify-content: space-around`: Distribui os itens de forma equilibrada, com espaçamento igual entre eles.
    - `flex-wrap: wrap`: Permite que os itens se ajustem à linha seguinte quando necessário.
    - `align-items: center`: Alinha verticalmente os itens ao centro da tela.
- **Texto e Padding**:
    - `color: var(--text-color)`: Define a cor do texto com base na variável `-text-color`, que provavelmente é definida no CSS.
    - `padding: 0 10%`: Adiciona um espaçamento de 10% nas laterais do contêiner.

#### **<span style="color: #AC58FA;">2. Estilo para Botões</span>**
```css
button {
    border: none;
    padding: 10px 20px;
    border-radius: 20px;
    margin-top: 20px;
}

button:hover {
    color: #000;
}

```
- **Botão**:
    - `border: none`: Remove a borda padrão do botão.
    - `padding: 10px 20px`: Define o preenchimento interno do botão, criando um espaçamento agradável em torno do texto.
    - `border-radius: 20px`: Adiciona bordas arredondadas ao botão.
    - `margin-top: 20px`: Adiciona um espaçamento de 20px no topo do botão.
- **Efeito Hover**:
    - `button:hover`: Ao passar o mouse sobre o botão, a cor do texto será alterada para **preto** (`#000`).

#### **<span style="color: #AC58FA;">3. Estilo para a Seção Principal (.main)</span>**
```css
.main {
    text-align: center;
    width: 100%;
    max-width: 450px;
    margin-bottom: 20px;
    align-content: center;
}

```
- **Centralização e Layout**:
    - `text-align: center`: Centraliza o texto dentro do elemento.
    - `width: 100%`: Define a largura como 100% da área disponível.
    - `max-width: 450px`: Limita a largura máxima do elemento a 450px.
    - `margin-bottom: 20px`: Adiciona um espaçamento de 20px abaixo do elemento.
    - `align-content: center`: Centraliza o conteúdo dentro de um contêiner de múltiplas linhas (quando necessário).

#### **<span style="color: #AC58FA;">4. Estilo para as Imagens (.imag)</span>**
```css
.imag {
    width: 100%;
    max-width: 400px;
    padding: 10px;
}

.imag img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

```
- **Contêiner da Imagem**:
    - `width: 100%`: Define a largura do contêiner da imagem como 100% do espaço disponível.
    - `max-width: 400px`: Limita a largura máxima do contêiner a 400px.
    - `padding: 10px`: Adiciona um preenchimento de 10px em torno da imagem.
- **Imagem**:
    - `width: 100%`: Faz com que a imagem ocupe 100% da largura do seu contêiner.
    - `height: auto`: Mantém a proporção original da imagem ao ajustar sua altura automaticamente.
    - `border-radius: 10px`: Adiciona bordas arredondadas à imagem.

#### **<span style="color: #AC58FA;">5. Estilo para o Título (.titulo)</span>**
```css
.titulo {
    color: var(--title-color);
    font-size: 2.5rem;
    font-weight: 400;
    margin-bottom: 20px;
}

```
- **Título**:
    - `color: var(--title-color)`: Define a cor do título com base na variável `-title-color`, que pode ser configurada no CSS.
    - `font-size: 2.5rem`: Define o tamanho da fonte como **2.5rem**, o que é um tamanho grande e adequado para um título.
    - `font-weight: 400`: Define o peso da fonte como **normal**.
    - `margin-bottom: 20px`: Adiciona um espaçamento de 20px abaixo do título.

#### **<span style="color: #AC58FA;">6. Media Queries para Responsividade</span>**
**Para telas de largura mínima de 768px (tablets e dispositivos maiores)**

```css
@media (min-width: 768px) {
    .bg_Home {
        justify-content: space-between;
    }

    .main {
        text-align: left;
    }

    .titulo {
        font-size: 3rem;
    }
}
```
- **Modificação de Layout**:
    - **`justify-content: space-between`**: Modifica a distribuição do conteúdo para ficar com o máximo de espaço entre os itens.
    - **`text-align: left`**: Alinha o texto da seção principal à esquerda.
    - **`font-size: 3rem`**: Aumenta o tamanho do título para **3rem**.

**Para telas de largura mínima de 1024px (desktops)**

```css
@media (min-width: 1024px) {
    .titulo {
        font-size: 4rem;
    }
}
```
- **Modificação para Desktop**:
    - **`font-size: 4rem`**: Aumenta o tamanho do título para **4rem** em telas grandes (desktops).

#### **<span style="color: #AC58FA;">7. Estilo para Botões de Ícone (.IconButton-homepage)</span>**
```css
css
Copiar código
.IconButton-homepage {
    text-decoration: none;
    color: var(--text-color);
    transition: color 0.3s ease, transform 0.3s ease;
    cursor: pointer;
    margin-right: 30px;
}

.IconButton-homepage:hover {
    color: #781010;
    cursor: pointer;
    transform: scale(1.1);
}

```
- **Botão de Ícone**:
    - `text-decoration: none`: Remove qualquer sublinhado de texto, se presente.
    - `color: var(--text-color)`: Define a cor do ícone com base na variável `-text-color`.
    - **Transições**: As propriedades de cor e transformação (como escala) têm uma transição suave de **0.3 segundos**.
    - **`cursor: pointer`**: Define o cursor como **ponteiro** quando o mouse passa sobre o ícone.
    - `margin-right: 30px`: Adiciona um espaçamento de 30px à direita do ícone.
- **Efeito Hover**:
    - `color: #781010`: Altera a cor para um tom mais escuro de vermelho ao passar o mouse sobre o ícone.
    - **`transform: scale(1.1)`**: Aumenta ligeiramente o tamanho do ícone quando o mouse passa sobre ele.

### <span style="color: #AC58FA;">Página de Login</span>
**Login.html**
```html 
{% extends 'index.html' %}
{% load static %}

{% block title %}
Login
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/login.css' %}">
{% endblock %}

{% block body %}
<div class="bg_Login animate downUp-1">
    <div class="main">
        <form action="{% url 'login' %}" method="post">
            {% csrf_token %}
            <div class="mb-3">
                <h2 class="titulo">Fazer Login</h2>
                <label for="username" class="form-label">Nome de Usuário</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.username }}
                </div>
            </div>
            <!-- INPUT DA SENHA -->
            <div class="mb-3">
                <label for="senha" class="form-label">Senha</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-key icone"></i>
                    </span>
                    {{ form.senha }}
                    <i class="bi bi-eye-slash esconder_senha" onclick="mostrar()" id="btnSenha"></i>
                </div>
            </div>
            {% if messages %}
            <div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
                {% for mensagem in messages %}
                {{ mensagem }}
                {% endfor %}
            </div>
            {% endif %}
            <button class="button" style="color: #40010D" type="submit">Entrar</button>
        </form>
    </div>
    <div class="imag">
        <img src="{% static 'img/img_login.webp' %}" alt="Imagem">
    </div>
</div>
{% endblock %}
```
Detalhes do código:
#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
```html
{% extends 'index.html' %}
```
- O template **herda** o conteúdo de `index.html`, o que significa que ele usará a estrutura básica (cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.

#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}
```
- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.

#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```html
{% block title %}
Login
{% endblock %}
```
- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.

#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```html
{% block head %}
{% endblock %}
```
- O bloco **`*head*`** está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag **`*<head>*`** do HTML (como links de CSS ou meta tags). É necessário caso precise adicionar algo específico a esse bloco, podenso sobrescrevê-lo neste template ou em templates filhos.

#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```html
{% block body %}
<div class="bg_Login animate downUp-1">
    <div class="main">
        <form action="{% url 'login' %}" method="post">
            {% csrf_token %}
            <div class="mb-3">
                <h2 class="titulo">Fazer Login</h2>
                <label for="username" class="form-label">Nome de Usuário</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.username }}
                </div>
            </div>
            <!-- INPUT DA SENHA -->
            <div class="mb-3">
                <label for="senha" class="form-label">Senha</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-key icone"></i>
                    </span>
                    {{ form.senha }}
                    <i class="bi bi-eye-slash esconder_senha" onclick="mostrar()" id="btnSenha"></i>
                </div>
            </div>
            {% if messages %}
            <div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
                {% for mensagem in messages %}
                {{ mensagem }}
                {% endfor %}
            </div>
            {% endif %}
            <button class="button" style="color: #40010D" type="submit">Entrar</button>
        </form>
    </div>
    <div class="imag">
        <img src="{% static 'img/img_login.webp' %}" alt="Imagem">
    </div>
</div>
{% endblock %}
```

- **Estrutura do `*body*`**:

Este é o conteúdo principal de uma página, onde a seção do corpo é definida. Contém o corpo de um documento ***HTML***, que é exibido pelo navegador em sua janela, ou seja, todo o conteúdo visível do site

- **Classe `*bg_Login*` e Animação**:
    - A **`*<div>*`** com a classe **`*bg_Login*`** serve como um **container** para o conteúdo da página.
    - A classe **`*animate downUp-1*`** indica que o conteúdo tem uma animação associada (definida no CSS), fazendo com que ele tenha um efeito visual de **deslocamento** ao ser carregado.
- **Seção Principal (`*main*`)**:
    - **Formulário de Login:**
        - O link aponta para a URL associada ao nome de View **`*login`*** no Django, gerado dinamicamente com **`*{% url 'login' %}*`**.
        - O título da página, **"Fazer Login"**, é exibido dentro de um **`*<h2>*`** com a classe **`*.titulo*`**.
        - A **`*label`*** nome de usuário é onde será inserido o **`*username`*** do usuário. A classe utilizada para a estilização da cor do texto da **`*label`*** é a **`*form-label*`** , ademais, por meio de um componente **`*span*`** exibe um ícone referente aos dados que serão inseridos.
        - A **`*label`*** senha é onde será inserido a **`*senha*`** do usuário. A classe utilizada para a estilização da cor do texto da **`*label*`** é a **`*form-label*`** , ademais, por meio de um componente **`*span*`** exibe um ícone referente aos dados que serão inseridos.
        - No campo de inserção da senha, é possível alterar a exibição da senha, escondendo ou exibindo-a por meio do icone **`*bi bi-eye-slash*`** que é ativada com o evento **`*onclick="mostrar()"*`** .
        
    - **Mensagem de Erro:**
        ```html
        {% if messages %}
        	<div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
        	    {% for mensagem in messages %}
        	    {{ mensagem }}
        	    {% endfor %}
        	</div>
        {% endif %}
        ```
        Caso algum dos dados inseridos pelo usuário esteja incorreto, ou seja, não está registrado nas informações do banco de dados, onde se encontram as informações dos usuários, será exibido uma  **`*<div>*`** alertando que alguma das informações estão incorretas.
        
- **Imagem de Fundo**:
    - Dentro de **`*<div class="imag">*`**, uma imagem de fundo é carregada com a tag **`*<img>*`**, utilizando o arquivo de imagem estática **`*img_login.webp*`** (com o caminho definido pelo **`*{% static 'img/img_login.webp' %}*`**).
    - A imagem tem largura de **400px** e altura de **300px**.

**login.css**

```css
* {
    font-family: "Kumbh Sans";
}

.bg_Login {
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center center;
    background-size: cover;
    height: 100vh;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    align-items: center;
    background-color: var(--background-color);
    padding: 0 10%;
}

.button {
    color: #40010D;
    background-color: #FFFAFB;
    border: none;
    padding: 10px 20px;
    border-radius: 10px;
    margin-top: 20px;
    max-width: 320px;
    width: 100%;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 500;
}

.button:hover {
    background-color: #f2f2f2;
    color: #40010D;
}

.main {
    padding: 40px;
    background: var(--background);
    border-radius: 20px;
    text-align: center;
    width: 100%;
    max-width: 400px;
    align-content: center;
}

.imag {
    width: 100%;
    max-width: 500px;
    padding: 10px;
}

.imag img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.titulo {
    color: #FFFAFB;
    font-size: 2.5rem;
    font-weight: 400;
    margin-bottom: 20px;
}

.form {
    border: none;
    background: var(--input-bg);
    color: #FFFAFB;
}

.form::placeholder {
    color: #FFFAFB;
    font-size: 13px;
}

.form:focus {
    border: none;
    background: var(--input-bg);
    color: #FFFAFB;
}

.form-label {
    color: #FFFAFB;
}

.icone {
    color: #FFFAFB;
}

.input-group {
    border: none;
    overflow: hidden;
    border-radius: 5px;
    background: var(--input-bg);
    padding: 1px;
}

.input-group .form-control {
    border: none;
    border-radius: 0;
}

.input-group-text {
    background-color: var(--input-bg);
    border: none;
    color: #FFFAFB;
}

.esconder_senha {
    color: #FFFAFB;
    cursor: pointer;
    position: absolute;
    right: 5%;
    top: 20%;
}

.fade-out {
    opacity: 1;
    transition: opacity 0.5s ease-out;
}

.fade-out-hidden {
    opacity: 0;
    height: 0;
    padding: 0;
    margin: 0;
    overflow: hidden;
    transition: opacity 0.5s ease-out, height 0s 0.5s;
    pointer-events: none;
}

@media (min-width: 768px) {
    .bg_Login {
        justify-content: space-between;
    }

    .main {
        text-align: left;
    }

    .titulo {
        font-size: 2.5rem;
        text-align: center;
    }
}

@media (min-width: 1024px) {
    .titulo {
        font-size: 1.5rem;
    }
}
```
Detalhes do código:

### <span style="color: #AC58FA;">Página de Cursos</span>
**cursos.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Cursos
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/cursos.css' %}">
{% endblock %}

{% block body %}

{% if messages %}
<div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
    {% for mensagem in messages %}
    {{ mensagem }}
    {% endfor %}
</div>
{% endif %}

<div class="container-conteudo animate downUp-1">
    <div class="topo">
        <h2 class="titulo">Cursos</h2>
        <div class="opcoes">
            <span>Cursos |</span>
            <a href="{% url 'relatorio' %}">
                <i class="bi bi-file-earmark-arrow-down pagina" aria-label="Baixar relatório"></i>
            </a>
            <span> | </span>
            <a href="{% url 'notificacoes' %}">
                <i class="notificacao bi {% if tem_notificacoes %}bi-envelope-paper{% else %}bi-envelope{% endif %} custom-icon"
                    aria-label="Ver notificações"></i>
            </a>
            <span> | </span>
            <i class="bi bi-search lupa" id="search-icon" aria-label="Pesquisar"></i>
            <div class="search-container" id="search-container">
                <form id="search-form" method="GET" action="{% url 'cursos' %}">
                    {{ form.search }}
                    <button type="submit">Pesquisar</button>
                </form>
            </div>
        </div>
    </div>
    <div class="container-cursos">
        <div class="ident">
            <h3 class="cabecalho">Curso</h3>
            <h3 class="cabecalho">Turma</h3>
            <h3 class="cabecalho">Responsável</h3>
        </div>
        <div class="fundo-curso" id="results-container">
            {% for curso in cursos %}
            <a href="{% url 'alunos' curso.turma %}">
                <div class="curso">
                    <h4 class="titulo-curso">{{ curso.nome_curso }}</h4>
                    <h4 class="titulo-curso">{{ curso.turma }}</h4>
                    <h4 class="titulo-curso">{{ curso.responsavel }}</h4>
                </div>
            </a>
            {% empty %}
            <p>Nenhum curso encontrado.</p>
            {% endfor %}
        </div>
    </div>
</div>
{% endblock %}
```

Detalhes do código:

#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
```html
{% extends 'index.html' %}
```

- O template **herda** o conteúdo de `index.html`, o que significa que ele usará a estrutura básica (cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.

#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}
```

- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.

#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```html
{% block title %}
Cursos
{% endblock %}
```

- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.

#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```html
{% block head %}
{% endblock %}
```

- O bloco **`*head*`** está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag **`*<head>*`** do HTML (como links de CSS ou meta tags). É necessário caso precise adicionar algo específico a esse bloco, podenso sobrescrevê-lo neste template ou em templates filhos.

#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```html
{% block body %}

{% if messages %}
<div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
    {% for mensagem in messages %}
    {{ mensagem }}
    {% endfor %}
</div>
{% endif %}

<div class="container-conteudo animate downUp-1">
    <div class="topo">
        <h2 class="titulo">Cursos</h2>
        <div class="opcoes">
            <span>Cursos |</span>
            <a href="{% url 'relatorio' %}">
                <i class="bi bi-file-earmark-arrow-down pagina" aria-label="Baixar relatório"></i>
            </a>
            <span> | </span>
            <a href="{% url 'notificacoes' %}">
                <i class="notificacao bi {% if tem_notificacoes %}bi-envelope-paper{% else %}bi-envelope{% endif %} custom-icon"
                    aria-label="Ver notificações"></i>
            </a>
            <span> | </span>
            <i class="bi bi-search lupa" id="search-icon" aria-label="Pesquisar"></i>
            <div class="search-container" id="search-container">
                <form id="search-form" method="GET" action="{% url 'cursos' %}">
                    {{ form.search }}
                    <button type="submit">Pesquisar</button>
                </form>
            </div>
        </div>
    </div>
    <div class="container-cursos">
        <div class="ident">
            <h3 class="cabecalho">Curso</h3>
            <h3 class="cabecalho">Turma</h3>
            <h3 class="cabecalho">Responsável</h3>
        </div>
        <div class="fundo-curso" id="results-container">
            {% for curso in cursos %}
            <a href="{% url 'alunos' curso.turma %}">
                <div class="curso">
                    <h4 class="titulo-curso">{{ curso.nome_curso }}</h4>
                    <h4 class="titulo-curso">{{ curso.turma }}</h4>
                    <h4 class="titulo-curso">{{ curso.responsavel }}</h4>
                </div>
            </a>
            {% empty %}
            <p>Nenhum curso encontrado.</p>
            {% endfor %}
        </div>
    </div>
</div>
{% endblock %}
```

- **Estrutura do `*body*`**:

Este é o conteúdo principal de uma página, onde a seção do corpo é definida. Contém o corpo de um documento ***HTML***, que é exibido pelo navegador em sua janela, ou seja, todo o conteúdo visível do site

- **Classe `container-conteudo` e Animação**:
    - A **`<div>`** com a classe `container-conteudo` serve como um **container** para o conteúdo da página.
    - A classe **`*animate downUp-1*`** indica que o conteúdo tem uma animação associada (definida no CSS), fazendo com que ele tenha um efeito visual de deslocamento ao ser carregado.
- **Seção Principal (`*main*`)**:
    - **Listagem dos Cursos:**
        - O link aponta para a URL associada ao nome de View **`*login`*** no Django, gerado dinamicamente com **`*{% url 'login' %}*`**.
        - O título da página, **"Cursos"**, é exibido dentro de um **`*<h2>*`** com a classe **`*.titulo*`**.
        - Na `<div class="alert-container">` há uma notificação que é exibida em caso de não existir cursos.
        - Na `<div>` com a classe de `opções`  ******é listado diversos ícones que redireciona o usuário para outras páginas, como a de notificações e relatórios e um botão para pesquisa de cursos específicos.
        - Na `<div class="container-curso">` é gerado os títulos da lista em um `<h3>` com a classe `cabecalho`
        - Para a geração da lista é importado os dados dos cursos por meio da `{% for curso in cursos %}` e suas informações são buscadas e exibidas nas `<h4>` com a classe `titulo-cursos` e em caso de não existir alunos será exibido um texto alertando, “Nenhum curso encontrado”.
        - Possui um botão que redireciona o usuário para a página de aluno pelo `{% url 'alunos' curso.turma %}`, quando o componente que contem o aluno for clicado, buscando os dados das turmas dos cursos.

**cursos.css**

```css
.container-conteudo {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background-color: var(--background-color);
    padding: 60px;
    box-sizing: border-box;
}

.container-cursos {
    width: 100%;
    max-width: 1000px;
    border-radius: 10px;
    color: #260104;
}

.curso {
    padding: 18px;
    border-radius: 20px;
    background: var(--list-bg-color);
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin: 15px 0;
    flex-wrap: wrap;
}

.curso:hover {
    background: #971c32;
    color: #fff;
    transition: background-color 0.3s ease, color 0.3s ease;
}

a {
    text-decoration: none;
}

a:hover {
    text-decoration: none;
}

.titulo-curso,
.detalhes-curso {
    font-size: 0.9rem;
    color: #454444;
    flex: 1;
    text-align: center;
    color: var(--text-color);
}

.topo {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.titulo {
    color: var(--text-color);
    font-size: 2rem;
    font-weight: 400;
    margin: 10px;
    padding: 30px;
}

.ident {
    display: flex;
    color: var(--text-color);
    justify-content: space-around;
    align-items: center;
    margin: 0 15px;
    flex-wrap: wrap;
    text-align: center;
    padding: 10px;
}

.cabecalho {
    font-size: 1.0rem;
    flex: 1;
    text-align: center;
}

.opcoes {
    display: flex;
    max-height: 35px;
    align-items: center;
    align-content: center;
    margin-left: 2rem;
    margin-bottom: 2rem;
    gap: 10px;
    font-size: 1.2rem;
    flex-wrap: wrap;
}

.lupa,
.pagina,

.notificacao {
    color: var(--text-color);
    cursor: pointer;
}

.lupa:hover,
.pagina:hover,
.notificacao:hover {
    color: #8C031C;
}

.search-container {
    display: flex;
    align-items: center;
    max-width: 0;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-out;
    overflow: hidden;
    margin-left: auto;
}

.search-container.visible {
    max-width: 660px;
    opacity: 1;
    visibility: visible;
}

.search-container form {
    display: flex;
    align-items: center;
    gap: 16px;
    width: 100%;
}

.search-container input {
    flex: 1;
    min-width: 200px;
    max-width: 400px;
    height: 36px;
    padding: 8px 16px;
    background: rgba(124, 13, 29, 0.6);
    font-size: 14px;
    border: none;
    border-radius: 20px;
    transition: all 0.3s ease;
}

.search-container input::placeholder {
    color: #fff;
}

.search-container input:focus {
    background: rgba(194, 67, 86, 0.8);
    box-shadow: 0 0 0 2px rgba(255, 6, 44, 0.3);
    color: #fff;
}

.search-container button {
    margin: 0;
    height: 36px;
    min-width: 80px;
    background: var(--button-home);
    color: var(--background-color);
    font-size: 14px;
    border: none;
    border-radius: 18px;
    cursor: pointer;
    transition: background-color 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
}

.search-container button:hover {
    background: var(--button-home-hover, rgb(143, 41, 41));
}

.fade-out {
    opacity: 1;
    transition: opacity 0.5s ease-out;
}

.fade-out-hidden {
    opacity: 0;
    height: 0;
    padding: 0;
    margin: 0;
    overflow: hidden;
    transition: opacity 0.5s ease-out, height 0s 0.5s;
    pointer-events: none;
}

@media screen and (max-width: 600px) {
    .search-container {
        width: 100%;
        margin: 8px 0;
    }

    .search-container form {
        width: 100%;
        gap: 8px;
    }

    .search-container input {
        min-width: 120px;
        font-size: 12px;
        padding: 8px 12px;
    }

    .search-container button {
        padding: 6px 12px;
        font-size: 12px;
        min-width: 60px;
    }

    .opcoes {
        font-size: 1rem;
        margin-left: 0.6rem;
    }
}
```

### <span style="color: #AC58FA;">Página de Alunos</span>
**alunos.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Gestão de Atrasos
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/alunos.css' %}">

<meta name="keywords"
    content="lista de alunos, gestão de frequência estudantil, controle de atrasos, presença de alunos, frequência escolar em tempo real, monitoramento de presença, sistema de gestão escolar">

{% endblock %}

{% block body %}
<div class="container-conteudo animate downUp-1">
    <div class="topo">
        <div class="voltar">
            <a href="{% url 'cursos' %}" aria-label="Voltar para a lista de cursos">
                <i class="bi bi-house-fill" aria-hidden="true"></i>
                <span>Voltar</span>
            </a>
        </div>
        <h2 class="titulo">{{ curso.nome_curso }}</h2>
    </div>
    <div class="container-atrasos">
        <div class="lista-alunos" role="table" aria-labelledby="alunos-table">
            <div class="ident" role="row">
                <div class="detalhes-info" role="columnheader">Aluno</div>
                <div class="detalhes-info" role="columnheader">Atrasos</div>
                <div class="detalhes-info" role="columnheader">Frequência</div>
                <div class="detalhes-info" role="columnheader">Faltas</div>
                {% if user.is_authenticated and user.is_superuser %}
                <div class="detalhes-info" role="columnheader">Opções</div>
                {% endif %}
            </div>

            {% for aluno in alunos_detalhes %}
            <div class="aluno-info" role="row">
                <div class="titulo-info" role="cell">{{ aluno.aluno }}</div>
                <div class="detalhes-info" role="cell">{{ aluno.atrasos }}</div>
                <div class="detalhes-info" role="cell">{{ aluno.porcentagem_carga_horaria }}%</div>
                <div class="detalhes-info" role="cell">{{ aluno.faltas }}</div>
                {% if user.is_authenticated and user.is_superuser %}
                <div class="detalhes-info" role="cell">
                    <form method="POST" action="{% url 'excluir_aluno' curso.turma aluno.id_carteirinha %}"
                        aria-label="Confirmar Exclusão">
                        {% csrf_token %}
                        <button type="submit" onclick="return confirm('Tem certeza de que deseja excluir este aluno?')"
                            aria-label="Excluir aluno: {{ aluno.aluno }}">
                            <i class="bi bi-trash" aria-hidden="true"></i>
                        </button>
                    </form>
                </div>
                {% endif %}
            </div>
            {% empty %}
            <p>Nenhum aluno encontrado.</p>
            {% endfor %}
        </div>

        <div class="inform">
            <div class="barra-lateral" aria-labelledby="informacoes-title">
                <h3 id="informacoes-title">Informações</h3>
                <p><strong>Responsável: </strong>{{ curso.responsavel }}</p>
                <p><strong>Código da Turma: </strong>{{ curso.turma }}</p>
                <p><strong>Horário: </strong>{{ curso.horario_entrada }} - {{ curso.horario_saida }}</p>
            </div>
            {% if user.is_authenticated and user.is_superuser %}
            <div class="botao-lateral">
                <button type="button" class="btn" data-bs-toggle="modal" data-bs-target="#excluirModal"
                    aria-label="Excluir curso {{ curso.nome_curso }}" style="font-size: 1rem;">Excluir Curso</button>
            </div>
            {% endif %}
        </div>
    </div>
</div>

<div class="modal fade" id="excluirModal" tabindex="-1" aria-labelledby="excluirModalLabel" aria-hidden="true"
    data-bs-backdrop="false">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header" data-bs-theme="dark">
                <h5 class="modal-title" id="excluirModalLabel" style="color: #FFF;">Excluir Curso
                </h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body" style="color: #FFF;">
                Tem certeza que deseja excluir este curso?<br><br>
                Observação: Ao deletar o curso, os alunos serão excluídos.
            </div>
            <div class="modal-footer" data-bs-theme="dark">
                <form method="POST" action="{% url 'excluir_curso' curso.turma %}" aria-label="Confirmar Exclusão"
                    style="margin: 0; padding: 0;">
                    {% csrf_token %}
                    <button type="submit" class="botao-cor" style="margin: 0;">
                        Excluir
                    </button>
                </form>
                <button type="button" class="botao-cor" data-bs-dismiss="modal">Cancelar</button>
            </div>
        </div>
    </div>
</div>
{% endblock %}
```

Detalhes do código:

#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
```html
{% extends 'index.html' %}
```

- O template **herda** o conteúdo de `index.html`, o que significa que ele usará a estrutura básica (cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.


#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}
```

- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.

#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```html
{% block title %}
Gestão de Atrasos
{% endblock %}
```

- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.

#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```html
{% block head %}
{% endblock %}
```

- O bloco **`*head*`** está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag **`*<head>*`** do HTML (como links de CSS ou meta tags). É necessário caso precise adicionar algo específico a esse bloco, podendo sobrescrevê-lo neste template ou em templates filhos.

#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```html
{% block body %}
<div class="container-conteudo animate downUp-1">
    <div class="topo">
        <div class="voltar">
            <a href="{% url 'cursos' %}" aria-label="Voltar para a lista de cursos">
                <i class="bi bi-house-fill" aria-hidden="true"></i>
                <span>Voltar</span>
            </a>
        </div>
        <h2 class="titulo">{{ curso.nome_curso }}</h2>
    </div>
    <div class="container-atrasos">
        <div class="lista-alunos" role="table" aria-labelledby="alunos-table">
            <div class="ident" role="row">
                <div class="detalhes-info" role="columnheader">Aluno</div>
                <div class="detalhes-info" role="columnheader">Atrasos</div>
                <div class="detalhes-info" role="columnheader">Frequência</div>
                <div class="detalhes-info" role="columnheader">Faltas</div>
                {% if user.is_authenticated and user.is_superuser %}
                <div class="detalhes-info" role="columnheader">Opções</div>
                {% endif %}
            </div>

            {% for aluno in alunos_detalhes %}
            <div class="aluno-info" role="row">
                <div class="titulo-info" role="cell">{{ aluno.aluno }}</div>
                <div class="detalhes-info" role="cell">{{ aluno.atrasos }}</div>
                <div class="detalhes-info" role="cell">{{ aluno.porcentagem_carga_horaria }}%</div>
                <div class="detalhes-info" role="cell">{{ aluno.faltas }}</div>
                {% if user.is_authenticated and user.is_superuser %}
                <div class="detalhes-info" role="cell">
                    <form method="POST" action="{% url 'excluir_aluno' curso.turma aluno.id_carteirinha %}"
                        aria-label="Confirmar Exclusão">
                        {% csrf_token %}
                        <button type="submit" onclick="return confirm('Tem certeza de que deseja excluir este aluno?')"
                            aria-label="Excluir aluno: {{ aluno.aluno }}">
                            <i class="bi bi-trash" aria-hidden="true"></i>
                        </button>
                    </form>
                </div>
                {% endif %}
            </div>
            {% empty %}
            <p>Nenhum aluno encontrado.</p>
            {% endfor %}
        </div>

        <div class="inform">
            <div class="barra-lateral" aria-labelledby="informacoes-title">
                <h3 id="informacoes-title">Informações</h3>
                <p><strong>Responsável: </strong>{{ curso.responsavel }}</p>
                <p><strong>Código da Turma: </strong>{{ curso.turma }}</p>
                <p><strong>Horário: </strong>{{ curso.horario_entrada }} - {{ curso.horario_saida }}</p>
            </div>
            {% if user.is_authenticated and user.is_superuser %}
            <div class="botao-lateral">
                <button type="button" class="btn" data-bs-toggle="modal" data-bs-target="#excluirModal"
                    aria-label="Excluir curso {{ curso.nome_curso }}" style="font-size: 1rem;">Excluir Curso</button>
            </div>
            {% endif %}
        </div>
    </div>
</div>

<div class="modal fade" id="excluirModal" tabindex="-1" aria-labelledby="excluirModalLabel" aria-hidden="true"
    data-bs-backdrop="false">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header" data-bs-theme="dark">
                <h5 class="modal-title" id="excluirModalLabel" style="color: #FFF;">Excluir Curso
                </h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body" style="color: #FFF;">
                Tem certeza que deseja excluir este curso?<br><br>
                Observação: Ao deletar o curso, os alunos serão excluídos.
            </div>
            <div class="modal-footer" data-bs-theme="dark">
                <form method="POST" action="{% url 'excluir_curso' curso.turma %}" aria-label="Confirmar Exclusão"
                    style="margin: 0; padding: 0;">
                    {% csrf_token %}
                    <button type="submit" class="botao-cor" style="margin: 0;">
                        Excluir
                    </button>
                </form>
                <button type="button" class="botao-cor" data-bs-dismiss="modal">Cancelar</button>
            </div>
        </div>
    </div>
</div>
{% endblock %}
```

- **Estrutura do `*body*`**:

Este é o conteúdo principal de uma página, onde a seção do corpo é definida. Contém o corpo de um documento ***HTML***, que é exibido pelo navegador em sua janela, ou seja, todo o conteúdo visível do site

- **Classe** `container-conteudo` **e Animação**:
    - A **`<div>`** com a classe `container-conteudo` serve como um **container** para o conteúdo da página.
    - A classe **`*animate downUp-1*`** indica que o conteúdo tem uma animação associada (definida no CSS), fazendo com que ele tenha um efeito visual de deslocamento ao ser carregado.
- **Seção Principal (`*main*`)**:
    - **Listagem das informações dos Alunos:**
        - O link aponta para a URL associada ao nome de View **`*login`*** no Django, gerado dinamicamente com **`*{% url 'login' %}*`**.
        - Um link por meio do componente `<a>` retorna o usuário para a página anterior
        - No título da página, o nome do Curso, é exibido dentro de um **`*<h2>`*** por meio de uma variável que exibe o nome correspondente ao curso sendo `{{ curso.nome_curso }}` , sendo estilizado com a classe **`*.titulo*`**.
        - Na `<div class="barra-lateral">` há vários componentes `<div>` que contem a classe `detalhes_info` , listando tópicos como nome do aluno, atraso, frequência, faltas e em caso do login ser feito com o perfil do administrador é exibido a opção de excluir curso ou usuário.
        - Na classe `alunos-info`  é exibido os dados específicos de cada aluno, sendo listados abaixo dos tópicos, ou em caso de não existir alunos, nada é exibido
        - Na `<div>` com a classe `modal`, utilizada para a exclusão de alunos e cursos, é exibido um componente de modal que ao ser clicado exibe uma confirmação de exclusão do aluno ou curso.

**alunos.css**

```css
body {
    font-family: "Kumbh Sans", sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    margin-top: 80px;
}

.container-conteudo {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background-color: var(--background-color);
    padding: 50px;
    text-align: center;
}

.topo {
    width: 100%;
    text-align: center;
    margin-bottom: 20px;
}

.titulo {
    color: var(--title);
    font-size: 2rem;
    font-weight: 400;
    text-align: center;
}

.container-atrasos {
    width: 90%;
    max-width: 1200px;
    border-radius: 10px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    min-height: 200px;
}

.lista-alunos {
    flex: 2;
    padding: 20px;
    border-radius: 10px;
    margin-right: 20px;
}

.ident {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    font-weight: 500;
}

.aluno-info {
    padding: 10px;
    border-radius: 20px;
    background: var(--list-bg-color);
    color: var(--text-color);
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 28px 0;
    flex-wrap: wrap;
    min-height: 50px;
}

.aluno-info button {
    background-color: transparent;
    margin: 0;
}

.aluno-info i {
    color: var(--text-color);
}

.voltar {
    font-family: "Krona One", sans-serif;
    font-size: 1rem;
    position: absolute;
    top: 5rem;
    left: 4.6rem;
    cursor: pointer;
}

.voltar a {
    text-decoration: none;
    color: var(--text-color);
}

.titulo-info,
.detalhes-info {
    font-size: 0.9rem;
    color: var(--title);
    flex: 1;
    text-align: center;
}

.inform {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding: 10px;
    padding-top: 64px;
    border-radius: 10px;
    align-items: flex-start;
    gap: 10px;
    max-width: 270px;
}

.inform h3 {
    margin: 0;
    color: var(--text-color);
}

.barra-lateral {
    display: flex;
    flex-direction: column;
    background: var(--list-bg-color);
    border-radius: 20px;
    width: 100%;
    padding: 1.2rem;
    text-align: left;
}

.barra-lateral h3 {
    align-self: center;
    font-family: "Krona One", sans-serif;
    font-size: 1rem;
    margin-bottom: 1rem;
}

.botao-lateral {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    width: 100%;
}

.botao-cor {
    color: white;
    background: var(--background);
}

.botao-cor:hover {
    color: #ffff;
    background: #971c32;
}

.botao-lateral button {
    color: var(--text-color);
    background: var(--list-bg-color);
    border-radius: 10px;
    width: 100%;
    text-align: center;
    padding: 15px;
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
    min-width: 150px;
}

.botao-lateral button:hover {
    background: #971c32;
    color: #fff;
}

.modal-content {
    background: var(--background);
    border-radius: 20px;
}

.modal-footer {
    display: flex;
    justify-content: end;
    align-items: center;
    gap: 15px;
}

form {
    margin-top: 0;
}

/* Responsividade */
@media (max-width: 768px) {
    .container-atrasos {
        flex-direction: column;
        align-items: center;
    }

    .container-conteudo {
        flex-wrap: wrap;
        flex-direction: column;
        align-items: center;
        align-content: center;
    }

    .aluno-info {
        flex-direction: column;
    }

    .inform {
        margin-top: 20px;
    }

    .ident {
        gap: 20px;
        align-items: center;
        align-content: center;
        text-align: center;
        padding: 5px;
        margin-bottom: 60px;
    }
}
```

### <span style="color: #AC58FA;">Página de Notificação</span>
**notificacoes.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Notificações
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/notificacoes.css' %}">

{% endblock %}

{% block body %}
<div class="container-conteudo animate downUp-1">
    <div class="topo">
        <div class="voltar">
            <a href="{% url 'cursos' %}">
                <i class="bi bi-house-fill"></i>
                <span>Voltar</span>
            </a>
        </div>
        <h2 class="titulo">Notificações</h2>
    </div>
    <div class="container-cursos">
        <div class="ident">
            <h5 class="nome-aluno">Nome</h5>
            <div class="detalhes-aluno">Atrasos</div>
            <div class="detalhes-aluno">Turma</div>
        </div>
        <div class="fundo-curso">
            {% for aluno in alunos_notificados %}
            <div class="curso">
                <h5 class="nome-aluno">{{ aluno.nome }}</h5>
                <div class="detalhes-aluno">{{ aluno.total_atrasos }}</div>
                <div class="detalhes-aluno">{{ aluno.turma}}</div>
            </div>
            {% empty %}
            <div class="curso">
                <h5 class="nome-aluno">Nenhum aluno com notificações.</h5>
                <div class="detalhes-aluno">0</div>
                <div class="detalhes-aluno">N/A</div>
            </div>
            {% endfor %}
        </div>
    </div>
</div>
{% endblock %}
```

Detalhes do código:

#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
```html
{% extends 'index.html' %}
```

- O template herda o conteúdo de `index.html`, o que significa que ele usará a estrutura básica 
(cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.

#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}
```

- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.


#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```html
{% block title %}
Notificações
{% endblock %}
```

- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.

#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```html
{% block head %}
{% endblock %}
```

- O bloco **`*head*`** está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag **`*<head>*`** do HTML (como links de CSS ou meta tags). É necessário caso precise adicionar algo específico a esse bloco, podenso sobrescrevê-lo neste template ou em templates filhos.

#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```html
{% block body %}
<div class="container-conteudo animate downUp-1">
    <div class="topo">
        <div class="voltar">
            <a href="{% url 'cursos' %}">
                <i class="bi bi-house-fill"></i>
                <span>Voltar</span>
            </a>
        </div>
        <h2 class="titulo">Notificações</h2>
    </div>
    <div class="container-cursos">
        <div class="ident">
            <h5 class="nome-aluno">Nome</h5>
            <div class="detalhes-aluno">Atrasos</div>
            <div class="detalhes-aluno">Turma</div>
        </div>
        <div class="fundo-curso">
            {% for aluno in alunos_notificados %}
            <div class="curso">
                <h5 class="nome-aluno">{{ aluno.nome }}</h5>
                <div class="detalhes-aluno">{{ aluno.total_atrasos }}</div>
                <div class="detalhes-aluno">{{ aluno.turma}}</div>
            </div>
            {% empty %}
            <div class="curso">
                <h5 class="nome-aluno">Nenhum aluno com notificações.</h5>
                <div class="detalhes-aluno">0</div>
                <div class="detalhes-aluno">N/A</div>
            </div>
            {% endfor %}
        </div>
    </div>
</div>
{% endblock %}
```

- **Estrutura do `*body*`**:

Este é o conteúdo principal de uma página, onde a seção do corpo é definida. Contém o corpo de um documento ***HTML***, que é exibido pelo navegador em sua janela, ou seja, todo o conteúdo visível do site

- **Classe** `container-conteudo` **e Animação**:
    - A **`<div>`** com a classe `container-conteudo` serve como um **container** para o conteúdo da página.
    - A classe **`*animate downUp-1*`** indica que o conteúdo tem uma animação associada (definida no CSS), fazendo com que ele tenha um efeito visual de deslocamento ao ser carregado.
- **Seção Principal (`*main*`)**:
    - **Listagem das Notificações:**
        - O link aponta para a URL associada ao nome de View **`*login`*** no Django, gerado dinamicamente com **`*{% url 'login' %}*`**.
        - Um link por meio do componente `<a>` retorna o usuário para a página anterior
        - O título da página, **"Notificações"**, é exibido dentro de um **`*<h2>*`** com a classe **`*.titulo*`**.
        - Na `<div class="container-cursos">` é listado todos os dados dos alunos separados pelos tópicos de Nome, Atrasos e Turma.
        - Na `<div>` com a classe de `fundo-curso` , é importado por meio do `{% for aluno in aluno_notificados %}` os dados dos alunos.
        - Na `<div class="container-curso">` é gerado os títulos da lista em um `<h3>` com a classe `cabecalho`
        - Em caso de não existir nenhum aluno com mais de 3 atrasos registrados, nada é listado.

**notificacoes.css**

```css
* {
    font-family: "Kumbh Sans";
}

.container-conteudo {
    min-height: 100%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background: var(--background-color);
    padding: 60px;
    box-sizing: border-box;
}

.container-cursos {
    width: 100%;
    max-width: 1000px;
    border-radius: 10px;
    color: #260104;
}

.curso {
    padding: 18px;
    border-radius: 20px;
    background: var(--list-bg-color);
    color: var(--text-color);
    display: flex;
    justify-content: space-around;
    align-items: center;
    align-content: center;
    margin: 15px 0;
    flex-wrap: wrap;
}

.curso .nome-aluno,
.curso .detalhes-aluno,
.curso .detalhes-info {
    flex: 1;
    text-align: center;
}

.fundo-curso a:hover .nome-aluno,
.fundo-curso a:hover .detalhes-aluno {
    color: #fff;
}

.fundo-curso :hover {
    background: #971C32;
    color: #fff;
    text-decoration: none;
}

.nome-aluno {
    margin: 0;
    font-size: 0.9rem;
    color: var(--text-color);
    flex: 1;
    text-align: center;
    text-decoration: none;
}

.detalhes-aluno {
    margin: 0;
    font-size: 0.9rem;
    color: var(--text-color);
    flex: 1;
    text-align: center;
    text-decoration: none;
}

.detalhes-info,
.options {
    text-decoration: none;
    color: var(--text-color);
    display: flexbox;
    gap: 10px;
}

.options a {
    color: var(--text-color);
    text-decoration: none;
}

.topo {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 10px;
}

.voltar {
    font-family: "Krona One", sans-serif;
    font-size: 1rem;
    display: flex;
    align-items: center;
    cursor: pointer;
    text-align: left;
    position: absolute;
    top: 5rem;
    left: 4.6rem;
}

.voltar i {
    margin-right: 4px;
    font-size: 1.1rem;
}

.voltar a {
    text-decoration: none;
    color: var(--text-color);
}

.titulo {
    color: var(--text-color);
    font-size: 2rem;
    font-weight: 400;
    margin: 20px;
    padding: 40px
}

.ident {
    display: flex;
    color: #ff0000;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
    text-align: center;
    padding: 10px;

}

.ident a {
    text-decoration: none;
    color: var(--text-color)
}

.ident a:hover {
    color: #971C32;
}

.titulo-curso {
    color: black;
}

@media (max-width: 768px) {
    .titulo-cabecalho {
        font-size: 2rem;
    }

    .curso,
    .ident {
        flex-direction: column;
        text-align: center;
    }

    .nome-aluno,
    .detalhes-aluno {
        font-size: 0.8rem;
        text-align: left;
    }
}
```

### <span style="color: #AC58FA;">Página de Relatórios</span>
**relatorio.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Relatório
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/relatorio.css' %}">
{% endblock %}

{% block body %}
<div class="bg_relatorio animate downUp-1">
    <div class="topo">
        <div class="voltar">
            <a href="{% url 'cursos' %}">
                <i class="bi bi-house-fill" aria-hidden="true"></i>
                <span>Voltar</span>
            </a>
        </div>
        <h2 class="titulo">Relatórios</h2>
    </div>
    <div class="container-cursos">
        <div class="imagem">
            <img src="{% static 'img/imagem_relatorios.webp' %}" alt="Imagem ilustrativa de relatórios">
        </div>
        <div class="relatorio-geral">
            <form method="GET" action="{% url 'relatorio' %}">
                <input type="hidden" name="format" value="pdf">
                <button type="submit">Gerar relatório em PDF</button>
            </form>
            <button type="button" data-bs-toggle="modal" data-bs-target="#relatorioModal">
                Sobre os Relatórios
            </button>
        </div>
    </div>
</div>

<div class="modal fade" id="relatorioModal" tabindex="-1" aria-labelledby="relatorioModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content" data-bs-theme="dark">
            <div class="modal-header">
                <h1 class="modal-title fs-5" id="relatorioModalLabel">Sobre os relatórios</h1>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                <p>
                    O relatório a ser baixado preza por mostrar à gestão escolar os dados referentes aos
                    maiores números de atrasos e faltas dos alunos, mostrando sua porcentagem total de frequência.
                    Assim, a gestão terá uma visão geral
                    sobre seus alunos, facilitando a tomada de decisões e gerenciamento da escola. Para
                    uma acessibilidade mais ampla, o relatório contará com tabelas contendo os dados a
                    serem analisados.
                </p>
            </div>
        </div>
    </div>
</div>

{% endblock %}
```

Detalhes do código:

#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
```html
{% extends 'index.html' %}
```

- O template **herda** o conteúdo de `index.html`, o que significa que ele usará a estrutura básica (cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.

#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}
```

- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.

#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```html
{% block title %}
Relatório
{% endblock %}
```

- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.

#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```html
{% block head %}
{% endblock %}
```

- O bloco **`*head*`** está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag **`*<head>*`** do HTML (como links de CSS ou meta tags). É necessário caso precise adicionar algo específico a esse bloco, podenso sobrescrevê-lo neste template ou em templates filhos.

#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```html
{% block body %}
<div class="bg_relatorio animate downUp-1">
    <div class="topo">
        <div class="voltar">
            <a href="{% url 'cursos' %}">
                <i class="bi bi-house-fill" aria-hidden="true"></i>
                <span>Voltar</span>
            </a>
        </div>
        <h2 class="titulo">Relatórios</h2>
    </div>
    <div class="container-cursos">
        <div class="imagem">
            <img src="{% static 'img/imagem_relatorios.webp' %}" alt="Imagem ilustrativa de relatórios">
        </div>
        <div class="relatorio-geral">
            <form method="GET" action="{% url 'relatorio' %}">
                <input type="hidden" name="format" value="pdf">
                <button type="submit">Gerar relatório em PDF</button>
            </form>
            <button type="button" data-bs-toggle="modal" data-bs-target="#relatorioModal">
                Sobre os Relatórios
            </button>
        </div>
    </div>
</div>

<div class="modal fade" id="relatorioModal" tabindex="-1" aria-labelledby="relatorioModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content" data-bs-theme="dark">
            <div class="modal-header">
                <h1 class="modal-title fs-5" id="relatorioModalLabel">Sobre os relatórios</h1>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                <p>
                    O relatório a ser baixado preza por mostrar à gestão escolar os dados referentes aos
                    maiores números de atrasos e faltas dos alunos, mostrando sua porcentagem total de frequência.
                    Assim, a gestão terá uma visão geral
                    sobre seus alunos, facilitando a tomada de decisões e gerenciamento da escola. Para
                    uma acessibilidade mais ampla, o relatório contará com tabelas contendo os dados a
                    serem analisados.
                </p>
            </div>
        </div>
    </div>
</div>

{% endblock %}
```

- **Estrutura do `*body*`**:

Este é o conteúdo principal de uma página, onde a seção do corpo é definida. Contém o corpo de um documento ***HTML***, que é exibido pelo navegador em sua janela, ou seja, todo o conteúdo visível do site

- **Classe `bg_relatorio` e Animação**:
    - A **`<div>`** com a classe `bg_relatorio` ****serve como um **container** para o conteúdo da página.
    - A classe **`*animate downUp-1*`** indica que o conteúdo tem uma animação associada (definida no CSS), fazendo com que ele tenha um efeito visual de deslocamento ao ser carregado.
- **Seção Principal (`*main*`)**:
    - **Listagem dos Relatórios:**
        - O link aponta para a URL associada ao nome de View **`*login`*** no Django, gerado dinamicamente com **`*{% url 'login' %}*`**.
        - Um link por meio do componente `<a>` retorna o usuário para a página anterior
        - O título da página, **"Relatórios"**, é exibido dentro de um **`*<h2>*`** com a classe **`*.titulo*`**.
        - Na `<div class="relatorio-geral">` é exibido um formulário exibindo a opção “Gerar um relatório em PDF”
        - No componente de botão, ao ser clicado é exibido uma modal sobre as informações que serão exibidas no relatório em PDF

**relatorio.css**

```css
* {
    font-family: "Kumbh Sans";
}

.bg_relatorio {
    min-height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    background-color: var(--background-color);
    padding: 40px;
    margin: 0px;
}

.topo {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.voltar {
    font-family: "Krona One", sans-serif;
    font-size: 1rem;
    display: flex;
    align-items: center;
    cursor: pointer;
    text-align: left;
    position: absolute;
    top: 5rem;
    left: 4.6rem;
}

.voltar i {
    margin-right: 4px;
    font-size: 1.1rem;
}

.voltar a {
    text-decoration: none;
    color: var(--text-color);
}

.titulo {
    font-size: 2rem;
    color: var(--title);
    font-weight: 400;
    margin-bottom: 20px;
    text-align: center;
}

.container-cursos {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%;
}

.imagem {
    max-width: 450px;
    max-height: 300px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.imagem img {
    width: 100%;
    height: auto;
    align-items: center;
    justify-content: center;

}

.icons {
    display: flex;
    align-items: center;
}

.icons i {
    margin-left: 10px;
    cursor: pointer;
    color: var(--text-color);
}

.relatorio-geral {
    text-align: center;
    display: flex;
    flex-direction: column;
}

.relatorio-geral button {
    background: var(--list-bg-color);
    border: none;
    border-radius: 20px;
    color: var(--text-color);
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
}

.relatorio-geral button:hover {
    background: #8C031C;
    color: #fff;
}

.modal-content {
    background: var(--background);
    color: #fff;
    border-radius: 20px;
}

@media (max-width: 768px) {
    .titulo {
        font-size: 1rem;
    }

    .container-cursos {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .relatorio-lista {
        margin-right: 0;
        width: 100%;
    }

    .imagem {
        max-width: 300px;
    }

    .relatorio-item {
        flex-direction: column;
        text-align: center;
    }

    .voltar {
        left: 10px;
        top: 10px;
    }
}
```

### <span style="color: #AC58FA;">Página de Cadastro</span>
**cadastro.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Cadastro
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/cadastro.css' %}">

{% endblock %}

{% block body %}
<div class="bg_Cadastro animate downUp-1">
    <div class="voltar">
        <a href="{% url 'cursos' %}">
            <i class="bi bi-house-fill"></i>
            <span>Voltar</span>
        </a>
    </div>
    <div class="main">
        <form method="post">
            <h2 class="titulo" style="color: white;">Fazer Cadastro</h2>
            {% csrf_token %}

            <div class="mb-3">
                <label for="exampleInputName" class="form-label">Nome</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.nome }}
                </div>
            </div>

            <div class="mb-3">
                <label for="exampleInputSobrenome" class="form-label">Sobrenome</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.sobrenome }}
                </div>
            </div>

            <div class="mb-3">
                <label for="exampleInputUser" class="form-label">Usuário</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.username }}
                </div>
            </div>

            <div class="mb-3">
                <label for="exampleInputPassword" class="form-label">Senha</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-key icone"></i>
                    </span>
                    {{ form.senha }}
                </div>
            </div>

            {% if messages %}
            <div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
                {% for mensagem in messages %}
                {{ mensagem }}
                {% endfor %}
            </div>
            {% endif %}

            <div style="justify-content: center; align-items: center">
                <button class="button" type="submit"
                    style="color: #40010D; text-decoration: none; text-align:center;">Cadastrar</button>
            </div>
        </form>
    </div>
    <div class="imag">
        <img src="{% static 'img/img_cadastro.webp' %}" alt="Imagem">
    </div>
</div>
{% endblock %}
```

Detalhes do código:

#### **<span style="color: #AC58FA;">1. Extensão de Template</span>**
**1. Extensão de Template**

```html
{% extends 'index.html' %}
```

- O template **herda** o conteúdo de `index.html`, o que significa que ele usará a estrutura básica (cabeçalho, rodapé, etc.) definida no arquivo `index.html`. O conteúdo específico será inserido nos **blocos** definidos no template pai.

#### **<span style="color: #AC58FA;">2. Carregamento de Arquivos Estáticos</span>**
```html
{% load static %}
```

- O comando `{% load static %}` é utilizado para **carregar arquivos estáticos** no Django (como imagens, arquivos CSS, JavaScript), que são armazenados em diretórios específicos. No código, isso permite que você acesse imagens e outros recursos estáticos.

#### **<span style="color: #AC58FA;">3. Bloco title</span>**
```html
{% block title %}
Cadastro
{% endblock %}
```

- Este bloco define o título da página que aparecerá na **aba do navegador**.
- Como o template extende `index.html`, esse bloco sobrescreve o título padrão do arquivo pai, definindo o título como **"Homepage"**.

#### **<span style="color: #AC58FA;">4. Bloco head</span>**
```html
{% block head %}
{% endblock %}
```

- O bloco **`*head*`** está vazio neste template, mas ele é utilizado para incluir **conteúdo adicional** dentro da tag **`*<head>*`** do HTML (como links de CSS ou meta tags). É necessário caso precise adicionar algo específico a esse bloco, podenso sobrescrevê-lo neste template ou em templates filhos.

#### **<span style="color: #AC58FA;">5. Bloco body</span>**
```html
{% block body %}
<div class="bg_Cadastro animate downUp-1">
    <div class="voltar">
        <a href="{% url 'cursos' %}">
            <i class="bi bi-house-fill"></i>
            <span>Voltar</span>
        </a>
    </div>
    <div class="main">
        <form method="post">
            <h2 class="titulo" style="color: white;">Fazer Cadastro</h2>
            {% csrf_token %}

            <div class="mb-3">
                <label for="exampleInputName" class="form-label">Nome</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.nome }}
                </div>
            </div>

            <div class="mb-3">
                <label for="exampleInputSobrenome" class="form-label">Sobrenome</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.sobrenome }}
                </div>
            </div>

            <div class="mb-3">
                <label for="exampleInputUser" class="form-label">Usuário</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-person icone"></i>
                    </span>
                    {{ form.username }}
                </div>
            </div>

            <div class="mb-3">
                <label for="exampleInputPassword" class="form-label">Senha</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-key icone"></i>
                    </span>
                    {{ form.senha }}
                </div>
            </div>

            {% if messages %}
            <div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
                {% for mensagem in messages %}
                {{ mensagem }}
                {% endfor %}
            </div>
            {% endif %}

            <div style="justify-content: center; align-items: center">
                <button class="button" type="submit"
                    style="color: #40010D; text-decoration: none; text-align:center;">Cadastrar</button>
            </div>
        </form>
    </div>
    <div class="imag">
        <img src="{% static 'img/img_cadastro.webp' %}" alt="Imagem">
    </div>
</div>
{% endblock %}
```

- **Estrutura do `*body*`**:

Este é o conteúdo principal de uma página, onde a seção do corpo é definida. Contém o corpo de um documento ***HTML***, que é exibido pelo navegador em sua janela, ou seja, todo o conteúdo visível do site

- **Classe `bg_relatorio` e Animação**:
    - A **`<div>`** com a classe `bg_relatorio` ****serve como um **container** para o conteúdo da página.
    - A classe **`*animate downUp-1*`** indica que o conteúdo tem uma animação associada (definida no CSS), fazendo com que ele tenha um efeito visual de deslocamento ao ser carregado.
- **Seção Principal (`*main*`)**:
    - **Formulário de Cadastro:**
        - O link aponta para a URL associada ao nome de View **`*login`*** no Django, gerado dinamicamente com **`*{% url 'login' %}*`**.
        - Um link por meio do componente `<a>` retorna o usuário para a página anterior
        - O título da página, **"Fazer Cadastro"**, é exibido dentro de um **`*<h2>*`** com a classe **`*.titulo*`**.
        - Na `<label>` com a classe `form-label`  é requerido Nome, Sobrenome  e senha do usuário
        - Em caso de alguma informação estar sendo inserida no formato errado será exibido uma notificação de alerta de que há informações inseridas de forma incorreta
- **Imagem de Fundo**:
    - Dentro de **`*<div class="imag">*`**, uma imagem de fundo é carregada com a tag **`*<img>*`**, utilizando o arquivo de imagem estática **`*img_cadastro.webp*`** (com o caminho definido pelo **`*{% static 'img/img_cadastro.webp' %}*`**).
    - A imagem tem largura de **400px** e altura de **300px**.
    

**cadastro.css**

```css
* {
    font-family: "Kumbh Sans";
}

.bg_Cadastro {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    background-color: var(--background-color);
    gap: 10px;
    padding: 80px;
    padding-top: 60px;
}

.voltar {
    font-family: "Krona One", sans-serif;
    font-size: 1rem;
    display: flex;
    align-items: center;
    cursor: pointer;
    text-align: left;
    position: absolute;
    top: 5rem;
    left: 4.6rem;
}

.voltar i {
    margin-right: 4px;
    font-size: 1.1rem;
}

.voltar a {
    text-decoration: none;
    color: var(--text-color);
}

.main {
    padding: 40px;
    background: var(--background);
    border-radius: 30px;
    text-align: center;
    width: 100%;
    max-width: 400px;
    margin: 30px;
}

.button {
    color: #260164;
    background-color: #FFFAFB;
    border: none;
    padding: 10px 20px;
    border-radius: 10px;
    margin-top: 20px;
    width: 100%;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: background-color 0.3s ease;
}

.button:hover {
    background-color: #f2f2f2;
    color: #40010D;
}

.alert-success {
    background-color: #d4edda;
    color: #155724;
}

.alert-warning {
    background-color: #fff3cd;
    color: #856404;
}

.imag {
    width: 100%;
    max-width: 600px;
}

.imag img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.titulo {
    color: #ffff;
    font-size: 2.5rem;
    font-weight: 400;
    margin-bottom: 20px;
}

.form {
    border: none;
    background: var(--input-bg);
    color: #FFFAFB;
}

.form::placeholder {
    color: #FFFAFB;
    font-size: 13px;
}

.form:focus {
    border: none;
    background: var(--input-bg);
    color: #FFFAFB;
}

.form-label {
    color: #FFFAFB;
}

.icone {
    color: #FFFAFB;
}

.input-group {
    border: none;
    overflow: hidden;
    border-radius: 5px;
    background: var(--input-bg);
    padding: 1px;
}

.input-group .form-control {
    border: none;
    border-radius: 0;
}

.input-group-text {
    background-color: var(--input-bg);
    border: none;
    color: #FFFAFB;
}

.fade-out {
    opacity: 1;
    transition: opacity 0.5s ease-out;
}

.fade-out-hidden {
    opacity: 0;
    height: 0;
    padding: 0;
    margin: 0;
    overflow: hidden;
    transition: opacity 0.5s ease-out, height 0s 0.5s;
    pointer-events: none;
}

@media (min-width: 768px) {
    .bg_Cadastro {
        justify-content: space-between;
        gap: 10px;
    }

    .main {
        text-align: left;
    }

    .titulo {
        font-size: 1.5rem;
        text-align: center;
    }
}

@media (min-width: 1024px) {
    .titulo {
        font-size: 1.5rem;
    }
}
```

### <span style="color: #AC58FA;">Páginas de adicionar curso, aluno e frequência</span>
**criar_curso.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Criar Curso
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/formulario.css' %}">
{% endblock %}

{% block body %}
<div class="voltar">
    <a href="{% url 'cursos' %}">
        <i class="bi bi-house-fill" aria-hidden="true"></i>
        <span>Voltar</span>
    </a>
</div>
<div class="formulario">

    <form action="{% url 'criar_curso' %}" method="post" enctype="multipart/form-data">
        {% csrf_token %}
        <label for="cursos" class="titulo">
            <h2>Selecione o arquivo</h2>
        </label>

        <div class="input-group mb-3">
            <input type="file" class="form-control" id="cursos" name="cursos" accept=".csv">
            <label class="input-group-text" for="inputGroupFile02"
                style="align-items: center; justify-content: center;"><button
                    style="background: transparent; color: #fefffa; align-items: center; justify-content: center;color: white; margin: 0; padding: 0;"
                    type="submit">Enviar</button></label>
        </div>
    </form>
</div>

{% endblock %}
```

**criar_aluno.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Criar Aluno
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/formulario.css' %}">
{% endblock %}

{% block body %}
<div class="voltar">
    <a href="{% url 'cursos' %}">
        <i class="bi bi-house-fill" aria-hidden="true"></i>
        <span>Voltar</span>
    </a>
</div>
<div class="formulario">
    <form action="{% url 'criar_aluno' %}" method="post" enctype="multipart/form-data">
        {% csrf_token %}
        <label for="alunos" class="titulo">
            <h2>Selecione o arquivo</h2>
        </label>

        <div class="input-group mb-3">
            <input type="file" class="form-control" id="alunos" name="alunos" accept=".csv">
            <label class="input-group-text" for="inputGroupFile02"
                style="align-items: center; justify-content: center;"><button
                    style="background: transparent; color: #fefffa; align-items: center; justify-content: center;color: white; margin: 0; padding: 0;"
                    type="submit">Enviar</button></label>
        </div>
    </form>
</div>

{% endblock %}
```

**frequencia.html**

```html
{% extends 'index.html' %}
{% load static %}

{% block title %}
Frequência
{% endblock %}

{% block head %}
<link rel="stylesheet" href="{% static 'css/formulario.css' %}">
{% endblock %}

{% block body %}
<div class="voltar">
    <a href="{% url 'cursos' %}">
        <i class="bi bi-house-fill" aria-hidden="true"></i>
        <span>Voltar</span>
    </a>
</div>
<div class="formulario">
    <form action="{% url 'freq' %}" method="post" enctype="multipart/form-data">
        {% csrf_token %}
        <label for="freq">
            <h2>Selecione o arquivo</h2>
        </label>

        <div class="input-group mb-3">
            <input type="file" class="form-control" id="freq" name="freq" accept=".txt">
            <label class="input-group-text" for="inputGroupFile02"
                style="align-items: center; justify-content: center;"><button
                    style="background: transparent; color: #fefffa; align-items: center; justify-content: center; margin: 0; padding: 0;"
                    type="submit">Enviar</button></label>
        </div>
    </form>
</div>

{% endblock %}
```

**formulario.css**

```css
body {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    min-height: 100vh;
    margin: 0;
    font-family: "Kumbh Sans";
    background-color: var(--background-color);

}

.formulario {
    background: var(--background);
    color: #fefffa;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    text-align: center;
    margin-bottom: 50px;
}

.formulario form {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;

}

.formulario label {
    margin-bottom: 10px;
}

.formulario input[type="file"] {
    margin-bottom: 15px;
}

.form-control {
    height: 42px;
}

.input-group-text {
    height: 42px;
    background: var(--background);
    color: #fefffa;
}

.voltar {
    font-family: "Krona One", sans-serif;
    font-size: 1rem;
    position: absolute;
    top: 7rem;
    left: 4.6rem;
    cursor: pointer;
}

.voltar a {
    text-decoration: none;
    color: var(--text-color);
}

.titulo {
    font-family: "Krona One", sans-serif;
    font-size: 2rem;
    margin-bottom: 20px;
    color: #fefffa;
}
```

---

### <span style="color: #AC58FA;">Lógica de mostrar e esconder senha</span>

Na página de login, para o melhor desempenho do site em relação ao usuário, foi adicionada uma lógica que possibilita esconder e mostrar a senha, de acordo com a preferência de quem estiver inserindo suas informações.
Os arquivos usados para a realização dessa tarefa foram:

- **HTML** - base da parte visual, contendo os elementos (tags) responsáveis pelos itens do site.
- **JavaScript** - responsável pela lógica.

***obs:** a estilização foi usada na tag `<style></style>` dentro do arquivo HTML.*

**Passo a passo do processo:**

#### **<span style="color: #AC58FA;">1- Base no HTML</span>**


```html
<div class="mb-3">
                <label for="senha" class="form-label">Senha</label>
                <div class="input-group">
                    <span class="input-group-text">
                        <i class="bi bi-key icone"></i>
                    </span>
                    {{ form.senha }}
                    <i class="bi bi-eye esconder_senha" onclick="mostrar()" id="btnSenha"></i> <!--ta errado-->
                </div>
            </div>
            {% if messages %}
            <div id="alert-container" class="mt-2 alert alert-warning fade-out" role="alert">
                {% for mensagem in messages %}
                {{ mensagem }}
                {% endfor %}
            </div>
            {% endif %}
```

#### **<span style="color: #AC58FA;">2- Lógica no JavaScript</span>**

```jsx
function mostrar() {
    var inputPass = document.getElementById('id_password');
    var btnShowPass = document.getElementById('btnSenha');
/* Os elementos que contém a senha e seu botão de exibir/esconder são capturados*/

    if (inputPass.type === 'password') {
        inputPass.setAttribute('type', 'text');
        btnShowPass.classList.replace('bi-eye', 'bi-eye-slash');
    } else {
        inputPass.setAttribute('type', 'password');
        btnShowPass.classList.replace('bi-eye-slash', 'bi-eye');
    }
}
```

### <span style="color: #AC58FA;">**Lógicas no arquivo views.py**</span>
Nesse arquivo, cada função (def) representa uma view, de acordo com a arquitetura MTV (Model-Template-View).
Importações realizadas:
```python
from .models import *
from .forms import *
from django.conf import settings
from django.shortcuts import render, redirect, get_object_or_404
from django.contrib.auth.models import User, Group
from django.contrib.auth.decorators import login_required
from django.contrib.auth import authenticate, login as auth_login, logout as auth_logout
from django.db import IntegrityError, connection
from django.contrib import messages
from django.core.files.storage import FileSystemStorage
from datetime import datetime
from django.http import FileResponse
from reportlab.lib import colors
from reportlab.lib.pagesizes import A4
from django.views.decorators.cache import cache_control
from reportlab.lib.styles import getSampleStyleSheet, ParagraphStyle
from reportlab.lib.units import inch
from reportlab.platypus import Table, TableStyle, Paragraph, SimpleDocTemplate, Spacer, Image
from io import BytesIO
import csv
import os
```
Dados:
- As importações feitas da biblioteca *ReportLab* são voltadas para a lógica de realização de relatórios, além de *BytesIO*, importado de *io*, e outras ferramentas disponibilizadas pelo framework Django.
- A função de *login_required*, importada de *django.contrib.auth.decorators*, serve para requerir o login a cada função a ser realizada que contenha essa ferramenta.


### <span style="color: #9A2EFE;">Lógicas de Login e Logout</span>
A função login é responsável por autenticar os usuários no sistema. Ela valida as credenciais enviadas pelo formulário de login e, caso sejam válidas, autentica o usuário e redireciona-o para a página principal do sistema. Caso contrário, exibe uma mensagem de erro. Essa função também garante que a página não seja armazenada no cache do navegador para melhorar a segurança.

#### <span style="color: #AC58FA;">**Login**</span>
```python
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def login(request):
    
    context = {}

    if request.method == "POST":
        form = FormLogin(request.POST)
    
        if form.is_valid():
            var_username = form.cleaned_data['username']
            var_senha = form.cleaned_data['senha']

            user = authenticate(username=var_username, password=var_senha)
            if user is not None:
                auth_login(request, user)
                return redirect("cursos")
            else:
                messages.error(request, "Nome de usuário ou senha incorretos.")
                return redirect("login")
    else:
        form = FormLogin()

    context.update({"form": form})
    return render(request, 'login.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**1. Decorador `@cache_control`**

```python
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
```

- Este decorador configura o cabeçalho HTTP para que a página de login não seja armazenada no cache do navegador. Ele utiliza três parâmetros:
    - **`no_cache=True`**: garante que o navegador sempre revalide o conteúdo com o servidor.
    - **`must_revalidate=True`**: especifica que qualquer dado armazenado no cache deve ser validado antes de ser reutilizado.
    - **`no_store=True`**: impede o armazenamento da página no cache local ou em cache intermediário.

Essas configurações são importantes para evitar que informações sensíveis sejam acessadas de forma não autorizada.

**2. Definição da Função**

```python
def login(request):
    context = {}

```

- A função recebe um parâmetro:
    - **`request`**: representa a solicitação HTTP feita pelo usuário.
- **`context`**: um dicionário usado para armazenar dados a serem enviados para o template HTML.

**3. Verificação do Método HTTP**

```python
if request.method == "POST":

```

- Verifica se o método da solicitação é `POST`. Isso indica que o formulário foi enviado pelo usuário.

**4. Inicialização do Formulário**

```python
form = FormLogin(request.POST)

```

- O objeto `FormLogin` é instanciado com os dados enviados pelo formulário. Esse formulário foi previamente definido para validar os campos necessários (ex.: `username` e `senha`).

**5. Validação do Formulário**

```python
if form.is_valid():
    var_username = form.cleaned_data['username']
    var_senha = form.cleaned_data['senha']

```

- **`form.is_valid()`**: verifica se os dados enviados pelo usuário atendem às regras de validação definidas no formulário.
- **`form.cleaned_data`**: extrai os dados limpos do formulário para uso no código.

**6. Autenticação do Usuário**

```python
user = authenticate(username=var_username, password=var_senha)
```

- A função **`authenticate`** verifica as credenciais fornecidas:
    - Se as credenciais estiverem corretas, retorna o objeto do usuário.
    - Caso contrário, retorna `None`.
    

**7. Verificação do Usuário**

```python
if user is not None:
    auth_login(request, user)
    return redirect("cursos")
else:
    messages.error(request, "Nome de usuário ou senha incorretos.")
    return redirect("login")
```

- Se o usuário for autenticado com sucesso:
    - **`auth_login(request, user)`**: Realiza o login do usuário no sistema.
    - **`redirect("cursos")`**: Redireciona o usuário autenticado para a página principal do sistema.
- Se a autenticação falhar:
    - **`messages.error`**: Adiciona uma mensagem de erro informando que o nome de usuário ou a senha estão incorretos.
    - **`redirect("login")`**: Redireciona o usuário de volta para a página de login.
    

**8. Tratamento do Método `GET`**

```python
else:
    form = FormLogin()

```

- Se o método HTTP da solicitação for `GET`, um formulário vazio é instanciado.

**9. Contexto e Renderização**

```python
context.update({"form": form})
return render(request, 'login.html', context)
```

- O formulário (com ou sem erros) é adicionado ao dicionário `context`.
- **`render(request, 'login.html', context)`**: Renderiza a página de login, enviando o formulário para exibição no template `login.html`.

#### <span style="color: #AC58FA;">***Fluxo de Execução***</span>

1. **Requisição GET**:
    - Um formulário vazio é exibido ao usuário.
2. **Requisição POST**:
    - O formulário é processado.
    - As credenciais são verificadas:
        - Se forem válidas: o usuário é autenticado e redirecionado.
        - Caso contrário: uma mensagem de erro é exibida, e o usuário é redirecionado para tentar novamente.
        

#### <span style="color: #AC58FA;">***Considerações de Segurança***</span>

1. **Prevenção de Cache**:
    - A utilização de `@cache_control` impede que dados sensíveis fiquem acessíveis via cache.
2. **Mensagens de Erro Genéricas**:
    - Mensagens genéricas como "Nome de usuário ou senha incorretos" dificultam que um invasor identifique se um nome de usuário existe no sistema.
3. **Validação e Sanitização de Dados**:
    - O uso de `form.is_valid()` e `form.cleaned_data` garante que os dados sejam devidamente validados e sanitizados antes do processamento.
    

#### <span style="color: #AC58FA;">***Dependências Externas***</span>

- **`FormLogin`**: classe do formulário de login, definida em um arquivo de formulários (ex.: `forms.py`).
- **`authenticate` e `auth_login`**: funções do Django usadas para autenticar e logar usuários.
- **`messages.error`**: módulo do Django utilizado para exibir mensagens temporárias ao usuário.
- **`redirect` e `render`**: funções auxiliares do Django para redirecionar ou renderizar páginas HTML.

#### <span style="color: #AC58FA;">**Logout**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `logout` é uma funcionalidade simples e essencial em aplicativos Django que gerenciam autenticação de usuários. Sua principal responsabilidade é encerrar a sessão de um usuário autenticado e redirecioná-lo para a página inicial do sistema.

Caso o usuário queira sair do sistema (logout), a lógica apresentada abaixo permite que o faça.

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def logout(request):
    auth_logout(request)
    return redirect("homepage")
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Componentes:**

1. **Decoradores:**
    - `@login_required`:
        - Garante que apenas usuários autenticados possam acessar essa função. Se um usuário não autenticado tentar acessar, ele será redirecionado para a página de login.
    - `@cache_control(no_cache=True, must_revalidate=True, no_store=True)`:
        - Define cabeçalhos HTTP relacionados ao cache para esta função. Essas configurações ajudam a proteger a página e os dados do usuário ao impedir o armazenamento no cache do navegador:
            - `no_cache=True`: Evita que o conteúdo seja armazenado em cache.
            - `must_revalidate=True`: Força o navegador a revalidar os dados antes de reutilizá-los.
            - `no_store=True`: Garante que nada seja armazenado no cache.
2. **`logout(request)` (Função):**
    - `auth_logout(request)`:
        - Esta função, fornecida pelo Django, encerra a sessão do usuário atual, removendo suas informações de autenticação.
        - Isso invalida o cookie de sessão, efetivamente desconectando o usuário.
    - `return redirect("homepage")`:
        - Após a execução do logout, o usuário é redirecionado para a página inicial do site (identificada pela URL "homepage").
        

**Lógica Completa:**

1. **Autenticação Obrigatória:**
    - Somente usuários autenticados podem acessar a função, garantindo segurança.
2. **Logout Seguro:**
    - Quando o usuário solicita logout, suas credenciais e dados de sessão são removidos.
3. **Controle de Cache:**
    - As configurações de cache evitam que o navegador armazene informações da sessão anterior, protegendo os dados do usuário, especialmente em computadores compartilhados.
4. **Redirecionamento:**
    - Após o logout, o usuário é levado para a página inicial do site.


### <span style="color: #9A2EFE;">Lógica de Registrar Frequência Fictícia</span>
#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `upload_frequencia` é responsável por realizar o upload, processamento e salvamento de dados de frequência a partir de um arquivo `.txt`. O arquivo deve conter dados de frequência tabulados (separados por tabulação). A função verifica a existência de alunos associados aos registros no banco de dados e cria entradas de frequência relacionadas.

Essa funcionalidade é protegida por autenticação e requer que o usuário esteja logado para acessá-la.
```python
@login_required
def upload_frequencia(request):
        if request.method == 'POST' and 'freq' in request.FILES:
            txt_file = request.FILES['freq']

            fs = FileSystemStorage()
            filename = fs.save(txt_file.name, txt_file)

            # Abrir o arquivo TXT
            with open(fs.path(filename), newline='', encoding='ISO-8859-1') as txtfile:
                reader = csv.reader(txtfile, delimiter='\t')  # Usando tabulação como delimitador

                for row in reader:
                    try:
                        # Assumindo que o TXT contém as colunas na ordem: data, id_carteirinha, hora, identificador
                        data = row[0].strip()  # Data da frequência
                        id_carteirinha = int(row[1].strip())
                        hora = row[2].strip()  # Hora da frequência
                        identificador = int(row[3].strip())  # Identificador de entrada ou saída

                        # Buscar o aluno pelo id_carteirinha
                        aluno = Aluno.objects.get(id_carteirinha=id_carteirinha)

                        # Criar a frequência no banco
                        Frequencia.objects.create(
                            id_aluno=aluno,
                            data=data,
                            hora=hora,
                            identificador=identificador
                        )

                    except Aluno.DoesNotExist:
                        print(request, f"Aluno com carteirinha {id_carteirinha} não encontrado.")
                    except IndexError:
                        print(request, "Erro no formato do arquivo TXT.")
                    except Exception as e:
                        print(request, f"Erro ao salvar a frequência: {str(e)}")

            messages.success(request, "Frequências carregadas com sucesso.")
            return redirect("homepage")

        return render(request, 'frequencia.html')
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**1. Decorador `@login_required`**

- Garante que apenas usuários autenticados possam acessar a função.
- Caso um usuário não autenticado tente acessar, ele será redirecionado para a página de login.

**2. Verificação do Método HTTP**

```python
if request.method == 'POST' and 'freq' in request.FILES:

```

- **`request.method == 'POST'`**: Verifica se a solicitação é do tipo POST, indicando que o arquivo foi enviado.
- **`'freq' in request.FILES`**: Certifica-se de que o arquivo enviado está presente no campo `freq` do formulário.

**3. Salvamento do Arquivo**

```python
fs = FileSystemStorage()
filename = fs.save(txt_file.name, txt_file)

```

- **`FileSystemStorage`**: Gerencia o armazenamento de arquivos no sistema de arquivos.
- **`fs.save()`**: Salva o arquivo no diretório configurado (geralmente no diretório de mídia).

**4. Abertura e Leitura do Arquivo TXT**

```python
with open(fs.path(filename), newline='', encoding='ISO-8859-1') as txtfile:
    reader = csv.reader(txtfile, delimiter='\t')

```

- **`fs.path(filename)`**: Obtém o caminho completo do arquivo salvo.
- **`encoding='ISO-8859-1'`**: Define o encoding para leitura do arquivo. O formato `ISO-8859-1` é comum em arquivos gerados em sistemas legados.
- **`csv.reader`**: Lê o arquivo, considerando tabulação (`\t`) como delimitador.

**5. Processamento de Cada Linha**

```python
for row in reader:
    try:
        data = row[0].strip()
        id_carteirinha = int(row[1].strip())
        hora = row[2].strip()
        identificador = int(row[3].strip())

```

- Itera sobre cada linha do arquivo.
- Os dados são extraídos e convertidos conforme necessário:
    - **`data`**: Data do registro.
    - **`id_carteirinha`**: ID único da carteirinha do aluno.
    - **`hora`**: Hora do registro.
    - **`identificador`**: Indica se o registro é de entrada ou saída (número inteiro).
    

**6. Verificação e Criação de Frequência**

```python
aluno = Aluno.objects.get(id_carteirinha=id_carteirinha)
Frequencia.objects.create(
    id_aluno=aluno,
    data=data,
    hora=hora,
    identificador=identificador
)

```

- **`Aluno.objects.get(id_carteirinha=id_carteirinha)`**:
    - Busca no banco de dados o aluno associado ao `id_carteirinha`.
    - Caso o aluno não exista, é lançada uma exceção `Aluno.DoesNotExist`.
- **`Frequencia.objects.create()`**:
    - Cria um registro na tabela `Frequencia` associando:
        - O aluno encontrado.
        - Data e hora da frequência.
        - Identificador do tipo de registro (entrada ou saída).
        

**7. Tratamento de Exceções**

```python
except Aluno.DoesNotExist:
    print(request, f"Aluno com carteirinha {id_carteirinha} não encontrado.")
except IndexError:
    print(request, "Erro no formato do arquivo TXT.")
except Exception as e:
    print(request, f"Erro ao salvar a frequência: {str(e)}")

```

- **`Aluno.DoesNotExist`**: Captura casos onde um `id_carteirinha` não corresponde a nenhum aluno.
- **`IndexError`**: Trata erros de formato no arquivo TXT, como colunas ausentes.
- **`Exception`**: Captura quaisquer outros erros não específicos durante o processamento.

**8. Mensagem de Sucesso e Redirecionamento**

```python
messages.success(request, "Frequências carregadas com sucesso.")
return redirect("homepage")
```

- **`messages.success`**: Exibe uma mensagem ao usuário indicando que o processo foi concluído com sucesso.
- **`redirect("homepage")`**: Redireciona o usuário para a página principal do sistema.

**9. Renderização Inicial**

```python
return render(request, 'frequencia.html')
```

- Caso a solicitação seja do tipo `GET`, renderiza a página `frequencia.html`, que contém o formulário para envio do arquivo.

#### <span style="color: #AC58FA;">***Fluxo de Execução***</span>

1. **Requisição GET**:
    - A página para envio do arquivo é exibida.
2. **Requisição POST**:
    - O arquivo TXT é enviado e salvo no sistema.
    - Cada linha do arquivo é processada para criar registros de frequência no banco.
    - Mensagens de erro são exibidas para casos específicos:
        - Aluno não encontrado.
        - Formato incorreto do arquivo.
    - Mensagem de sucesso é exibida ao final do processamento.
3. **Redirecionamento**:
    - Após o processamento, o usuário é redirecionado para a página inicial.
    
#### <span style="color: #AC58FA;">***Considerações de Segurança***</span>

1. **Proteção por Login**:
    - Apenas usuários autenticados podem acessar a funcionalidade.
2. **Validação do Arquivo**:
    - O código assume que o arquivo enviado segue um formato esperado (TXT tabulado). Adicionar validações adicionais seria uma boa prática.
3. **Tratamento de Exceções**:
    - As exceções capturadas garantem que o sistema não falhe completamente devido a erros isolados.
    
#### <span style="color: #AC58FA;">***Dependências Externas***</span>

- **`FileSystemStorage`**: Gerencia o armazenamento e acesso ao arquivo TXT.
- **`Aluno` e `Frequencia`**: Modelos do banco de dados, usados para consultar e criar registros.
- **`csv.reader`**: Biblioteca padrão do Python para leitura de arquivos tabulados.
- **`messages.success`**: Componente do Django usado para exibir mensagens temporárias ao usuário.
- **`redirect` e `render`**: Funções do Django para redirecionar e renderizar páginas.


### <span style="color: #9A2EFE;">Lógica de Cálculo de Frequência dos Alunos</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `alunos` exibe detalhes sobre a frequência, presença, faltas e atrasos dos alunos de uma turma específica. Ela utiliza consultas SQL avançadas com tabelas e funções analíticas para calcular métricas de desempenho de frequência por aluno, relacionadas à carga horária total e porcentagem de presença no curso.

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def alunos(request, turma):
    curso = get_object_or_404(Curso, turma=turma)

    with connection.cursor() as cursor:
        cursor.execute("""
            WITH frequencias_calculadas AS (
                SELECT 
                    f.id_aluno_id,
                    f.data,
                    f.hora,
                    LEAD(f.hora) OVER (PARTITION BY f.id_aluno_id, f.data ORDER BY f.hora) AS proxima_hora,
                    CAST(f.identificador AS INTEGER) AS identificador,
                    CASE 
                        WHEN CAST(f.identificador AS INTEGER) = 2 
                        AND NOT EXISTS (
                            SELECT 1
                            FROM web_frequencia f2 
                            WHERE f2.id_aluno_id = f.id_aluno_id 
                            AND f2.data = f.data 
                            AND CAST(f2.identificador AS INTEGER) = 1
                        ) THEN true
                        ELSE false
                    END AS apenas_saida
                FROM 
                    web_frequencia AS f
            ),
            presenca_por_dia AS (
                SELECT 
                    aluno.id_carteirinha,
                    f.data,
                    CASE 
                        WHEN f.apenas_saida THEN
                            EXTRACT(EPOCH FROM (
                                f.hora - c.horario_entrada
                            )) / 3600.0
                            - 
                            EXTRACT(EPOCH FROM c.carga_horaria_intervalo) / 3600.0
                        WHEN CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN
                            CASE 
                                WHEN f.hora IS NULL THEN 0
                                ELSE
                                    EXTRACT(EPOCH FROM LEAST(
                                        COALESCE(f.proxima_hora, c.horario_saida),
                                        c.horario_saida
                                    ) - 
                                    GREATEST(
                                        f.hora,
                                        c.horario_entrada
                                    )) / 3600.0
                                    - 
                                    EXTRACT(EPOCH FROM c.carga_horaria_intervalo) / 3600.0
                            END
                        ELSE 0
                    END AS horas_presenca,
                    CASE 
                        WHEN f.id_aluno_id IS NULL THEN 1
                        WHEN f.apenas_saida THEN 0         
                        WHEN f.hora IS NULL AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN 1 
                        ELSE 0 
                    END AS teve_falta,
                    CASE 
                        WHEN f.apenas_saida THEN 0
                        WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN 1 
                        ELSE 0 
                    END AS teve_atraso,
                    CASE 
                        WHEN CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 
                            OR CAST(COALESCE(f.identificador, 0) AS INTEGER) = 2
                            OR f.apenas_saida
                            OR f.hora IS NOT NULL
                        THEN 1
                        ELSE 0
                    END AS presenca
                FROM 
                    web_aluno AS aluno
                CROSS JOIN
                    web_curso AS c 
                LEFT JOIN 
                    frequencias_calculadas AS f ON aluno.id_carteirinha = f.id_aluno_id
                    AND f.data BETWEEN c.data_inicio AND c.data_fim
                WHERE 
                    c.turma = %s
            ),
            totais_aluno AS (
                SELECT 
                    aluno.id_carteirinha,
                    COALESCE(SUM(p.horas_presenca), 0) AS total_horas_presenca,
                    COALESCE(COUNT(DISTINCT CASE WHEN p.teve_atraso = 1 THEN p.data END), 0) AS total_atrasos,
                    COALESCE(COUNT(DISTINCT CASE WHEN p.presenca = 1 THEN p.data END), 0) AS total_presencas
                FROM 
                    web_aluno AS aluno
                LEFT JOIN 
                    presenca_por_dia AS p ON aluno.id_carteirinha = p.id_carteirinha
                WHERE
                    aluno.id_curso_id = %s
                GROUP BY 
                    aluno.id_carteirinha
            )
            SELECT 
                aluno.id_carteirinha,
                aluno.nome,
                GREATEST(c.dias_letivos - t.total_presencas, 0) AS total_faltas,  -- Atualizado para calcular total_faltas
                t.total_atrasos,
                t.total_presencas,
                LEAST(t.total_horas_presenca, 600) AS carga_horaria_cumprida,
                CASE 
                    WHEN c.dias_letivos > 0 THEN 
                        LEAST(100, ROUND((LEAST(t.total_horas_presenca, 600) / (c.dias_letivos * 7.5)) * 100, 2))
                    ELSE 0
                END AS porcentagem_frequencia
            FROM 
                web_aluno AS aluno
            JOIN 
                totais_aluno AS t ON aluno.id_carteirinha = t.id_carteirinha
            JOIN 
                web_curso AS c ON aluno.id_curso_id = c.turma
            WHERE 
                c.turma = %s
            ORDER BY 
                aluno.nome;
        """, [curso.turma, curso.turma, curso.turma])

        resultados = cursor.fetchall()

    alunos_detalhes = []
    for resultado in resultados:
        alunos_detalhes.append({
            'id_carteirinha': resultado[0],
            'aluno': resultado[1],
            'faltas': resultado[2],
            'atrasos': resultado[3],
            'presencas': resultado[4],
            'carga_horaria_aluno': resultado[5],
            'porcentagem_carga_horaria': round(resultado[6], 2),
        })

    context = {
        'curso': curso,
        'alunos_detalhes': alunos_detalhes,
    }

    return render(request, 'alunos.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**1. Decoradores**

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
```

- **`@login_required`**: Garante que somente usuários autenticados possam acessar a função.
- **`@cache_control`**: Desativa o cache do navegador para evitar a exibição de dados desatualizados.

**2. Obtenção do Curso**

```python
curso = get_object_or_404(Curso, turma=turma)
```

- Usa o `get_object_or_404` para buscar o curso pela turma. Retorna erro 404 se não encontrar.

**3. Consulta SQL Avançada**

A consulta realiza as seguintes etapas:

**a) Subconsulta: `frequencias_calculadas`**

- Utiliza a função `LEAD` para calcular a próxima hora de registro de presença.
- Identifica registros de apenas saída (`apenas_saida`), ausência de entrada, e outros dados de frequência.

**b) Subconsulta: `presenca_por_dia`**

- Calcula as horas de presença por dia, considerando atrasos e faltas.
- Garante que somente alunos dentro do período letivo sejam avaliados.

**c) Subconsulta: `totais_aluno`**

- Soma horas de presença, conta atrasos e dias de presença para cada aluno.
- Agrupa os dados por aluno.

**d) Resultado Final**

- Calcula faltas restantes (`total_faltas`) baseadas nos dias letivos do curso.
- Garante que a carga horária máxima não exceda 600 horas.
- Calcula a porcentagem de frequência com base no total de horas exigidas pelo curso.

**4. Processamento de Resultados**

```python
alunos_detalhes = []
for resultado in resultados:
    alunos_detalhes.append({
        'id_carteirinha': resultado[0],
        'aluno': resultado[1],
        'faltas': resultado[2],
        'atrasos': resultado[3],
        'presencas': resultado[4],
        'carga_horaria_aluno': resultado[5],
        'porcentagem_carga_horaria': round(resultado[6], 2),
    })
```

- Converte os resultados da consulta para um dicionário utilizável no template.

**5. Renderização do Template**

```python
context = {
    'curso': curso,
    'alunos_detalhes': alunos_detalhes,
}

return render(request, 'alunos.html', context)
```

- Passa os detalhes do curso e dos alunos para o template `alunos.html`.


### <span style="color: #9A2EFE;">Lógica de Geração de Relatórios</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `gerar_relatorio_pdf` gera um relatório em formato PDF que apresenta informações detalhadas sobre frequência e atrasos de alunos, estruturando os dados de forma organizada e visualmente atrativa. O relatório inclui tabelas, gráficos e textos formatados para facilitar a análise de desempenho acadêmico.

```python
def gerar_relatorio_pdf(relatorio):
    buffer = BytesIO()
    doc = SimpleDocTemplate(buffer, pagesize=A4, title="Relatório de Frequência")
    elementos = []

    styles = getSampleStyleSheet()
    styles.add(ParagraphStyle(name="Subtitle", fontSize=18, leading=22, spaceAfter=12, alignment=1))

    caminho_imagem = os.path.join(settings.BASE_DIR, 'static', 'img', 'senai_logo.webp')

# Se o caminnho existe, realizar ações na imagem (retorna valor booleano)
    if os.path.exists(caminho_imagem):
        img = Image(caminho_imagem)
        img.drawHeight = 0.5 * inch 
        img.drawWidth = 1.5 * inch 
        elementos.append(img)
    else:
        elementos.append(Paragraph("Imagem não encontrada", styles['BodyText']))
    # Estilos para título e subtítulo
    styles = getSampleStyleSheet()
    styles.add(ParagraphStyle(name="Subtitle", fontSize=18, leading=22, spaceAfter=12, alignment=1))

    # Capa do Relatório
    # Variável para verificar o dia a aparecer no relatório
    hoje = datetime.now().strftime('%d/%m/%Y')
    elementos.append(Spacer(1, 12))
    elementos.append(Paragraph("Relatório de Frequência e Atrasos", styles['Title']))
    elementos.append(Paragraph("Análise de Desempenho dos Alunos", styles['Subtitle']))
    elementos.append(Paragraph(f"Gerado em: {hoje}", styles['BodyText']))
    elementos.append(Spacer(1, 12))

    # Tabela Resumo 
    elementos.append(Paragraph("Análise de Dados", styles['Heading2']))

    # Tabela de Alunos com Mais Atrasos
    elementos.append(Paragraph("Alunos com Mais Atrasos", styles['Heading3']))
    top_atrasos_data = [['Nome', 'Turma', 'Total de Atrasos']]
    for aluno in relatorio:
        if aluno['categoria'] == 'Top Atrasos':
            top_atrasos_data.append([
                aluno['nome'],
                aluno['turma'],
                str(aluno['total_atrasos'])
            ])
    # Definindo propriedades da tabela
    top_atrasos_table = Table(top_atrasos_data, colWidths=[2.5 * inch, 1.0 * inch, 1.2 * inch, 1.2 * inch, 1.0 * inch])
    top_atrasos_table.setStyle(TableStyle([
        ('BACKGROUND', (0, 0), (-1, 0), colors.Color(223/255, 78/255, 78/255)),
        ('TEXTCOLOR', (0, 0), (-1, 0), colors.white),
        ('ALIGN', (0, 0), (-1, -1), 'CENTER'),
        ('FONTNAME', (0, 0), (-1, 0), 'Helvetica-Bold'),
        ('FONTSIZE', (0, 0), (-1, 0), 10),
        ('FONTSIZE', (0, 1), (-1, -1), 8),
        ('BOTTOMPADDING', (0, 0), (-1, 0), 10),
        ('BACKGROUND', (0, 1), (-1, -1), colors.whitesmoke),
        ('GRID', (0, 0), (-1, -1), 0.5, colors.black),
        ('VALIGN', (0, 1), (-1, -1), 'MIDDLE')
    ]))
    elementos.append(top_atrasos_table)
    elementos.append(Spacer(1, 12))

    # Tabela de Alunos com Baixa Frequência
    elementos.append(Paragraph("Alunos com Baixa Frequência", styles['Heading3']))
    baixa_frequencia_data = [['Nome', 'Turma', 'Total de Faltas']]
    for aluno in relatorio:
        if aluno['categoria'] == 'Baixa Frequência':
            baixa_frequencia_data.append([
                aluno['nome'],
                aluno['turma'],
                str(aluno['total_faltas'])
            ])
    baixa_frequencia_table = Table(baixa_frequencia_data, colWidths=[2.5 * inch, 1.0 * inch, 1.2 * inch, 1.2 * inch, 1.0 * inch])
    baixa_frequencia_table.setStyle(TableStyle([
        ('BACKGROUND', (0, 0), (-1, 0), colors.Color(223/255, 78/255, 78/255)),
        ('TEXTCOLOR', (0, 0), (-1, 0), colors.white),
        ('ALIGN', (0, 0), (-1, -1), 'CENTER'),
        ('FONTNAME', (0, 0), (-1, 0), 'Helvetica-Bold'),
        ('FONTSIZE', (0, 0), (-1, 0), 10),
        ('FONTSIZE', (0, 1), (-1, -1), 8),
        ('BOTTOMPADDING', (0, 0), (-1, 0), 10),
        ('BACKGROUND', (0, 1), (-1, -1), colors.whitesmoke),
        ('GRID', (0, 0), (-1, -1), 0.5, colors.black),
        ('VALIGN', (0, 1), (-1, -1), 'MIDDLE')
    ]))
    elementos.append(baixa_frequencia_table)
    elementos.append(Spacer(1, 12))

    # Tabela de Informações Detalhadas dos Alunos
    elementos.append(Paragraph("Detalhes dos Alunos", styles['Heading2']))
    detalhes_alunos_data = [['Nome', 'Turma', 'Total de Atrasos', 'Total de Faltas']]
    for aluno in relatorio:
        detalhes_alunos_data.append([
            aluno['nome'],
            aluno['turma'],
            str(aluno['total_atrasos']),
            str(aluno['total_faltas'])
        ])
    detalhes_alunos_table = Table(detalhes_alunos_data, colWidths=[2.5 * inch, 1.0 * inch, 1.2 * inch, 1.2 * inch, 1.0 * inch])
    detalhes_alunos_table.setStyle(TableStyle([
        ('BACKGROUND', (0, 0), (-1, 0), colors.Color(223/255, 78/255, 78/255)),
        ('TEXTCOLOR', (0, 0), (-1, 0), colors.white),
        ('ALIGN', (0, 0), (-1, -1), 'CENTER'),
        ('FONTNAME', (0, 0), (-1, 0), 'Helvetica-Bold'),
        ('FONTSIZE', (0, 0), (-1, 0), 10),
        ('FONTSIZE', (0, 1), (-1, -1), 8),
        ('BOTTOMPADDING', (0, 0), (-1, 0), 10),
        ('BACKGROUND', (0, 1), (-1, -1), colors.whitesmoke),
        ('GRID', (0, 0), (-1, -1), 0.5, colors.black),
        ('VALIGN', (0, 1), (-1, -1), 'MIDDLE')
    ]))
    elementos.append(detalhes_alunos_table)

    # Construção do PDF
    doc.build(elementos)
    buffer.seek(0)
    return buffer
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Criação do buffer**

Dentro da função de estilizar e gerar relatório, foi criada uma variável chamada *buffer*:

```python
buffer = BytesIO()
doc = SimpleDocTemplate(buffer, pagesize=A4, title="Relatório de Frequência")
```

- Buffer significa uma área em que os dados serão armazenados temporariamente enquanto vão de um sistema de *input* para um sistema de *output* (enquanto estão sendo processados).
- O uso de *BytesIO()* significa que os dados inseridos na variável serão transformados em *bytes* enquanto forem armazenados.

**Documento em PDF**

1. **Uso de ReportLab**:
    - A biblioteca é utilizada para criar o PDF com texto, imagens e tabelas.
    - A classe `SimpleDocTemplate()` cria o template vinculado ao nome do arquivo.
    - As tabelas são estilizadas com `Table` e `TableStyle`.
    
2. **Estrutura do Relatório**:
    - **Capa do relatório**: para capa do relatório, foram adicionadas informações relevantes:
        
        ```python
        hoje = datetime.now().strftime('%d/%m/%Y')
            elementos.append(Spacer(1, 12))
            elementos.append(Paragraph("Relatório de Frequência e Atrasos", styles['Title']))
            elementos.append(Paragraph("Análise de Desempenho dos Alunos", styles['Subtitle']))
            elementos.append(Paragraph(f"Gerado em: {hoje}", styles['BodyText']))
            elementos.append(Spacer(1, 12))
        ```
        
        - A variável `hoje` foi criada para definir o dia, utilizando a classe datetime e os métodos `now` e `strftime`.
        - Foram adicionados elementos como espaço e parágrafo, através da variável criada previamente.
    - **Tabelas**:
        - "Alunos com Mais Atrasos".
        - "Alunos com Baixa Frequência".
        - "Detalhes dos Alunos".
    - As tabelas são geradas dinamicamente a partir da lista `relatorio`, que deve conter os dados organizados por categoria e outros atributos dos alunos.
    
3. **Verificação de imagem**:
    - Verifica se o arquivo de logo (`senai_logo.webp`) está no diretório esperado e o adiciona ao PDF.
        - Uma variável `caminho_imagem` foi criada para definir o caminho da imagem a ser inserida no documento, através do módulo `os`
        - É usada a classe `Imagem` para inserir a imagem, caso o caminho exista.
            
            Para a tabela de alunos com mais atrasos e frequência mais baixa, além da, foram adicionados títulos e foram criadas listas, que conterão o conteúdo das colunas e linhas.
            
            Em seguida, as tabelas foram estilizadas
            
    
4. **Personalização do Estilo**:
    - Usa estilos predefinidos e customizados do `getSampleStyleSheet` para títulos, subtítulos e corpo do texto.

A variável `buffer` é chamada em seguida, como demonstrado abaixo:

```python
buffer.seek(0)
```

A função *seek* é usada para mover o cursor ao lugar desejado do arquivo ao ser aberto, em que 0 significa que será movido para o início do arquivo.


### <span style="color: #9A2EFE;">**Lógica de Consulta de Relatório**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `relatorio` é responsável por gerar e exibir um relatório de frequência e atrasos de alunos. O relatório pode ser exibido em uma página HTML ou baixado como PDF, dependendo do parâmetro `format` passado na requisição.

```python
# Controle de acesso para a função
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def relatorio(request):
# Realização da consulta no banco de dados
    with connection.cursor() as cursor:
        cursor.execute("""
            WITH frequencias_calculadas AS (
                SELECT 
                    f.id_aluno_id,
                    f.data,
                    f.hora,
                    LEAD(f.hora) OVER (PARTITION BY f.id_aluno_id, f.data ORDER BY f.hora) AS proxima_hora,
                    CAST(f.identificador AS INTEGER) AS identificador,
                    CASE
                        WHEN CAST(f.identificador AS INTEGER) = 2 
                        AND NOT EXISTS (
                            SELECT 1
                            FROM web_frequencia f2 
                            WHERE f2.id_aluno_id = f.id_aluno_id 
                            AND f2.data = f.data 
                            AND CAST(f2.identificador AS INTEGER) = 1
                        ) THEN true
                        ELSE false
                    END AS apenas_saida
                FROM 
                    web_frequencia AS f
            ),
            atrasos_aluno AS (
                SELECT 
                    aluno.id_carteirinha,
                    aluno.nome,
                    c.turma,
                    COUNT(DISTINCT CASE WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN f.data END) AS total_atrasos,
                    COUNT(DISTINCT f.data) AS dias_presenca,
                    c.dias_letivos,
                    GREATEST(c.dias_letivos - COUNT(DISTINCT f.data), 0) AS total_faltas
                FROM 
                    web_aluno AS aluno
                JOIN 
                    web_curso AS c ON aluno.id_curso_id = c.turma
                LEFT JOIN 
                    frequencias_calculadas AS f ON aluno.id_carteirinha = f.id_aluno_id
                    AND f.data BETWEEN c.data_inicio AND c.data_fim
                GROUP BY 
                    aluno.id_carteirinha, aluno.nome, c.turma, c.dias_letivos
            ),
            frequencia_aluno AS (
                SELECT
                    nome,
                    turma,
                    total_atrasos,
                    dias_presenca,
                    dias_letivos,
                    total_faltas
                FROM 
                    atrasos_aluno
            ),
            top_atrasos AS (
                SELECT nome, turma, total_atrasos, total_faltas
                FROM frequencia_aluno
                ORDER BY total_atrasos DESC
                LIMIT 5
            ),
            baixa_frequencia AS (
                SELECT nome, turma, total_atrasos, total_faltas
                FROM frequencia_aluno
                LIMIT 5
            )
            
            SELECT 
                'Top Atrasos' AS categoria, 
                nome, turma, total_atrasos, total_faltas
            FROM 
                top_atrasos
            UNION ALL
            SELECT 
                'Baixa Frequência' AS categoria, 
                nome, turma, total_atrasos, total_faltas
            FROM 
                baixa_frequencia
            ORDER BY 
                categoria, total_atrasos DESC;
        """)
        alunos_detalhes = cursor.fetchall()

    relatorio = [
        {
            'categoria': row[0],
            'nome': row[1],
            'turma': row[2],
            'total_atrasos': row[3],
            'total_faltas': row[4],
        } for row in alunos_detalhes
    ]

    if request.GET.get('format') == 'pdf':
        buffer = gerar_relatorio_pdf(relatorio)
        
        return FileResponse(buffer, as_attachment=True, filename="relatorio_de_frequencia.pdf")
    
    context = {'relatorio': relatorio}
    return render(request, 'relatorio.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Informações**

- Após a consulta ao banco de dados, é criada a compreensão de lista `relatorio`, em que os resultados brutos da consulta são transformados em uma lista de dicionários mais legível.
- Essa compreensão de lista atua sobre cada *row* (linha) e adiciona um dicionário com chaves descritivas para cada uma.
- Dentro de um `if`, é conferido se o formato está conforme esperado. Caso esteja, a variável buffer converterá a função de gerar relatório em bytes.

**1. Decoradores**

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)

```

- **@login_required**:
    
    Garante que apenas usuários autenticados possam acessar a função.
    
- **@cache_control(no_cache=True, must_revalidate=True, no_store=True)**:
    
    Impede o armazenamento em cache para garantir que os dados exibidos estejam sempre atualizados.
    

**2. Parâmetros de Entrada**

- **request**:
Contém os dados da requisição HTTP, permitindo verificar o formato de saída desejado (HTML ou PDF).

**3. Execução da Consulta SQL**

A consulta é estruturada com subconsultas para organizar e consolidar os dados em várias etapas:

**a) Subconsulta: `frequencias_calculadas`**

- Calcula:
    - **Hora seguinte** (`proxima_hora`) usando a função analítica `LEAD`.
    - Identifica se o registro representa apenas uma saída, sem entrada correspondente (`apenas_saida`).
- Garante que os dados sejam organizados por aluno e data.

**b) Subconsulta: `atrasos_aluno`**

- Relaciona os alunos com os dados de frequência.
- Calcula:
    - Total de atrasos (`total_atrasos`): Dias em que o aluno chegou mais de 10 minutos atrasado.
    - Dias de presença (`dias_presenca`): Total de dias em que o aluno foi identificado.
    - Total de faltas (`total_faltas`): Diferença entre dias letivos e dias de presença.

**c) Subconsulta: `frequencia_aluno`**

- Estrutura os dados consolidados para serem utilizados nas categorias finais.

**d) Subconsulta: `top_atrasos`**

- Seleciona os 5 alunos com o maior número de atrasos.

**e) Subconsulta: `baixa_frequencia`**

- Seleciona os 5 alunos com menor frequência (independente do número de atrasos).

**f) Resultado Final**

- Consolida os dados em duas categorias:
    - "Top Atrasos": Alunos com maior número de atrasos.
    - "Baixa Frequência": Alunos com menor índice de presença.
    

**4. Processamento dos Resultados**

```python
alunos_detalhes = cursor.fetchall()
```

- Os resultados são armazenados em uma lista estruturada de dicionários, onde cada entrada contém:
    - **categoria**: Tipo de registro (Top Atrasos ou Baixa Frequência).
    - **nome**: Nome do aluno.
    - **turma**: Turma do aluno.
    - **total_atrasos**: Número total de atrasos.
    - **total_faltas**: Número total de faltas.
    

**5. Geração do PDF**

Se a requisição contém o parâmetro `format=pdf`, o relatório é convertido para PDF:

```python
if request.GET.get('format') == 'pdf':
    buffer = gerar_relatorio_pdf(relatorio)
    return FileResponse(buffer, as_attachment=True, filename="relatorio_de_frequencia.pdf")
```

**6. Renderização do Template**

Se a saída é HTML, os dados são enviados para o template:

```python
context = {'relatorio': relatorio}
return render(request, 'relatorio.html', context)

```

- O template exibe o relatório com base nas informações calculadas.


### <span style="color: #9A2EFE;">Lógica de Notificações</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `notificacoes` é responsável por calcular e exibir notificações relacionadas a atrasos frequentes de alunos em seus horários de entrada. Utilizando consultas SQL complexas, a função verifica alunos que acumularam três ou mais atrasos durante o período letivo e exibe essas informações na interface do usuário.

Essa funcionalidade é protegida por autenticação e caching está desabilitado para garantir a exibição de dados atualizados.
Essa lógica foi realizada na função de notificacoes, realizando uma consulta no banco de dados, buscando alunos com mais de 3 atrasos, e fazendo aparecer na página correspondente.

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def notificacoes(request):
    with connection.cursor() as cursor:
        cursor.execute("""
            WITH frequencias_calculadas AS (
                SELECT 
                    f.id_aluno_id,
                    f.data,
                    f.hora,
                    LEAD(f.hora) OVER (PARTITION BY f.id_aluno_id, f.data ORDER BY f.hora) AS proxima_hora,
                    CAST(f.identificador AS INTEGER) AS identificador,
                    CASE 
                        WHEN CAST(f.identificador AS INTEGER) = 2 
                        AND NOT EXISTS (
                            SELECT 1
                            FROM web_frequencia f2 
                            WHERE f2.id_aluno_id = f.id_aluno_id 
                            AND f2.data = f.data 
                            AND CAST(f2.identificador AS INTEGER) = 1
                        ) THEN true
                        ELSE false
                    END as apenas_saida
                FROM 
                    web_frequencia AS f
            ),
            atrasos_aluno AS (
                SELECT 
                    aluno.id_carteirinha,
                    aluno.nome,
                    c.turma,
                    COUNT(DISTINCT CASE WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN f.data END) AS total_atrasos
                FROM 
                    web_aluno AS aluno
                JOIN 
                    web_curso AS c ON aluno.id_curso_id = c.turma
                LEFT JOIN 
                    frequencias_calculadas AS f ON aluno.id_carteirinha = f.id_aluno_id
                    AND f.data BETWEEN c.data_inicio AND c.data_fim
                GROUP BY 
                    aluno.id_carteirinha, aluno.nome, c.turma
                HAVING 
                    COUNT(DISTINCT CASE WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN f.data END) >= 3
            )
            SELECT 
                nome,
                turma,
                total_atrasos
            FROM 
                atrasos_aluno
            ORDER BY 
                nome;
        """)

        notificacoes = cursor.fetchall()

    alunos_notificados = []
    for notificacao in notificacoes:
        alunos_notificados.append({
            'nome': notificacao[0],
            'turma': notificacao[1],
            'total_atrasos': notificacao[2],
        })

    tem_notificacoes = len(alunos_notificados) > 0
    context = {
        'alunos_notificados': alunos_notificados,
        'tem_notificacoes': tem_notificacoes,
    }

    return render(request, 'notificacoes.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Informações:**

1. **Autenticação e Cache:**
    - O decorator `@login_required` garante que apenas usuários autenticados possam acessar essa funcionalidade.
    - `@cache_control(no_cache=True, must_revalidate=True, no_store=True)` desabilita o cache da página para garantir que as informações exibidas estejam sempre atualizadas.
    
2. **Consulta SQL Complexa:**
    - Utiliza a conexão direta ao banco de dados (`connection.cursor()`) para executar uma consulta SQL detalhada com subconsultas e janelas analíticas. A consulta pode ser dividida em etapas:
    
    a. **Subconsulta `frequencias_calculadas`:**
    
    - Processa os dados de frequência (`web_frequencia`) para:
        - Identificar a próxima marcação de horário usando a função `LEAD`.
        - Verificar se há registros de "saída" (`identificador = 2`) sem uma entrada correspondente no mesmo dia.
        
    
    b. **Subconsulta `atrasos_aluno`:**
    
    - Calcula o total de atrasos por aluno considerando:
        - Um atraso ocorre quando a hora de entrada (`identificador = 1`) excede o horário de entrada do curso por mais de 10 minutos.
        - Filtra apenas as frequências dentro do período do curso (entre `data_inicio` e `data_fim`).
    - Agrupa os resultados por aluno e turma e filtra apenas os alunos com três ou mais dias de atraso.
    
    c. **Consulta Final:**
    
    - Seleciona o nome do aluno, a turma, e o total de atrasos a partir da subconsulta `atrasos_aluno`.
    - Ordena os resultados pelo nome do aluno.
    
3. **Extração dos Dados:**
    - A função executa a consulta e obtém os resultados com `cursor.fetchall()`.
    
4. **Estruturação dos Dados:**
    - Os resultados da consulta são convertidos em uma lista de dicionários (`alunos_notificados`) para facilitar a renderização no template.
    - Também é calculada uma flag `tem_notificacoes` para verificar se há notificações a serem exibidas.
    
5. **Renderização do Template:**
    - Retorna o template `notificacoes.html` com o contexto:
        - `alunos_notificados`: Lista de alunos com três ou mais atrasos.
        - `tem_notificacoes`: Indica se há notificações disponíveis.


### <span style="color: #9A2EFE;">Lógica de Adicionar curso</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A view `criar_cursos` tem o objetivo de permitir a criação de cursos no sistema a partir de um arquivo CSV enviado pelo usuário. Ela processa o arquivo CSV, valida as informações e cria os cursos no banco de dados.

```python
@login_required
def criar_cursos(request):

        if request.method == 'POST' and 'cursos' in request.FILES:
            csv_file = request.FILES['cursos']
            
            fs = FileSystemStorage()
            filename = fs.save(csv_file.name, csv_file)

            with open(fs.path(filename), newline='', encoding='ISO-8859-1') as csvfile:
                reader = csv.reader(csvfile, delimiter=';')

                for row in reader:
                    try:
                        if Curso.objects.filter(turma=row[0], nome_curso=row[1]).exists():
                            print(f"Curso já existe: {row[0]}, {row[1]}")
                            continue

                        dias = [dia.strip() for dia in row[6].split(',')]
                        data_inicio = datetime.strptime(row[7], '%d/%m/%Y').date()
                        data_fim = datetime.strptime(row[8], '%d/%m/%Y').date()

                        Curso.objects.create(
                            turma=row[0],
                            nome_curso=row[1],
                            horario_entrada=row[2],
                            horario_saida=row[3],
                            carga_horaria=row[4],
                            responsavel=row[5],
                            dias_funcionamento=dias,
                            data_inicio=data_inicio,
                            data_fim=data_fim,
                            carga_horaria_intervalo=row[9],
                            dias_letivos=row[10]
                        )
                    except (IndexError, ValueError) as e:
                        print(f"Linha mal formatada ou erro: {row}, Erro: {e}")

            messages.success(request, "Cursos criados com sucesso.")
            return redirect("cursos")
        
        return render(request, 'criar_curso.html')
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Informações**

1. **Método de Requisição**:
    - A view trata requisições `POST` com arquivos (`multipart/form-data`), ou seja, o usuário envia um arquivo CSV através de um formulário.
2. **Validação do Arquivo**:
    - O arquivo enviado é lido como CSV, utilizando o delimitador `;` para separar os campos das linhas.
    - Para cada linha do CSV, o sistema tenta extrair informações como turma, nome do curso, horários e datas.
3. **Verificação de Cursos Existentes**:
    - Antes de criar um novo curso, o sistema verifica se já existe um curso com a mesma **turma** e **nome do curso**. Se já existir, ele ignora a linha e passa para a próxima.
4. **Criação de Curso**:
    - Caso a linha seja válida, o curso é criado no banco de dados com os campos extraídos do CSV.
    - Além disso, a data de início e de fim do curso são convertidas para o formato adequado, e os dias de funcionamento são divididos e armazenados.
5. **Exceções**:
    - Se ocorrer algum erro no processo de criação (como erro de formatação ou dados inválidos), o sistema captura e registra o erro, mas não interrompe o processamento do arquivo.
6. **Respostas ao Usuário**:
    - Se os cursos forem criados com sucesso, o sistema exibe uma mensagem de sucesso e redireciona o usuário para a lista de cursos.
    - Caso contrário, uma mensagem de erro será exibida.
    

**Decoradores**

- **`@login_required`:**
    - Garante que apenas usuários autenticados possam acessar esta funcionalidade. Se o usuário não estiver autenticado, ele será redirecionado para a página de login.

**Fluxo da Função**

1. **Verificação de Método e Arquivo:**
    - Confere se a requisição é do tipo `POST` e se contém um arquivo chamado `cursos` enviado pelo usuário.
    - Se essas condições forem verdadeiras, o arquivo CSV será processado.
2. **Armazenamento do Arquivo:**
    - Utiliza `FileSystemStorage` para salvar o arquivo enviado no sistema de arquivos local. Isso permite acessar o conteúdo do arquivo durante o processamento.
3. **Leitura do Arquivo CSV:**
    - O arquivo CSV salvo é aberto com `open()` usando codificação `ISO-8859-1` para evitar problemas de compatibilidade com caracteres especiais.
    - O leitor de CSV (`csv.reader`) interpreta o conteúdo do arquivo, separando as colunas por `;`.
4. **Processamento das Linhas:**
    - Para cada linha do arquivo CSV, tenta-se:
        - **Evitar duplicatas:** Verifica se já existe um registro com a mesma turma e nome de curso. Se existir, a linha é ignorada.
        - **Conversões necessárias:**
            - Divide os dias de funcionamento por vírgula e remove espaços.
            - Converte as datas de início e fim para objetos `datetime.date` com o formato esperado (`%d/%m/%Y`).
        - **Criação de Registro:**
            - Se não houver problemas, um novo curso é criado com os dados fornecidos.
5. **Tratamento de Erros:**
    - Se houver problemas, como índices fora de alcance (`IndexError`) ou falhas na conversão de dados (`ValueError`), esses erros são capturados e exibidos no console para depuração, mas o processamento continua para as próximas linhas.
6. **Mensagem de Sucesso:**
    - Após processar o arquivo, exibe uma mensagem de sucesso na interface do usuário usando `messages.success`.
7. **Redirecionamento:**
    - Após a criação bem-sucedida dos cursos, o usuário é redirecionado para a página "cursos".
8. **Renderização:**
    - Se o método de requisição não for `POST`, ou se nenhum arquivo for enviado, renderiza um template chamado `criar_curso.html` para o usuário carregar um novo arquivo.


### <span style="color: #9A2EFE;">Lógica de Deletar Curso</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A view `delete_curso` tem como objetivo permitir a exclusão de um curso específico e todos os alunos associados a ele. A view recebe a turma como parâmetro e, após a confirmação de que o usuário tem as permissões necessárias, exclui o curso e todos os alunos associados a ele.

```python
@login_required
def delete_curso(request, turma):
    curso = get_object_or_404(Curso, turma=turma) 
    alunos = curso.aluno_set.all()  

    if not request.user.is_superuser:
        messages.error(request, "Você não tem permissão para acessar essa página.")
        return redirect('cursos')

    if request.method == 'POST':
        Frequencia.objects.filter(id_aluno__in=alunos).delete()
        alunos.delete()
        curso.delete()

        messages.success(request, "Curso e alunos associados excluídos com sucesso.")
        return redirect('cursos')
    
    else:
        messages.error(request, "Erro ao excluir curso.")

    context = {'curso': curso, 'alunos': alunos}
    return render(request, 'alunos.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Funcionamento:**

1. **Método de Requisição**:
    - A view trata requisições `POST` para confirmar a exclusão do curso e seus alunos. Se a requisição não for `POST`, uma mensagem de erro é exibida.
2. **Autenticação e Permissões**:
    - O sistema verifica se o usuário é um superusuário (administrador) para permitir a exclusão do curso. Caso contrário, a ação é impedida e uma mensagem de erro é exibida.
3. **Verificação de Existência do Curso**:
    - O sistema tenta localizar o curso com base na **turma** fornecida. Se o curso não for encontrado, será gerado um erro 404.
4. **Exclusão de Curso e Alunos**:
    - Caso o curso seja encontrado, o sistema localiza todos os alunos associados a esse curso e os exclui.
    - O sistema também remove os registros de frequência dos alunos excluídos.
    - Após excluir todos os alunos e registros de frequência, o curso é excluído.
5. **Respostas ao Usuário**:
    - Se a exclusão for bem-sucedida, o sistema exibe uma mensagem de sucesso e redireciona o usuário para a lista de cursos.
    - Caso contrário, uma mensagem de erro será exibida.

#### <span style="color: #AC58FA;">***Fluxo Detalhado da Função***</span>

1. **Autenticação Obrigatória (`@login_required`):**
    - A função só pode ser acessada por usuários autenticados. Caso contrário, o usuário será redirecionado para a página de login.
2. **Busca do Curso pelo `turma`:**
    - Usa `get_object_or_404` para buscar um curso específico com base no identificador `turma`.
    - Caso o curso não seja encontrado, retorna uma página de erro 404 automaticamente.
3. **Busca dos Alunos Associados:**
    - Recupera todos os alunos relacionados ao curso usando o relacionamento reverso (`aluno_set.all()`).
4. **Verificação de Permissões:**
    - Apenas usuários com status de superusuário (`is_superuser`) têm permissão para excluir o curso e os alunos associados.
    - Se o usuário não for um superusuário:
        - Uma mensagem de erro é exibida ao usuário com `messages.error`.
        - O sistema redireciona para a página de cursos.
5. **Exclusão do Curso e Dados Relacionados (Método `POST`):**
    - Verifica se a requisição é do tipo `POST` para confirmar a exclusão.
    - Se confirmado:
        - Exclui os registros de frequência associados aos alunos do curso usando o filtro `Frequencia.objects.filter(id_aluno__in=alunos).delete()`.
        - Exclui os alunos associados ao curso com `alunos.delete()`.
        - Exclui o curso em si com `curso.delete()`.
        - Exibe uma mensagem de sucesso ao usuário com `messages.success`.
        - Redireciona para a página de cursos.
6. **Erro no Método Diferente de `POST`:**
    - Se o método da requisição não for `POST`, exibe uma mensagem de erro indicando que a exclusão falhou.
7. **Renderização de Template:**
    - Caso a exclusão não seja realizada ou seja apenas visualização, renderiza um template `alunos.html`, passando o curso e seus alunos como contexto.


### <span style="color: #9A2EFE;">Lógica de Adicionar Aluno</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A view `criar_alunos` tem como objetivo permitir o cadastro em massa de alunos no sistema a partir de um arquivo CSV enviado pelo usuário. Ela processa o arquivo CSV, valida as informações e cria os alunos no banco de dados.

```python
@login_required
def criar_alunos(request):

        if request.method == 'POST' and 'alunos' in request.FILES:
            csv_file = request.FILES['alunos']

            fs = FileSystemStorage()
            filename = fs.save(csv_file.name, csv_file)

            with open(fs.path(filename), newline='', encoding='ISO-8859-1') as csvfile:
                reader = csv.reader(csvfile, delimiter=';')  

                for row in reader:
                    try:
                        nome = row[0].strip()
                        
                        # Verifica se id_carteirinha não está vazio e é um número
                        if row[1].strip().isdigit():
                            id_carteirinha = int(row[1].strip())
                        else:
                            print(f"ID da carteirinha inválido para o aluno '{nome}'. Verifique o arquivo CSV.")
                            continue  # Pula para o próximo registro se o id_carteirinha estiver inválido

                        curso_id = row[2].strip()
                        
                        # Verifica se o curso existe
                        try:
                            curso = Curso.objects.get(turma=curso_id)
                        except Curso.DoesNotExist:
                            print(f"Curso com turma '{curso_id}' não encontrado para o aluno '{nome}'. Verifique o arquivo CSV.")
                            continue  # Pula este registro e continua com o próximo

                        # Verifica se o aluno já existe
                        if Aluno.objects.filter(id_carteirinha=id_carteirinha).exists():
                            print(f"Aluno com ID de carteirinha '{id_carteirinha}' já existe. Ignorando...")
                            continue  # Ignora este registro e continua com o próximo

                        # Criação do aluno
                        Aluno.objects.create(
                            nome=nome,
                            id_carteirinha=id_carteirinha,
                            id_curso=curso
                        )
                    except IndexError:
                        print("Erro: O arquivo CSV está com formato incorreto.")
                        return redirect("criar_aluno")

            messages.success(request, "Alunos criados com sucesso.")
            return redirect("cursos")

        return render(request, 'criar_aluno.html')
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Funcionamento:**

1. **Método de Requisição**:
    - A view trata requisições `POST` com arquivos (`multipart/form-data`), ou seja, o usuário envia um arquivo CSV através de um formulário.
2. **Validação do Arquivo**:
    - O arquivo enviado é lido como CSV, utilizando o delimitador `;` para separar os campos das linhas.
    - Para cada linha do CSV, o sistema tenta extrair informações como nome do aluno, ID da carteirinha e o curso (identificado pela turma).
3. **Verificação de Alunos Existentes**:
    - Antes de criar um novo aluno, o sistema verifica se já existe um aluno com o mesmo **ID de carteirinha**. Se já existir, ele ignora a linha e passa para a próxima.
    - O sistema também verifica se o curso informado existe no banco de dados. Se o curso não for encontrado, o registro do aluno será ignorado.
4. **Criação de Aluno**:
    - Caso a linha seja válida, o aluno é criado no banco de dados com os campos extraídos do CSV.
5. **Exceções**:
    - Se ocorrer algum erro no processo de leitura ou validação (como erro de formatação ou dados inválidos), o sistema captura e registra o erro, mas não interrompe o processamento do arquivo.
6. **Respostas ao Usuário**:
    - Se os alunos forem criados com sucesso, o sistema exibe uma mensagem de sucesso e redireciona o usuário para a lista de cursos.
    - Caso contrário, uma mensagem de erro será exibida.

#### <span style="color: #AC58FA;">***Fluxo Detalhado da Função***</span>

1. **Autenticação:**
    - O decorator `@login_required` garante que apenas usuários autenticados podem acessar essa funcionalidade.
2. **Manipulação de Requisição POST:**
    - A função verifica se a requisição é do tipo `POST` e se o arquivo CSV está presente no campo `'alunos'`.
3. **Armazenamento Temporário do Arquivo:**
    - O arquivo CSV é salvo no sistema usando `FileSystemStorage` para manipulação posterior.
4. **Processamento do Arquivo CSV:**
    - O arquivo é aberto e lido linha por linha usando o módulo `csv`.
    - O delimitador `;` é utilizado para separar os campos, e a codificação é definida como `ISO-8859-1` para lidar com caracteres especiais.
5. **Validação e Criação dos Registros:**
Para cada linha do arquivo CSV:
    - **Nome do Aluno:**
        - O primeiro campo é tratado como o nome do aluno e é "limpo" com `.strip()` para remover espaços em branco.
    - **ID da Carteirinha:**
        - Verifica se o campo não está vazio e é numérico.
        - Se for inválido, o registro é ignorado, e uma mensagem é exibida no console.
    - **Curso:**
        - O campo do curso é usado para buscar a instância correspondente na tabela de cursos.
        - Se o curso não existir, o registro é ignorado.
    - **Duplicidade:**
        - Verifica se já existe um aluno com o mesmo `id_carteirinha`. Se sim, o registro é ignorado.
    - **Criação do Aluno:**
        - Caso todas as validações passem, o aluno é criado com os dados fornecidos.
6. **Mensagens ao Usuário:**
    - Após o processamento, uma mensagem de sucesso é exibida ao usuário via `messages.success`.
7. **Redirecionamento:**
    - O usuário é redirecionado para a página de cursos após o processamento.
8. **Renderização do Template:**
    - Caso a requisição seja `GET`, o formulário para upload do arquivo CSV é exibido.


### <span style="color: #9A2EFE;">**Lógica de Deletar Aluno**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A view `delete_aluno` tem como objetivo permitir a exclusão de um aluno específico no sistema. Ela recebe como parâmetros a turma e o ID da carteirinha do aluno, verifica as permissões do usuário e, se autorizado, exclui o aluno do banco de dados.

```python
@login_required
def delete_aluno(request, turma, id_carteirinha):
    curso = get_object_or_404(Curso, turma=turma)
    aluno = get_object_or_404(Aluno, id_carteirinha=id_carteirinha)
    
    if not request.user.is_superuser:
        messages.error(request, "Você não tem permissão para acessar essa página.")
        return redirect('/')
    
    if request.method == 'POST':
        aluno.delete()
        messages.success(request, "Aluno excluído com sucesso.")
        return redirect('cursos')
    else:
        messages.error(request, "Erro ao excluir aluno.")

    context = {
        'curso': curso,
        'aluno': aluno,
    }
    return render(request, 'alunos.html', context)

```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Funcionamento:**

1. **Método de Requisição**:
    - A view trata requisições `POST` para confirmar a exclusão do aluno. Se a requisição for diferente, uma mensagem de erro será exibida.
2. **Autenticação e Permissões**:
    - O sistema verifica se o usuário é um superusuário (administrador) para permitir a exclusão do aluno. Caso contrário, o sistema impede a ação e exibe uma mensagem de erro.
3. **Verificação de Existência de Aluno**:
    - O sistema tenta localizar o aluno com base no `id_carteirinha` e no código da turma. Se o aluno não for encontrado, um erro 404 será gerado.
4. **Exclusão de Aluno**:
    - Caso o aluno seja encontrado, ele é excluído do banco de dados com o método `aluno.delete()`.
5. **Respostas ao Usuário**:
    - Se a exclusão for bem-sucedida, o sistema exibe uma mensagem de sucesso e redireciona o usuário para a lista de cursos.
    - Caso contrário, se ocorrer algum erro durante o processo, uma mensagem de erro será exibida.

#### <span style="color: #AC58FA;">***Fluxo Detalhado da Função***</span>

1. **Autenticação:**
    - O decorator `@login_required` garante que apenas usuários autenticados podem acessar a funcionalidade.
2. **Busca dos Registros:**
    - O curso é buscado usando `get_object_or_404` com base no identificador `turma`.
    - O aluno é buscado pelo número de carteirinha (`id_carteirinha`) usando também `get_object_or_404`.
3. **Verificação de Permissão:**
    - Apenas usuários com permissão de superusuário (`request.user.is_superuser`) podem executar a ação de exclusão.
    - Caso o usuário não seja superusuário, uma mensagem de erro é exibida via `messages.error`, e ele é redirecionado para a página inicial (`'/'`).
4. **Processamento de Requisição POST:**
    - Se o método da requisição for `POST`, o registro do aluno é excluído.
    - Após a exclusão, uma mensagem de sucesso é exibida com `messages.success`.
    - O usuário é redirecionado para a página de cursos (`'cursos'`).
5. **Requisição GET ou Falha na Exclusão:**
    - Caso a requisição não seja do tipo `POST`, ou ocorra algum erro, uma mensagem de erro é exibida.
    - As informações do curso e do aluno são passadas para o contexto para exibição na página `'alunos.html'`.
6. **Renderização do Template:**
    - Renderiza o template `alunos.html` com informações do aluno e do curso, permitindo exibir detalhes ao usuário antes de tomar a ação.


### <span style="color: #9A2EFE;">Lógica de cadastro</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `cadastro` é responsável por gerenciar o cadastro de novos usuários no sistema. Ela permite que um usuário crie uma conta com um nome, sobrenome, nome de usuário e senha. O usuário criado será automaticamente atribuído ao grupo "COORDENAÇÃO", e um registro adicional será criado na tabela `Usuario` com o cargo de "COORDENAÇÃO". Caso o nome de usuário já exista no banco de dados, uma mensagem de erro será exibida.

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def cadastro(request):
    context = {}

    if request.user.groups.filter(name='COORDENAÇÃO').exists():
        messages.error(request, "Você não tem permissão para acessar essa página.")
        return redirect('/')

    else:
        if request.method == "POST":
            form = FormCadastro(request.POST)
            if form.is_valid():
                var_nome = form.cleaned_data['nome']
                var_sobrenome = form.cleaned_data['sobrenome']
                var_username = form.cleaned_data['username']
                var_senha = form.cleaned_data['senha']

                try:
                    user = User.objects.create_user(username=var_username, password=var_senha)
                    user.first_name = var_nome
                    user.last_name = var_sobrenome
                    user.save()

                    coordenacao_group = Group.objects.get(name='COORDENAÇÃO')
                    user.groups.add(coordenacao_group)

                    Usuario.objects.create(
                        nome=var_nome,
                        sobrenome=var_sobrenome,
                        username=var_username,
                        cargo="COORDENAÇÃO",
                    )
                    messages.success(request, "Usuário cadastrado.")
                    return redirect("cadastro")

                except IntegrityError:
                    messages.error(request, "Nome de usuário já existe. Por favor, escolha outro nome de usuário.")
                    context.update({"form": form})
                    return render(request, 'cadastro.html', context)
            else:
                context.update({"form": form})
                return render(request, 'cadastro.html', context)
        else:
            form = FormCadastro()

    context.update({"form": form})
    return render(request, 'cadastro.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Fluxo da Função**

1. **Autenticação e Controle de Cache:**
    - O decorator `@login_required` garante que apenas usuários autenticados podem acessar a página.
    - `@cache_control(no_cache=True, must_revalidate=True, no_store=True)` evita que o navegador armazene o cache da página, garantindo segurança e privacidade.
2. **Restrição para Grupo 'COORDENAÇÃO':**
    - Se o usuário autenticado pertence ao grupo "COORDENAÇÃO", ele é redirecionado para a página inicial com uma mensagem de erro: *"Você não tem permissão para acessar essa página."*
3. **Tratamento de Requisição POST:**
    - Se o método da requisição for `POST`, os dados do formulário (`FormCadastro`) são validados:
        - **Validação bem-sucedida:**
            - Os campos `nome`, `sobrenome`, `username`, e `senha` são extraídos.
            - Um novo usuário é criado com `User.objects.create_user`.
            - O nome e sobrenome são atribuídos aos campos `first_name` e `last_name` do objeto `User`.
            - O usuário é associado ao grupo "COORDENAÇÃO".
            - Um registro adicional é criado na tabela `Usuario` com informações complementares.
            - Uma mensagem de sucesso é exibida: *"Usuário cadastrado."*
            - O usuário é redirecionado para a mesma página de cadastro.
        - **Erro de Integridade:**
            - Caso o nome de usuário já exista, é exibida a mensagem: *"Nome de usuário já existe. Por favor, escolha outro nome de usuário."*
            - O formulário preenchido é retornado ao template.
4. **Requisição GET:**
    - Se a requisição for `GET`, um formulário vazio (`FormCadastro`) é inicializado.
5. **Contexto e Renderização:**
    - O formulário é enviado ao template `cadastro.html` para renderização.

### <span style="color: #9A2EFE;">**Lógica para Listagem dos Alunos e Informações de Frequência**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `alunos` é responsável por gerar uma visão detalhada sobre a frequência dos alunos de um determinado curso e turma. Ela calcula e exibe informações como faltas, atrasos, presenças, carga horária cumprida e porcentagem de frequência de cada aluno, considerando os dados de frequência armazenados no banco de dados. As informações são calculadas por meio de uma consulta SQL complexa que analisa as entradas e saídas dos alunos, incluindo considerações sobre horários de entrada, saída e intervalos. O resultado é apresentado em uma página de detalhes dos alunos.

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def alunos(request, turma):
    curso = get_object_or_404(Curso, turma=turma)

    with connection.cursor() as cursor:
        cursor.execute("""
            WITH frequencias_calculadas AS (
                SELECT 
                    f.id_aluno_id,
                    f.data,
                    f.hora,
                    LEAD(f.hora) OVER (PARTITION BY f.id_aluno_id, f.data ORDER BY f.hora) AS proxima_hora,
                    CAST(f.identificador AS INTEGER) AS identificador,
                    CASE 
                        WHEN CAST(f.identificador AS INTEGER) = 2 
                        AND NOT EXISTS (
                            SELECT 1
                            FROM web_frequencia f2 
                            WHERE f2.id_aluno_id = f.id_aluno_id 
                            AND f2.data = f.data 
                            AND CAST(f2.identificador AS INTEGER) = 1
                        ) THEN true
                        ELSE false
                    END AS apenas_saida
                FROM 
                    web_frequencia AS f
            ),
            presenca_por_dia AS (
                SELECT 
                    aluno.id_carteirinha,
                    f.data,
                    CASE 
                        WHEN f.apenas_saida THEN
                            EXTRACT(EPOCH FROM (
                                f.hora - c.horario_entrada
                            )) / 3600.0
                            - 
                            EXTRACT(EPOCH FROM c.carga_horaria_intervalo) / 3600.0
                        WHEN CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN
                            CASE 
                                WHEN f.hora IS NULL THEN 0
                                ELSE
                                    EXTRACT(EPOCH FROM LEAST(
                                        COALESCE(f.proxima_hora, c.horario_saida),
                                        c.horario_saida
                                    ) - 
                                    GREATEST(
                                        f.hora,
                                        c.horario_entrada
                                    )) / 3600.0
                                    - 
                                    EXTRACT(EPOCH FROM c.carga_horaria_intervalo) / 3600.0
                            END
                        ELSE 0
                    END AS horas_presenca,
                    CASE 
                        WHEN f.id_aluno_id IS NULL THEN 1
                        WHEN f.apenas_saida THEN 0         
                        WHEN f.hora IS NULL AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN 1 
                        ELSE 0 
                    END AS teve_falta,
                    CASE 
                        WHEN f.apenas_saida THEN 0
                        WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN 1 
                        ELSE 0 
                    END AS teve_atraso,
                    CASE 
                        WHEN CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 
                            OR CAST(COALESCE(f.identificador, 0) AS INTEGER) = 2
                            OR f.apenas_saida
                            OR f.hora IS NOT NULL
                        THEN 1
                        ELSE 0
                    END AS presenca
                FROM 
                    web_aluno AS aluno
                CROSS JOIN
                    web_curso AS c 
                LEFT JOIN 
                    frequencias_calculadas AS f ON aluno.id_carteirinha = f.id_aluno_id
                    AND f.data BETWEEN c.data_inicio AND c.data_fim
                WHERE 
                    c.turma = %s
            ),
            totais_aluno AS (
                SELECT 
                    aluno.id_carteirinha,
                    COALESCE(SUM(p.horas_presenca), 0) AS total_horas_presenca,
                    COALESCE(COUNT(DISTINCT CASE WHEN p.teve_atraso = 1 THEN p.data END), 0) AS total_atrasos,
                    COALESCE(COUNT(DISTINCT CASE WHEN p.presenca = 1 THEN p.data END), 0) AS total_presencas
                FROM 
                    web_aluno AS aluno
                LEFT JOIN 
                    presenca_por_dia AS p ON aluno.id_carteirinha = p.id_carteirinha
                WHERE
                    aluno.id_curso_id = %s
                GROUP BY 
                    aluno.id_carteirinha
            )
            SELECT 
                aluno.id_carteirinha,
                aluno.nome,
                GREATEST(c.dias_letivos - t.total_presencas, 0) AS total_faltas,  -- Atualizado para calcular total_faltas
                t.total_atrasos,
                t.total_presencas,
                LEAST(t.total_horas_presenca, 600) AS carga_horaria_cumprida,
                CASE 
                    WHEN c.dias_letivos > 0 THEN 
                        LEAST(100, ROUND((LEAST(t.total_horas_presenca, 600) / (c.dias_letivos * 7.5)) * 100, 2))
                    ELSE 0
                END AS porcentagem_frequencia
            FROM 
                web_aluno AS aluno
            JOIN 
                totais_aluno AS t ON aluno.id_carteirinha = t.id_carteirinha
            JOIN 
                web_curso AS c ON aluno.id_curso_id = c.turma
            WHERE 
                c.turma = %s
            ORDER BY 
                aluno.nome;
        """, [curso.turma, curso.turma, curso.turma])

        resultados = cursor.fetchall()

    alunos_detalhes = []
    for resultado in resultados:
        alunos_detalhes.append({
            'id_carteirinha': resultado[0],
            'aluno': resultado[1],
            'faltas': resultado[2],
            'atrasos': resultado[3],
            'presencas': resultado[4],
            'carga_horaria_aluno': resultado[5],
            'porcentagem_carga_horaria': round(resultado[6], 2),
        })

    context = {
        'curso': curso,
        'alunos_detalhes': alunos_detalhes,
    }

    return render(request, 'alunos.html', context)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Funcionamento**

1. **Requer Login:**
    - O decorator `@login_required` impede que usuários não autenticados acessem a página.
2. **Controle de Cache:**
    - `@cache_control(no_cache=True, must_revalidate=True, no_store=True)` evita cache da página, garantindo que os dados exibidos estejam sempre atualizados.
3. **Busca do Curso:**
    - A função utiliza `get_object_or_404` para buscar o curso pela turma. Caso o curso não seja encontrado, retorna uma página de erro 404.
4. **Consulta SQL Avançada:**
    - Usa a funcionalidade de CTEs (Common Table Expressions) para estruturar a consulta:
        - **`frequencias_calculadas`:**
            - Gera dados sobre cada entrada de frequência, incluindo a próxima hora de entrada e se há apenas registro de saída sem entrada.
        - **`presenca_por_dia`:**
            - Calcula as horas de presença, verifica se houve faltas ou atrasos, e identifica registros de presença por dia.
        - **`totais_aluno`:**
            - Resume as informações por aluno, como total de horas de presença, atrasos e presenças.
    - A consulta final retorna:
        - ID do aluno.
        - Nome do aluno.
        - Total de faltas.
        - Total de atrasos.
        - Total de presenças.
        - Carga horária cumprida (limitada a 600 horas).
        - Porcentagem de frequência (baseada em 7,5 horas por dia letivo).
5. **Manipulação dos Resultados:**
    - Os resultados da consulta SQL são armazenados em `resultados`.
    - Cada registro é processado para criar um dicionário com os dados relevantes para o aluno, que são armazenados na lista `alunos_detalhes`.
6. **Contexto e Renderização:**
    - Um dicionário `context` é criado com:
        - Informações do curso (`curso`).
        - Detalhes dos alunos (`alunos_detalhes`).
    - O contexto é passado para o template `alunos.html`.


### <span style="color: #9A2EFE;">**Lógica de Listar Cursos**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `cursos` é responsável por exibir informações detalhadas sobre os cursos de uma instituição, permitindo a pesquisa por nome do curso, turma ou aluno. Ela também realiza o cálculo de atrasos de alunos, apresentando notificações para os casos em que os alunos acumulam três ou mais atrasos. Além disso, a função permite o gerenciamento eficiente de cache, garantindo que os dados exibidos estejam sempre atualizados. O resultado é apresentado em uma página de cursos, onde o usuário pode visualizar os cursos filtrados e as notificações de atrasos dos alunos.

```python
@login_required
@cache_control(no_cache=True, must_revalidate=True, no_store=True)
def cursos(request):
    search_query = request.GET.get('search', '')

    if search_query:
        cursos = Curso.objects.filter(
            nome_curso__icontains=search_query
        ) | Curso.objects.filter(
            turma__icontains=search_query
        ) | Curso.objects.filter(
            aluno__nome__icontains=search_query
        )
        cursos = cursos.distinct()  # Remove duplicatas
    else:
        cursos = Curso.objects.all()

    form = FormPesquisa(initial={'search': search_query})

    with connection.cursor() as cursor:
        cursor.execute("""
            WITH frequencias_calculadas AS (
                SELECT 
                    f.id_aluno_id,
                    f.data,
                    f.hora,
                    LEAD(f.hora) OVER (PARTITION BY f.id_aluno_id, f.data ORDER BY f.hora) AS proxima_hora,
                    CAST(f.identificador AS INTEGER) AS identificador,
                    CASE 
                        WHEN CAST(f.identificador AS INTEGER) = 2 
                        AND NOT EXISTS (
                            SELECT 1
                            FROM web_frequencia f2 
                            WHERE f2.id_aluno_id = f.id_aluno_id 
                            AND f2.data = f.data 
                            AND CAST(f2.identificador AS INTEGER) = 1
                        ) THEN true
                        ELSE false
                    END as apenas_saida
                FROM 
                    web_frequencia AS f
            ),
            atrasos_aluno AS (
                SELECT 
                    aluno.id_carteirinha,
                    aluno.nome,
                    c.turma,
                    COUNT(DISTINCT CASE WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN f.data END) AS total_atrasos
                FROM 
                    web_aluno AS aluno
                JOIN 
                    web_curso AS c ON aluno.id_curso_id = c.turma
                LEFT JOIN 
                    frequencias_calculadas AS f ON aluno.id_carteirinha = f.id_aluno_id
                    AND f.data BETWEEN c.data_inicio AND c.data_fim
                GROUP BY 
                    aluno.id_carteirinha, aluno.nome, c.turma
                HAVING 
                    COUNT(DISTINCT CASE WHEN f.hora > c.horario_entrada + INTERVAL '10 minutes' AND CAST(COALESCE(f.identificador, 0) AS INTEGER) = 1 THEN f.data END) >= 3
            )
            SELECT 
                nome,
                turma,
                total_atrasos
            FROM 
                atrasos_aluno
            ORDER BY 
                nome;
        """)

        notificacoes = cursor.fetchall()
    
    tem_notificacoes = len(notificacoes) > 0

    return render(request, 'cursos.html', {
        'form': form,
        'cursos': cursos,
        'tem_notificacoes': tem_notificacoes
    })

```
#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Fluxo da Função**

**1. Busca de Cursos**

O primeiro bloco de código verifica se há uma consulta de pesquisa na URL (`search_query`).

- **Filtragem Condicional**:
    
    ```python
    cursos = Curso.objects.filter(
        nome_curso__icontains=search_query
    ) | Curso.objects.filter(
        turma__icontains=search_query
    ) | Curso.objects.filter(
        aluno__nome__icontains=search_query
    )
    ```
    
    - Busca cursos cujo nome, turma ou nome de aluno associado contenha o termo pesquisado.
    - O operador `|` (OR) combina os filtros, e `.distinct()` garante que os resultados não se repitam.
- **Caso não haja consulta**:
    
    ```python
    cursos = Curso.objects.all()
    ```
    
- Um formulário (`FormPesquisa`) é inicializado para manter o termo de busca na interface.

**2. Notificações de Atrasos**

- **Consulta SQL com `WITH`**:
A consulta SQL embutida calcula os atrasos por aluno:
    - **CTE `frequencias_calculadas`**: Processa a frequência por aluno, destacando registros como "apenas saída" ou atrasos (considerando horário de entrada com tolerância de 10 minutos).
    - **CTE `atrasos_aluno`**: Calcula o total de atrasos por aluno para cursos em que houve atrasos repetidos (>= 3).
    - **Consulta Final**:
        
        ```sql
        SELECT
            nome,
            turma,
            total_atrasos
        FROM
            atrasos_aluno
        ORDER BY
            nome;
        ```
        
        - Retorna a lista de alunos com atrasos recorrentes.
    - **Resultados**:
        
        ```python
        notificacoes = cursor.fetchall()
        tem_notificacoes = len(notificacoes) > 0
        ```


### <span style="color: #9A2EFE;">**Lógica Homepage**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `homepage` é responsável por exibir a página inicial do sistema. Caso o usuário já esteja autenticado, ele será redirecionado automaticamente para a página de cursos (`cursos`). Caso contrário, a função renderiza a página de entrada (`homepage.html`), permitindo que usuários não autenticados possam visualizar a página de boas-vindas.

```python
def homepage(request):
    if request.user.is_authenticated:
        return redirect('cursos')
    return render(request, 'homepage.html')
```

O método `homepage` é simples e funcional. Ele determina qual página será exibida com base no estado de autenticação do usuário.

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**1. Checagem de Autenticação**

```python
if request.user.is_authenticated:
    return redirect('cursos')
```

- O método `is_authenticated` verifica se o usuário atual está autenticado.
- Se o usuário estiver autenticado, ele será redirecionado para a página `cursos`.
    - O `redirect('cursos')` presume que há uma URL nomeada como `'cursos'` configurada no `urls.py`.
    

**2. Exibição da Página Inicial**

```python
return render(request, 'homepage.html')
```

- Se o usuário **não estiver autenticado**, a página inicial (`homepage.html`) será renderizada.


### <span style="color: #9A2EFE;">**Lógica de Nome de Usuário**</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

A função `nomeUsuario` é responsável por retornar o nome completo do usuário autenticado no sistema. Ela verifica o usuário autenticado por meio do nome de usuário (`username`) e recupera o objeto `Usuario` correspondente. O nome do usuário é então retornado.

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**1. Decorador**

```python
@login_required
```

- Assegura que apenas usuários autenticados possam acessar essa função.

**2. Obtenção do Usuário**

```python
usuario = Usuario.objects.get(username=request.user.username)
```

- Usa o modelo `Usuario` para buscar o objeto relacionado ao usuário autenticado. O `request.user.username` fornece o nome de usuário.

**3. Retorno**

```python
return usuario.nome
```

- Retorna diretamente o nome do usuário como resposta.

---

### <span style="color: #9A2EFE;">Lógicas do JavaScript</span>
#### Lógica de Exibição de Senha

A lógica para mostrar ou esconder a senha é implementada no arquivo `mostrar_senha.js`. Essa funcionalidade altera o tipo de um campo de senha de "password" para "text" e vice-versa, permitindo que o usuário visualize ou oculte a senha.

**Função:**

```jsx
function mostrar() {
    const senhaInput = document.querySelector('input[name="senha"]');
    const btnSenha = document.getElementById('btnSenha');

    if (senhaInput.type === 'password') {
        senhaInput.type = 'text';
        btnSenha.classList.remove('bi-eye-slash');
        btnSenha.classList.add('bi-eye');
    } else {
        senhaInput.type = 'password';
        btnSenha.classList.remove('bi-eye');
        btnSenha.classList.add('bi-eye-slash');
    }
}
```

Na função `mostrar()`, o código realiza a verificação do tipo do campo de senha (`senhaInput.type`) e altera o tipo entre "password" e "text". Também faz alterações nas classes CSS do botão (`btnSenha`), para mudar o ícone de olho, indicando se a senha está visível ou oculta.

#### Lógica de Mensagem de Erro

O arquivo `msg_erro.js` gerencia a exibição e o desaparecimento de mensagens de erro na interface do usuário. A funcionalidade é executada assim que o DOM estiver completamente carregado.

**Função de desaparecimento de mensagem de erro:**

```jsx
document.addEventListener("DOMContentLoaded", function () {
    const alertContainer = document.getElementById("alert-container");
    if (alertContainer) {
        setTimeout(() => {
            alertContainer.classList.add("fade-out-hidden");
        }, 3000);
    }
});
```

Dentro dessa função, o código aguarda o carregamento completo do DOM e, após 3 segundos, adiciona a classe `fade-out-hidden` ao elemento de alerta (`alert-container`). Isso resulta na ocultação gradual da mensagem de erro, que provavelmente foi estilizada para desaparecer de forma suave com transições CSS.

#### Lógica de Troca de Tema

A troca de tema, permitindo a alternância entre o modo claro e escuro, está implementada no arquivo `script.js`. Essa funcionalidade permite que o tema atual seja armazenado localmente e reaplicado sempre que a página for recarregada.

**Função de troca de tema:**

```jsx
document.addEventListener("DOMContentLoaded", function () {
    const themeToggleBtn = document.getElementById("theme-toggle");
    const themeIcon = document.getElementById("theme-icon");
    let currentTheme = localStorage.getItem("theme") || "light";

    document.documentElement.setAttribute("data-theme", currentTheme);
    themeIcon.classList.remove("bi-sun-fill", "bi-moon-fill");
    themeIcon.classList.add(currentTheme === "light" ? "bi-sun-fill" : "bi-moon-fill");

    themeToggleBtn.addEventListener("click", function () {
        currentTheme = currentTheme === "light" ? "dark" : "light";

        document.documentElement.setAttribute("data-theme", currentTheme);

        localStorage.setItem("theme", currentTheme);

        themeIcon.classList.remove("bi-sun-fill", "bi-moon-fill");
        themeIcon.classList.add(currentTheme === "light" ? "bi-sun-fill" : "bi-moon-fill");
    });
});
```

A lógica de troca de tema funciona da seguinte forma:

1. Ao carregar a página, o tema atual é recuperado do `localStorage`, ou o padrão "light" é aplicado caso não haja tema salvo.
2. O atributo `data-theme` do elemento `<html>` é alterado para aplicar o tema selecionado (claro ou escuro).
3. O ícone de tema (um ícone de sol ou lua) é ajustado conforme o tema atual.
4. Ao clicar no botão de alternância (`theme-toggle`), o tema é alterado entre "light" e "dark", e o novo valor é salvo no `localStorage`.

#### Lógica de Pesquisa com Animação

No arquivo `search_transição.js`, a lógica lida com a exibição e ocultação da barra de pesquisa, além de aplicar uma transição suave.

**Função de exibição e ocultação da barra de pesquisa:**

```jsx
document.addEventListener('DOMContentLoaded', function () {
    const searchIcon = document.getElementById('search-icon');
    const searchContainer = document.getElementById('search-container');

    if (searchIcon && searchContainer) {
        searchIcon.addEventListener('click', function () {
            searchContainer.classList.toggle('visible');
            if (searchContainer.classList.contains('visible')) {
                setTimeout(() => {
                    const input = searchContainer.querySelector('input');
                    if (input) input.focus();
                }, 500);
            }
        });

        document.addEventListener('click', function (event) {
            if (
                !searchContainer.contains(event.target) &&
                !searchIcon.contains(event.target)
            ) {
                searchContainer.classList.remove('visible');
            }
        });
    }
});
```

O código executa as seguintes ações:

1. Ao clicar no ícone de pesquisa (`search-icon`), a classe `visible` é alternada no contêiner de pesquisa (`search-container`), fazendo com que a barra de pesquisa apareça ou desapareça.
2. Se a barra de pesquisa se tornar visível, um `setTimeout` é usado para garantir que o foco seja dado ao campo de entrada (`input`) após meio segundo.
3. Caso o usuário clique fora do contêiner de pesquisa ou do ícone de pesquisa, a barra de pesquisa é ocultada, removendo a classe `visible`.


### <span style="color: #9A2EFE;">Lógica de Automação com o Selenium, PyAutoGui e Agendador de Tarefas</span>

#### <span style="color: #AC58FA;">***Descrição Geral***</span>

O código que abaixo implementa um processo automatizado para baixar arquivos de catraca, combiná-los, e inserir dados extraídos em um banco de dados PostgreSQL. Abaixo está uma explicação do que o código faz.

```python
import os
import re
import time
import pyautogui
import schedule
import psycopg2
from psycopg2 import sql
from datetime import datetime
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import TimeoutException

def executar_tarefa():
    # Diretório onde os arquivos serão baixados
    download_path = r'rota'

    # Nomes dos arquivos que devem ser verificados
    file1 = os.path.join(download_path, 'catraca 03.txt')
    file2 = os.path.join(download_path, 'catraca 04.txt')
    combined_file = os.path.join(download_path, 'catracas.txt')

    # Verificar e apagar os arquivos antigos, se existirem
    if os.path.exists(file1):
        print(f"Apagando arquivo antigo: {file1}")
        os.remove(file1)
    if os.path.exists(file2):
        print(f"Apagando arquivo antigo: {file2}")
        os.remove(file2)
    if os.path.exists(combined_file):
        print(f"Apagando arquivo antigo combinado: {combined_file}")
        os.remove(combined_file)

    # Configurar opções do Chfome (modo anônimo)
    chrome_options = Options()
    chrome_options.add_argument("--incognito")
    
    # Iniciar o navegador Chrome em modo anônimo
    nav = webdriver.Chrome(options=chrome_options)

    login = 'login'
    senha = 'senha'

    try:
        login_input = WebDriverWait(nav, 10).until(
            EC.presence_of_element_located((By.ID, 'lblLogin'))
        )
        login_input.send_keys(login)
    except TimeoutException:
        print("Elemento 'lblLogin' não encontrado no tempo esperado.")

##########################################################| catraca NÚMERO 03 |##################################################################################

    nav.get('url')
    time.sleep(5)

    # Login
    login_input = nav.find_element(By.ID, 'lblLogin')
    login_input.send_keys(login)
    time.sleep(3)

    senha_input = nav.find_element(By.ID, 'lblPass')
    senha_input.send_keys(senha)
    time.sleep(3)

    login_button = nav.find_element(By.LINK_TEXT, 'Entrar')
    login_button.click()
    time.sleep(3)

    # Botão dados
    botao_dados = nav.find_element(By.CSS_SELECTOR, "a[onclick='subComp(0, 8, 0);']")
    botao_dados.click()
    time.sleep(3)

    # Botão salvar
    botao_salvar = nav.find_element(By.PARTIAL_LINK_TEXT, "Salvar")
    botao_salvar.click()
    time.sleep(3)

    pyautogui.write('catraca 03')
    time.sleep(3)

    pyautogui.press('enter')
    time.sleep(120)

    sair = nav.find_element(By.XPATH, "//a[center[text()='Sair']]")
    sair.click()
    time.sleep(3)

##########################################################| catraca NÚMERO 04 |######################################################################################

    nav.get('url')
    time.sleep(5)

    # Login
    login_input = nav.find_element(By.ID, 'lblLogin')
    login_input.send_keys(login)
    time.sleep(3)

    senha_input = nav.find_element(By.ID, 'lblPass')
    senha_input.send_keys(senha)
    time.sleep(3)

    login_button = nav.find_element(By.LINK_TEXT, 'Entrar')
    login_button.click()
    time.sleep(5)

    # Botão dados
    botao_dados = nav.find_element(By.CSS_SELECTOR, "a[onclick='subComp(0, 8, 0);']")
    botao_dados.click()
    time.sleep(3)

    # Botão salvar
    botao_salvar = nav.find_element(By.PARTIAL_LINK_TEXT, "Salvar")
    botao_salvar.click()
    time.sleep(3)

    pyautogui.write('catraca 04')
    time.sleep(3)

    pyautogui.press('enter')
    time.sleep(120)

    sair = nav.find_element(By.XPATH, "//a[center[text()='Sair']]")
    sair.click()
    time.sleep(3)
  
    combined_file_path = unir_arquivos()
    print(f"Arquivo combinado disponível em: {combined_file_path}")
    filtrar()

##########################################################| catraca NÚMERO 02 |######################################################################################

    # nav.get('url')
    # time.sleep(5)

    # # Login
    # login_input = nav.find_element(By.ID, 'lblLogin')
    # login_input.send_keys(login)
    # time.sleep(3)

    # senha_input = nav.find_element(By.ID, 'lblPass')
    # senha_input.send_keys(senha)
    # time.sleep(3)

    # login_button = nav.find_element(By.LINK_TEXT, 'Entrar')
    # login_button.click()
    # time.sleep(3)

    # # Botão dados
    # botao_dados = nav.find_element(By.CSS_SELECTOR, "a[onclick='subComp(0, 8, 0);']")
    # botao_dados.click()
    # time.sleep(3)

    # # Botão salvar
    # botao_salvar = nav.find_element(By.PARTIAL_LINK_TEXT, "Salvar")
    # botao_salvar.click()
    # time.sleep(3)

    # pyautogui.write('catraca 04')
    # time.sleep(3)

    # pyautogui.press('enter')
    # time.sleep(34)

    # sair = nav.find_element(By.XPATH, "//a[center[text()='Sair']]")
    # sair.click()
    # time.sleep(3)

##########################################################| MANIPULAÇÃO DOS ARQUIVOS TXT |###########################################################################

def unir_arquivos():
    # Diretório onde os arquivos foram baixados
    download_path = r'c:\Users\Aluno\Downloads'

    # Nomes dos arquivos baixados
    file1 = os.path.join(download_path, 'catraca 03.txt')
    file2 = os.path.join(download_path, 'catraca 04.txt')
    combined_file = os.path.join(download_path, 'catracas.txt')

    try:
        # Verificar se os arquivos existem
        if os.path.exists(file1) and os.path.exists(file2):
            print("Arquivos encontrados, iniciando a combinação...")

            # Verificação do conteúdo dos arquivos
            with open(file1, 'r', encoding='utf-8') as f1, open(file2, 'r', encoding='utf-8') as f2:
                data1 = f1.readlines()
                data2 = f2.readlines()

                # Verificação do conteúdo de cada arquivo
                if not data1:
                    print(f"O arquivo {file1} está vazio ou não contém dados.")
                if not data2:
                    print(f"O arquivo {file2} está vazio ou não contém dados.")

                # Se ambos os arquivos tiverem conteúdo, combinar
                if data1 and data2:
                    # Concatenar as linhas de ambos os arquivos
                    combined_data = data1 + data2

                    # Escrever o resultado no arquivo final
                    output_file = os.path.join(download_path, 'catracas.txt')
                    with open(output_file, 'w', encoding='utf-8') as outfile:
                        outfile.writelines(combined_data)

                    print(f"Arquivos combinados e salvos em {output_file}")
                else:
                    print("Um dos arquivos está vazio. Verifique os dados antes de continuar.")
        else:
            print("Um ou ambos os arquivos não foram encontrados. Verifique os nomes e o diretório.")
    except Exception as e:
        print(f"Ocorreu um erro ao combinar os arquivos: {e}")
              
    return combined_file

##########################################################| Subir dados no Banco de Dados |##########################################################################

def filtrar():
    download_path = r'rota'
    arquivo_entrada = f'{download_path}\\catracas.txt'

    # parâmetros
    db_params = {
        'database': 'database',
        'user': 'user',
        'password': 'password',
        'host': 'host',
        'port': 0000
    }

    # IDs específicos para filtrar
    ids_selecionados = [
        '1',
        '2',
        '3',
        '4',
        '5',
        '6'
    ]

    # lista para armazenar os dados extraídos
    dados_extraidos = []

    # Faz a filtragem de texto pra capturar a data e o horário
    padrao_data_hora = re.compile(r'(\d{2}/\d{2}/\d{4} \d{2}:\d{2}:\d{2})')

    # lógica para abrir o arquivo e procurar pelas linhas que contenham os IDs
    with open(arquivo_entrada, 'r', encoding='utf-8') as file:
        linhas = file.readlines()
        for linha in linhas:
            for id in ids_selecionados:
                if id in linha:
                    # lógica para procurar a data e o horário na linha
                    match_data_hora = padrao_data_hora.search(linha)
                    if match_data_hora:
                        data_hora = match_data_hora.group(1)

                        # Pega o número (1 ou 2) que vem logo após a data/hora
                        pos_data_hora = match_data_hora.end()
                        numero = linha[pos_data_hora + 1]  # número referente a entrada e saída (1=entrada; 2=saída)

                        # Armazena os dados extraídos
                        dados_extraidos.append((id, data_hora.split()[0], data_hora.split()[1], numero))
                    break  # Se encontrar o ID, não precisa continuar procurando outros IDs na mesma linha

    # Verifica se encontrou alguma linha
    if dados_extraidos:
        conn = None  # Inicializa a conexão como None
        try:
            # Conecta ao banco de dados
            conn = psycopg2.connect(**db_params)
            cur = conn.cursor()

            # Cria a tabela se ela não existir
            cur.execute("""
                CREATE TABLE IF NOT EXISTS web_frequencia (
                    id SERIAL PRIMARY KEY,
                    data DATE,
                    id_aluno_id VARCHAR,
                    hora TIME,
                    identificador CHAR(1)
                )
            """)

            # Verifica se a tabela está vazia
            cur.execute("SELECT COUNT(*) FROM web_frequencia")
            count = cur.fetchone()[0]

            if count == 0:
                # Se a tabela estiver vazia, insere todos os dados
                insert_query = sql.SQL("""
                    INSERT INTO web_frequencia (id_aluno_id, data, hora, identificador)
                    VALUES (%s, %s, %s, %s)
                """)
                cur.executemany(insert_query, dados_extraidos)
                print("Tabela vazia. Todos os dados foram inseridos.")
            else:
                # Se a tabela não estiver vazia, insere apenas os novos dados
                for dado in dados_extraidos:
                    cur.execute("""
                        SELECT COUNT(*) FROM web_frequencia
                        WHERE id_aluno_id = %s AND data = %s AND hora = %s AND identificador = %s
                    """, dado)
                    if cur.fetchone()[0] == 0:
                        cur.execute("""
                            INSERT INTO web_frequencia (id_aluno_id, data, hora, identificador)
                            VALUES (%s, %s, %s, %s)
                        """, dado)
                print("Apenas os novos dados foram inseridos.")

            # Commita as mudanças e fechar a conexão
            conn.commit()
            print("Operação concluída com sucesso.")

        except (Exception, psycopg2.Error) as error:
            print(f"Erro ao conectar ao PostgreSQL: {error}")

        finally:
            # Fecha a conexão apenas se ela foi estabelecida corretamente
            if conn is not None:
                cur.close()
                conn.close()
                print("Conexão com o banco de dados fechada.")
    else:
        print("Nenhum dado correspondente foi encontrado.")

##########################################################| Agendamento de tarefas para rodar em horários específicos |###############################################

schedule.every().day.at("08:20").do(executar_tarefa)
schedule.every().day.at("13:00").do(executar_tarefa)
schedule.every().day.at("15:00").do(executar_tarefa)
schedule.every().day.at("18:00").do(executar_tarefa)

while True:
    schedule.run_pending()
    time.sleep(1)
```

#### <span style="color: #AC58FA;">***Explicação Detalhada***</span>

**Descrição do código**:

1. **Automação de navegação no navegador**:
    - Usa `selenium` para automatizar o login em uma página web e clicar em botões para baixar arquivos de catracas (`catraca 03` e `catraca 04`).
    - Após o login, o script navega e baixa os arquivos de dados das catracas e os salva com o nome correspondente utilizando o PyAutoGui.
2. **Manipulação de arquivos**:
    - Após o download dos arquivos, o script verifica se os arquivos existem, combina os dados de dois arquivos (`catraca 03.txt` e `catraca 04.txt`) em um único arquivo chamado `catracas.txt`.
    - Se algum dos arquivos não for encontrado ou estiver vazio, o código imprime uma mensagem de erro.
3. **Filtragem e inserção no banco de dados**:
    - O script lê o arquivo combinado, filtra as linhas que contêm IDs específicos e extrai as informações de data, hora e número de entrada/saída.
    - Ele então conecta a um banco de dados PostgreSQL e insere os dados extraídos na tabela `web_frequencia`.
    - Antes de inserir, ele verifica se os dados já existem na tabela para evitar duplicações.
4. **Agendamento de execução**:
    - Utiliza o módulo `schedule` para agendar a execução da função `executar_tarefa` em horários específicos (08:20, 13:00, 15:00, 18:00).

**Usando o Agendador de Tarefas:**

Para realizar o agendamento automático e executar o código que obterá o arquivo contendo os dados extraídos das catracas, foi optado pela utilização do Agendador de Tarefa do Windows, que, ao criar a tarefa, precisa definir informações básicas como nome, com qual condição será iniciada a tarefa e também sua data de início, horário e dias específicos que executará (dependendo da necessidade).

Na etapa da imagem abaixo, é definido quando iniciar a tarefa, sendo indicado o intervalo para a execução do tarefa, horário para a tarefa ser executada e/ou suas datas específicas de funcionamento:

<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/agendador_1.png" alt="Agendador de Tarefas - 1" width="45%">
</p>

Após isso, a ação que será realizada na tarefa agendada é escolhida, nesse caso sendo **iniciar um programa.** A tarefa executará um arquivo **.bat**, que informa onde o código principal será rodado (interpretador ou linguagem de programação) e o caminho do código a ser percorrido. Ao ser inciado, abrirá em segundo plano e executará o código python principal.

Na etapa da imagem abaixo, é definida a ação que a tarefa executará e caminho do programa/script a ser aberto:

<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/agendador_2.png" alt="Agendador de Tarefas - 2" width="45%">
</p>

**Observação: Todos os prints utilizados de exemplo foram extraídos de um teste para a utilização do agendador de tarefas no projeto.**


### <span style="color: #9A2EFE;">Testes de Software</span>
Os testes de software **são um processo fundamental no desenvolvimento de software, que visa verificar se o produto ou aplicativo cumpre o que se propõe**. Eles podem ser realizados em qualquer parte do software, desde a unidade até o funcionamento global, e são essenciais para evitar problemas e bugs.

Os benefícios de bons testes incluem: prevenir bugs, melhorar o desempenho, identificar e corrigir falhas e bugs, otimizar a gestão de recursos.

**Fluxos da aplicação testados**

- **Cadastro de Coordenador:** esta página deve estar visível apenas para o administrador. Deve ser inserida as informações para a criação do usuário (coordenador), clicar no botão de “Cadastrar” e, assim, o usuário é cadastrado pelo sistema no banco de dados.
- **Formulário de Login:** a partir da página inicial, deve ser acessada a página de Login. Deve-se realizar a verificação de se a página está acessível, inserir as credenciais para autenticação (válidas e inválidas para teste) e clicar no botão “Entrar”, realizando o login do usuário pelo sistema.

**Funções testadas**

- **Geração de relatório:** esta função deve realizar uma consulta no banco de dados para a geração do relatório, contendo os nomes dos alunos com mais faltas e atrasos, e a frequência total (%).
- **Exclusão de curso:** a partir da página de Cursos, deve ser acessada a página de Curso Teste e o deletar.
- **Cálculo de frequência:** esta função deve realizar uma consulta no documento das informações extraídas das catracas sobre entrada e saída de cada aluno. Deve calcular suas faltas, atrasos e a frequência total (%).

#### <span style="color: #AC58FA;">Resultados obtidos</span>

#### <span style="color: #AC58FA;">Testes Automatizados</span>

#### **Cadastro de Coordenador**

<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/teste_cadastro.png" alt="Teste de Cadastro" width="45%">
</p>

```javascript
describe('Testes da Página de Cadastro', () => {
  beforeEach(() => {
    // Acessa a página de login antes de cada teste
    cy.visit('http://127.0.0.1:8000/login');
  });

  it('deve carregar a página de login corretamente', () => {
    cy.title().should('contain', 'Controle de Frequência');
    cy.get('.titulo').should('be.visible').and('have.text', 'Fazer Login');
  });

  it('deve redirecionar para a página de cursos após login bem-sucedido', () => {
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();
    cy.url().should('include', '/cursos');
  });

  it('deve abrir o offcanvas e clicar no link de cadastro após login', () => {
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();
    cy.url().should('include', '/cursos');
    cy.get('.navbar-toggler').click();
    cy.get('.offcanvas').should('be.visible');
    cy.get('.nav-link').contains('Cadastro').click();
    cy.url().should('include', '/cadastro');
  });

  it('deve carregar os campos de cadastro corretamente', () => {
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();
    cy.url().should('include', '/cursos');
    cy.get('.navbar-toggler').click();
    cy.get('.offcanvas').should('be.visible');
    cy.get('.nav-link').contains('Cadastro').click();
    cy.get('h2.titulo').should('contain.text', 'Fazer Cadastro');
    cy.get('input[name="nome"]').should('exist');
    cy.get('input[name="sobrenome"]').should('exist');
    cy.get('input[name="username"]').should('exist');
    cy.get('input[name="senha"]').should('exist');
    cy.get('button[type="submit"]').should('contain.text', 'Cadastrar');
  });

  it('deve preencher e enviar o formulário de cadastro com sucesso', () => {
    // Gerar um nome de usuário único usando um timestamp ou UUID
    const username = `usuario_${Date.now()}`;
    const password = 'Senha123';
  
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();
    cy.url().should('include', '/cursos');
    cy.get('.navbar-toggler').click();
    cy.get('.offcanvas').should('be.visible');
    cy.get('.nav-link').contains('Cadastro').click();
  
    // Preencher os campos com dados dinâmicos
    cy.get('input[name="nome"]').type('Ruan');
    cy.get('input[name="sobrenome"]').type('silva');
    cy.get('input[name="username"]').type(username); // Nome de usuário único
    cy.get('input[name="senha"]').type(password);
  
    // Submeter o formulário
    cy.get('button[type="submit"]').click();
  
    // Verificar mensagem de sucesso
    cy.get('#alert-container')
      .should('be.visible')
      .and('contain.text', 'Usuário cadastrado.');
  });
  

  it('deve exibir mensagem de erro se o nome de usuário já existir', () => {
    const username = 'admin'; // Nome de usuário existente
    const password = 'Senha123';
  
    // Primeira execução: cadastrar o usuário
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();
    cy.url().should('include', '/cursos');
    cy.get('.navbar-toggler').click();
    cy.get('.offcanvas').should('be.visible');
    cy.get('.nav-link').contains('Cadastro').click();
  
    // Preencher com dados do usuário já existente
    cy.get('input[name="nome"]').type('Ruan');
    cy.get('input[name="sobrenome"]').type('silva');
    cy.get('input[name="username"]').type(username); 
    cy.get('input[name="senha"]').type(password);
  
    // Submeter o formulário
    cy.get('button[type="submit"]').click();
  
    // Verificar mensagem de erro
    cy.get('#alert-container')
      .should('be.visible')
      .and('contain.text', 'Nome de usuário já existe. Por favor, escolha outro nome de usuário.');
  });
  
});
```

**Estrutura Geral**

1. **`describe`**:
    - Agrupa todos os testes relacionados ao mesmo tema: neste caso, os testes das páginas de **Cadastro** e **Login**.
    - Torna a organização mais clara e melhora a legibilidade dos testes.
2. **`beforeEach`**:
    - Esse método é executado **antes de cada teste** individualmente.
    - A lógica aqui é acessar a página de login (`cy.visit('http://127.0.0.1:8000/login')`) para garantir que todos os testes partam de um estado inicial comum e controlado.
    

**1º. Teste: Carregar a Página de Login**

**Lógica**:

- Verificar se a página carrega corretamente.
- **Passos**:
    1. Obtém o título da página (`cy.title()`).
    2. Garante que o título contém a palavra "Controle de Frequência".
    3. Localiza o elemento com a classe `.titulo` e verifica:
        - Se está visível.
        - Se contém o texto "Fazer Login".
        

**2º. Teste: Login Bem-Sucedido**

**Lógica**:

- Simula um login válido.
- **Passos**:
    1. Preenche o campo de **usuário** com `'admin'`.
    2. Preenche o campo de **senha** com `'Senai502@TCC'`.
    3. Clica no botão de **login**.
    4. Verifica se a URL da página redirecionada contém `/cursos`, garantindo que o login foi bem-sucedido.
    

**3º. Teste: Abrir o Menu e Navegar para Cadastro**

**Lógica**:

- Após realizar o login, verifica a funcionalidade de navegação pelo menu offcanvas para acessar a página de cadastro.
- **Passos**:
    1. Realiza o login (passos do teste anterior).
    2. Clica no botão do menu (`.navbar-toggler`).
    3. Garante que o menu lateral (offcanvas) está visível.
    4. Localiza o link "Cadastro" e clica nele.
    5. Verifica se a URL redireciona para `/cadastro`.
    

**4º. Teste: Verificar Campos na Página de Cadastro**

**Lógica**:

- Verifica a presença dos campos necessários na página de cadastro.
- **Passos**:
    1. Após acessar a página de cadastro (lógica do teste anterior), verifica:
        - Se os campos "Nome", "Sobrenome", "Username" e "Senha" existem.
        - Se o botão de submissão contém o texto "Cadastrar".
        

**5º. Teste: Envio Bem-Sucedido do Formulário de Cadastro**

**Lógica**:

- Preenche o formulário com dados válidos e o envia, verificando se a criação do usuário é bem-sucedida.
- **Diferencial**:
    - O nome de usuário (**username**) é gerado dinamicamente utilizando o timestamp retornado pelo método `Date.now()`. Esse método fornece o timestamp atual em milissegundos desde 1º de janeiro de 1970 (Época Unix), criando um número único baseado no momento em que o código é executado. Como os testes são realizados em momentos diferentes, esse valor assegura que o nome de usuário seja sempre único.
- **Passos**:
    1. Preenche os campos do formulário.
    2. Envia o formulário clicando no botão "Cadastrar".
    3. Verifica se uma mensagem de sucesso aparece.
    

**6º. Teste: Exibição de Erro para Usuário Existente**

**Lógica**:

- Simula a tentativa de cadastrar um usuário com o mesmo nome de usuário já existente no sistema.
- **Passos**:
    1. Após acessar a página de cadastro, preenche os campos com dados onde o nome de usuário já é utilizado.
    2. Envia o formulário.
    3. Verifica se uma mensagem de erro aparece informando que o nome de usuário já existe.

#### **Página Homepage + Formulário de Login**

<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/teste_home.png" alt="Teste de Homepage" width="45%">
  <img src="img/teste_login.png" alt="Teste de Login" width="45%">
</p>

***Homepage***

```jsx
describe('Testes da Página Inicial', () => {
  beforeEach(() => {
    // Ajuste a URL base conforme necessário para seu ambiente de desenvolvimento
    cy.visit('http://127.0.0.1:8000/');
  });

  it('deve carregar a página inicial corretamente', () => {
    // Verifica se o título da página contém o nome correto
    cy.title().should('contain', 'Controle de Frequência');

    // Resto do teste permanece o mesmo
    cy.get('.titulo').should('be.visible');
    cy.get('.titulo').should('have.text', 'Gestão de Atrasos');
  });

  it('deve ter um botão de login com os atributos corretos', () => {
    // Verifica o botão de login
    cy.get('a[href*="login"]').should('exist');
    cy.get('a[href*="login"]').should('be.visible');
    cy.get('a[href*="login"]').should('have.attr', 'aria-label', 'Entrar na conta');
    cy.get('a[href*="login"]').should('have.attr', 'accesskey', 'l');
  });

  it('deve ter uma imagem de fundo', () => {
    // Verifica a imagem de fundo
    cy.get('.imag img').should('be.visible');
    cy.get('.imag img')
      .should('have.attr', 'src')
      .and('include', 'img_home.webp');
    
    cy.get('.imag img')
      .should('have.attr', 'width', '400')
      .and('have.attr', 'height', '300');
  });

  it('deve navegar para a página de login ao clicar no botão de login', () => {
    // Testa a navegação para a página de login
    cy.get('a[href*="login"]').click();
    cy.url().should('include', '/login');
  });

  it('deve ter as classes CSS corretas para animações', () => {
    // Verifica as classes de animação
    cy.get('.bg_Home').should('have.class', 'animate');
    cy.get('.bg_Home').should('have.class', 'downUp-1');
  });

  it('deve carregar com o tema claro por padrão', () => {
    // Verifica se o tema inicial é claro
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'light');
    cy.get('#theme-icon').should('have.class', 'bi-sun-fill');
  });

  it('deve alternar para o tema escuro ao clicar no botão de alternância', () => {
    // Clica no botão de alternância de tema
    cy.get('#theme-toggle').click();
    
    // Verifica se o tema mudou para escuro
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'dark');
    cy.get('#theme-icon').should('have.class', 'bi-moon-fill');
  });

  it('deve alternar de volta para o tema claro ao clicar no botão de alternância novamente', () => {
    // Alterna para o tema escuro
    cy.get('#theme-toggle').click();
    
    // Alterna de volta para o tema claro
    cy.get('#theme-toggle').click();
    
    // Verifica se o tema voltou para claro
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'light');
    cy.get('#theme-icon').should('have.class', 'bi-sun-fill');
  });

  it('deve lembrar a escolha do tema entre sessões', () => {
    // Altera para o tema escuro e garante que a escolha seja salva
    cy.get('#theme-toggle').click();
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'dark');
    cy.window().its('localStorage').invoke('getItem', 'theme').should('equal', 'dark');
    
    // Recarrega a página e verifica se o tema permanece escuro
    cy.reload();
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'dark');
    cy.get('#theme-icon').should('have.class', 'bi-moon-fill');
  });
});

```

**Estrutura Geral**

- **`describe`**: Agrupa todos os testes relacionados à página inicial.
- **`beforeEach`**: Configurações comuns a todos os testes dentro do `describe`. Aqui, cada teste começa com o acesso à URL da página inicial.

**1º. Teste: Carregar a página inicial corretamente**

- **Objetivo**: Validar que a página carrega sem problemas e exibe as informações esperadas.
- **Validações**:
    - O título da aba do navegador contém "Controle de Frequência".
    - Um elemento com a classe `.titulo` está visível e exibe o texto "Gestão de Atrasos".
    

**2º. Teste: Botão de login**

- **Objetivo**: Verificar a existência e atributos do botão de login.
- **Validações**:
    - O botão de login existe, é visível e possui atributos específicos como:
        - `aria-label`: Para acessibilidade.
        - `accesskey`: Atalho de teclado para acessar o botão.
        

**3º. Teste: Imagem de fundo**

- **Objetivo**: Verificar a presença e atributos de uma imagem na página inicial.
- **Validações**:
    - A imagem está visível.
    - O atributo `src` contém o nome do arquivo `img_home.webp`.
    - A imagem tem largura e altura definidas (`400` e `300`).
    

**4º. Teste: Navegação para a página de login**

- **Objetivo**: Verificar a funcionalidade do botão de login.
- **Validações**:
    - Ao clicar no botão, o usuário é redirecionado para a URL `/login`.
    

**5º. Teste: Classes CSS de animações**

- **Objetivo**: Verificar que elementos específicos têm classes CSS aplicadas corretamente para animações.
- **Validações**:
    - O elemento com a classe `.bg_Home` possui as classes `animate` e `downUp-1`.
    

**6º. Teste: Tema claro por padrão**

- **Objetivo**: Garantir que o tema inicial da página seja **claro**.
- **Validações**:
    - O atributo `data-theme` no elemento raiz do documento está definido como `light`.
    - O ícone do tema é representado pela classe `bi-sun-fill`.
    

**7º. Teste: Alternância para tema escuro**

- **Objetivo**: Testar a funcionalidade de alternância para o tema escuro.
- **Validações**:
    - Ao clicar no botão de alternância, o tema muda para `dark`.
    - O ícone do tema agora possui a classe `bi-moon-fill`.
    

**8º. Teste: Alternância de volta para tema claro**

- **Objetivo**: Testar a alternância do tema escuro de volta para o tema claro.
- **Validações**:
    - O atributo `data-theme` retorna para `light`.
    - O ícone do tema exibe `bi-sun-fill` novamente.
    

**9º. Teste: Persistência do tema entre sessões**

- **Objetivo**: Garantir que o tema escolhido pelo usuário (ex.: escuro) é salvo no `localStorage` e carregado ao recarregar a página.
- **Validações**:
    - Após mudar para o tema escuro, a entrada no `localStorage` é "dark".
    - Após recarregar a página, o tema ainda está definido como escuro.

***Login***

```jsx
describe('Testes da Página de Login', () => {
  
  beforeEach(() => {
    // Visita a página de login antes de cada teste
    cy.visit('http://127.0.0.1:8000/login');
  });

  it('deve carregar a página de login corretamente', () => {
    // Verifica o título da página
    cy.title().should('include', 'Controle de Frequência');
  
    // Verifica se o título da página existe, independentemente da visibilidade
    cy.get('.titulo').should('exist').and('have.text', 'Fazer Login');
  });
  

  it('deve fazer login com credenciais válidas', () => {
    cy.intercept('POST', 'http://127.0.0.1:8000/login').as('loginRequest');

    // Preenche os campos de login
    cy.get('input[name="username"]').type('teste');
    cy.get('input[name="senha"]').type('teste@123');
    cy.get('button[type="submit"]').click();

    // Espera a resposta e verifica o código de status
    cy.wait('@loginRequest').its('response.statusCode').should('be.oneOf', [200, 302]);

    // Verifica se a URL mudou para a página de cursos
    cy.url().should('include', '/cursos');
  });

  it('deve exibir mensagem de erro com credenciais inválidas', () => {
    cy.intercept('POST', '/login').as('loginRequest');

    // Preenche campos com credenciais inválidas
    cy.get('input[name="username"]').type('usuario_invalido');
    cy.get('input[name="senha"]').type('senha_invalida');
    cy.get('button[type="submit"]').click();

    // Espera a resposta e verifica a URL
    cy.wait('@loginRequest').its('response.statusCode').should('eq', 302);
    cy.url().should('include', '/login');

    // Verifica se a mensagem de erro está visível
    cy.get('#alert-container').should('be.visible').and('have.class', 'alert-warning');
  });

  it('deve alternar a visibilidade da senha', () => {
    const passwordField = 'input[name="senha"]';

    // Verifica se o tipo do campo de senha é password
    cy.get(passwordField).should('have.attr', 'type', 'password');
    cy.get('#btnSenha').click();
    cy.get(passwordField).should('have.attr', 'type', 'text');
    cy.get('#btnSenha').click();
    cy.get(passwordField).should('have.attr', 'type', 'password');
  });

  it('deve redirecionar para a página de cursos após login bem-sucedido', () => {
    cy.get('input[name="username"]').type('teste');
    cy.get('input[name="senha"]').type('teste@123');
    cy.get('button[type="submit"]').click();

    cy.url().should('include', '/cursos');
  });

  it('deve carregar com o tema claro por padrão', () => {
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'light');
    cy.get('#theme-icon').should('have.class', 'bi-sun-fill');
  });

  it('deve alternar para o tema escuro ao clicar no botão de alternância', () => {
    cy.get('#theme-toggle').click();
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'dark');
    cy.get('#theme-icon').should('have.class', 'bi-moon-fill');
  });

  it('deve alternar de volta para o tema claro ao clicar novamente', () => {
    cy.get('#theme-toggle').click();
    cy.get('#theme-toggle').click();
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'light');
    cy.get('#theme-icon').should('have.class', 'bi-sun-fill');
  });

  it('deve lembrar a escolha do tema entre sessões', () => {
    cy.get('#theme-toggle').click();
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'dark');
    
    // Verifica se o tema foi salvo no localStorage
    cy.window().its('localStorage').invoke('getItem', 'theme').should('equal', 'dark');

    // Recarrega a página e verifica se o tema permanece
    cy.reload();
    cy.document().its('documentElement').should('have.attr', 'data-theme', 'dark');
    cy.get('#theme-icon').should('have.class', 'bi-moon-fill');
  });
});
```

**Estrutura Geral**

- **`describe`**: Agrupa os testes relacionados à página de login.
- **`beforeEach`**: Configurações comuns a todos os testes dentro do `describe`. Antes de cada teste, a página de login é acessada (`cy.visit`).

**1º. Teste: Carregar a página de login corretamente**

- **Objetivo**: Garantir que a página de login carrega corretamente.
- **Validações**:
    - O título da aba do navegador contém "Controle de Frequência".
    - O elemento com a classe `.titulo` existe e exibe o texto "Fazer Login".
    

**2º. Teste: Login com credenciais válidas**

- **Objetivo**: Testar o fluxo de login com credenciais corretas.
- **Validações**:
    - Um `POST` é enviado para o endpoint de login.
    - A resposta do servidor retorna status 200 ou 302 (redirecionamento).
    - Após login bem-sucedido, a URL muda para `/cursos`.
    

**3º. Teste: Mensagem de erro com credenciais inválidas**

- **Objetivo**: Testar o fluxo de login com credenciais incorretas.
- **Validações**:
    - A requisição `POST` retorna status 302 (redirecionando de volta para a página de login).
    - A URL permanece `/login`.
    - Um alerta de erro visível, com a classe `alert-warning`, aparece na página.
    

**4º. Teste: Alternância da visibilidade da senha**

- **Objetivo**: Verificar o comportamento do botão de alternância da visibilidade da senha.
- **Validações**:
    - O campo de senha inicia com o atributo `type="password"`.
    - Após clicar no botão, o atributo muda para `type="text"` (mostrando a senha).
    - Outro clique no botão retorna o campo para `type="password"`.
    

**5º. Teste: Redirecionamento após login bem-sucedido**

- **Objetivo**: Confirmar o redirecionamento correto após login válido.
- **Validação**:
    - Após o login, a URL é alterada para `/cursos`.
    

**6º. Teste: Tema claro por padrão**

- **Objetivo**: Garantir que o tema inicial é **claro**.
- **Validações**:
    - O atributo `data-theme` do elemento raiz (`documentElement`) está definido como `light`.
    - O ícone do tema é representado pela classe `bi-sun-fill`.
    

**7º. Teste: Alternância para tema escuro**

- **Objetivo**: Testar a funcionalidade de alternância para o tema escuro.
- **Validações**:
    - O atributo `data-theme` muda para `dark`.
    - O ícone do tema exibe a classe `bi-moon-fill`.
    

**8º. Teste: Alternância de volta para tema claro**

- **Objetivo**: Testar a alternância do tema escuro de volta para claro.
- **Validações**:
    - O atributo `data-theme` retorna para `light`.
    - O ícone do tema exibe `bi-sun-fill`.
    

**9º. Teste: Persistência do tema entre sessões**

- **Objetivo**: Garantir que o tema escolhido pelo usuário é salvo e reaplicado após recarregar a página.
- **Validações**:
    - O tema "dark" é salvo no `localStorage`.
    - Após recarregar, o tema permanece "dark".

#### **Página Cursos + Exclusão de Curso**

<p align="center" style="display: flex; justify-content: center; gap: 10px;">
  <img src="img/teste_cursos.png" alt="Teste de Cursos" width="45%">
</p>

#### Página de Cursos + Alunos

```jsx
describe('Teste de login', () => {
  beforeEach(() => {
    // Acessa a página de login antes de cada teste
    cy.visit('http://127.0.0.1:8000/login');
  });

  it('Deve preencher o formulário de login corretamente', () => {
    // Verifica se o campo de nome de usuário está visível
    cy.get('input[name="username"]').should('be.visible');
    // Verifica se o campo de senha está visível
    cy.get('input[name="senha"]').should('be.visible');
  });

  it('Deve realizar o login com sucesso', () => {
    // Realiza o login
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();

    // Verifica redirecionamento para a página de cursos
    cy.url().should('include', '/cursos');
  });
});

describe('Teste de acesso à página de relatórios', () => {
  beforeEach(() => {
    // Realiza o login antes de acessar as páginas
    cy.visit('http://127.0.0.1:8000/login');
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();

    // Verifica redirecionamento para a página de cursos
    cy.url().should('include', '/cursos');
  });

  it('Deve acessar a página de relatórios', () => {
    // Clica no ícone de relatórios
    cy.get('a[href="/relatorio"]').click();

    // Verifica se foi redirecionado corretamente
    cy.url().should('include', '/relatorio');

    // Valida se algum elemento específico da página de relatórios está visível
    cy.get('h2').contains('Relatórios').should('be.visible');
  });
});

describe('Teste de acesso à página de notificações', () => {
  beforeEach(() => {
    // Realiza o login antes de acessar as páginas
    cy.visit('http://127.0.0.1:8000/login');
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();

    // Verifica redirecionamento para a página de cursos
    cy.url().should('include', '/cursos');
  });

  it('Deve acessar a página de notificações', () => {
    // Clica no ícone de notificações
    cy.get('a[href="/notificacoes"]').click();

    // Verifica se foi redirecionado corretamente
    cy.url().should('include', '/notificacoes');

    // Valida se algum elemento específico da página de notificações está visível
    cy.get('h2').contains('Notificações').should('be.visible');
  });
});

// Descreve a navegação para a página de cursos após login
describe('Teste de navegação para a página de cursos', () => {
  beforeEach(() => {
    // Realiza o login antes de acessar a página de cursos
    cy.visit('http://127.0.0.1:8000/login');
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();

    // Verifica redirecionamento para a página de cursos
    cy.url().should('include', '/cursos');
  });

  it('Deve acessar a página de cursos após login', () => {
    // Verifica se a URL contém "/cursos"
    cy.url().should('include', '/cursos');
  });

  it('Deve exibir a lista de cursos', () => {
    // Verifica se o container de cursos está visível
    cy.get('#results-container').should('be.visible');
    // Verifica se há cursos na lista
    cy.get('#results-container .curso').should('exist');
  });

  it('Deve exibir mensagem apropriada quando nenhum curso é encontrado', () => {
    // Abre o campo de pesquisa
    cy.get('#search-icon').click();
    
    // Insere um termo que não corresponda a nenhum curso
    cy.get('#search-container input').type('CursoInexistente');
    
    // Executa a pesquisa
    cy.get('#search-container button').click();

    // Verifica se a mensagem "Nenhum curso encontrado" aparece
    cy.get('#results-container').should('contain', 'Nenhum curso encontrado');
    
    // Alternativamente, verifica se nenhum curso é listado
    cy.get('#results-container .curso').should('not.exist');
  });
});

describe('Teste de pesquisa e exclusão de curso', () => {
  beforeEach(() => {
    // Realiza o login antes de acessar a página de cursos
    cy.visit('http://127.0.0.1:8000/login');
    cy.get('input[name="username"]').type('admin');
    cy.get('input[name="senha"]').type('Senai502@TCC');
    cy.get('button[type="submit"]').click();

    // Verifica redirecionamento para a página de cursos
    cy.url().should('include', '/cursos');
  });

  it('Deve excluir um curso com sucesso e verificar mensagens', () => {
    // Abre o campo de pesquisa
    cy.get('#search-icon').click();
    // Insere o termo "Teste" no campo de busca
    cy.get('#search-container input').type('Teste');
    // Executa a pesquisa
    cy.get('#search-container button').click();

    // Verifica se cursos foram encontrados
    cy.get('#results-container .curso').should('exist');

    // Clica no primeiro curso encontrado
    cy.get('#results-container .curso').first().click();

    // Verifica se foi redirecionado para a página do aluno
    cy.url().should('include', '/alunos');

    // Clica no botão "Excluir Curso" para abrir o modal de confirmação
    cy.get('button[data-bs-target="#excluirModal"]').click();

    // Verifica se o modal está visível
    cy.get('#excluirModal').should('be.visible');

    // Confirma a exclusão do curso clicando no botão de confirmação dentro do modal
    cy.get('#excluirModal form button[type="submit"]').click();

    // Aguarda o redirecionamento para a página de cursos
    cy.url().should('include', '/cursos');

    // Verifica se a mensagem de sucesso foi exibida na página de cursos
    cy.get('#alert-container', { timeout: 10000 })  // Aumentando o timeout
      .should('contain', 'Curso e alunos associados excluídos com sucesso.');

  });
});
```

**Estrutura Geral**

1. **`describe`**:
    - Agrupa testes relacionados sob um mesmo "contexto" ou funcionalidade, como login, acesso a páginas ou ações específicas (ex.: exclusão de cursos).
2. **`beforeEach`**:
    - Executa comandos repetitivos antes de cada teste dentro de um `describe`. Aqui, normalmente acessa a página de login e realiza o login automático.
3. **`it`**:
    - Representa um **caso de teste específico**. Cada `it` contém uma descrição e os passos necessários para verificar uma funcionalidade.
4. **Comandos Cypress**:
    - Cypress utiliza comandos encadeados para realizar interações com a interface e validações, como `cy.visit`, `cy.get`, `cy.url`, entre outros.
    

**1º. Testes de Login**

Os testes dentro do primeiro `describe` verificam o funcionamento básico do login.

- **Verificação de campos visíveis**:
    - `cy.get('input[name="username"]').should('be.visible');`
    - Garante que os campos de username e senha estejam visíveis na página.
- **Teste de login bem-sucedido**:
    - Preenche os campos com credenciais válidas (`admin` e `Senai502@TCC`), clica no botão de login e verifica se o redirecionamento para a página `/cursos` ocorre.
    

**2º. Teste de Acesso à Página de Relatórios**

Este `describe` foca em validar o acesso à página de relatórios após o login.

- **Login Automático no `beforeEach`**:
    - Antes de cada teste, o sistema faz login para garantir que o usuário está autenticado.
- **Acesso à Página de Relatórios**:
    - O teste clica no link que leva à página de relatórios (`a[href="/relatorio"]`).
    - Valida que a URL muda para `/relatorio` e verifica se um elemento da página de relatórios, como um título, está visível.
    

**3º. Teste de Acesso à Página de Notificações**

Semelhante ao teste anterior, mas foca na página de notificações.

- **Verifica elementos da página de notificações**:
    - Após clicar no link de notificações (`a[href="/notificacoes"]`), o teste garante que o título "Notificações" está visível e que a URL foi atualizada corretamente.
    

**4º. Teste de Navegação para a Página de Cursos**

Estes testes validam o funcionamento da página de cursos:

- **Verificar URL e conteúdo**:
    - Garante que, após o login, a página `/cursos` é carregada.
    - Valida que a lista de cursos (identificada pelo ID `results-container`) está visível.
- **Testar funcionalidade de busca**:
    - Simula a pesquisa por cursos, verifica resultados e exibe mensagens apropriadas se nenhum curso for encontrado (ex.: "Nenhum curso encontrado").
    

**5º. Teste de Pesquisa e Exclusão de Curso**

Este `describe` testa a funcionalidade de excluir um curso específico.

- **Fluxo da exclusão**:
    - Simula a pesquisa de um curso com o termo "Teste" ( “Teste” e um curso criado apenas para o teste desta função de exclusão ).
    - Após encontrar um curso, clica no curso listado e verifica o redirecionamento para `/alunos`.
    - Clica no botão de exclusão, abre um modal de confirmação, e confirma a exclusão.
    - Verifica se o curso foi removido e se a mensagem de sucesso é exibida.
- **Detalhes importantes**:
    - **Aumento de timeout**:
        - No comando `cy.get('#alert-container', { timeout: 10000 })`, o timeout é aumentado para lidar com eventuais atrasos no carregamento da página ou na exibição da mensagem de sucesso.


#### <span style="color: #AC58FA;">Testes Unitários</span>

#### **Geração de Relatório**

```python
from io import BytesIO
from django.test import TestCase
from web.views import gerar_relatorio_pdf

class GerarRelatorioPdfTestCase(TestCase):

    def test_geracao_pdf(self):
        # Mock dos dados para o relatório
        relatorio = [
            {"categoria": "Top Atrasos", "nome": "João Silva", "turma": "DS101", "total_atrasos": 5, "total_faltas": 2},
            {"categoria": "Baixa Frequência", "nome": "Maria Souza", "turma": "DS102", "total_atrasos": 3, "total_faltas": 10},
        ]

        pdf_buffer = gerar_relatorio_pdf(relatorio)

        # Validações
        self.assertIsInstance(pdf_buffer, BytesIO)  # Certifica-se de que o retorno é um BytesIO
        self.assertGreater(len(pdf_buffer.getvalue()), 0)  # Verifica se o PDF não está vazio
```

**Resultado**

```python
Found 1 test(s).
Creating test database for alias 'default'...
System check identified no issues (0 silenced).
.
----------------------------------------------------------------------
Ran 1 test in 0.077s

OK
Destroying test database for alias 'default'...
```

O teste executado foi bem-sucedido, conforme o resultado:

- **Resumo:**
    - Foi encontrado **1 teste** (`Found 1 test(s).`).
    - O banco de dados de teste foi criado e utilizado sem problemas.
    - O sistema identificou que não há problemas estruturais com o projeto (`System check identified no issues`).
    - O teste foi **concluído com sucesso** (`Ran 1 test in 0.077s` e `OK`).
    

Isso significa que a função `gerar_relatorio_pdf` está funcionando conforme esperado. O retorno do PDF está sendo gerado corretamente como um objeto `BytesIO` e possui conteúdo, atendendo às validações feitas no teste.

#### <span style="color: #AC58FA;">Testes Manuais</span>

Os testes realizados no sistema de Controle de Frequência foram conduzidos, além disso, de forma manual, onde foi acessado o site diretamente para verificar o funcionamento das funcionalidades implementadas. Durante o processo de testes, exploramos diversas áreas, páginas e funções do sistema, realizando as interações como um usuário comum faria, sem a utilização de ferramentas automáticas de testes.

Esses testes manuais consistiram em navegar pelas páginas do site, preencher formulários, verificar a integridade dos dados exibidos e validar os comportamentos esperados para as funcionalidades, como o registro de entradas e saídas, a exibição de informações dos alunos, o cálculo da frequência, adição e exclusão de cursos ou alunos, etc.

A abordagem manual nos permitiu verificar certos pontos do nosso projeto:

- Usabilidade do sistema;
- Identificação de possíveis falhas na interface;
- Garantir interações com o banco de dados (inserção de dados, recuperação de informações);

Embora os testes manuais possam ser mais lentos e suscetíveis a erros humanos, foram fundamentais para garantir que as funcionalidades mais críticas do sistema estivessem funcionando conforme o esperado antes da implementação de testes automatizados.

Após a execução dos testes, os resultados mostraram que os testes manuais foram bem-sucedidos no uso do sistema. Não foram encontrados erros críticos, e o sistema funcionou conforme o esperado, com a navegação fluindo de forma intuitiva e as funcionalidades respondendo de maneira adequada às interações dos usuários.

---

## <span style="color: #9A2EFE;">Autores</span>

<div align="center">
    <table>
    <tr>
        <td align="center" >
        <a href="https://github.com/Projectyuuri07?tab=following">
            <img src="https://avatars.githubusercontent.com/Projectyuuri07" width="115px;" alt="Foto_Yuri"/><br>
            <sub>
            <b>Yuri</b>
            </sub>
        </a>
        </td>
        <td align="center" >
        <a href="https://github.com/alemes7">
            <img src="https://avatars.githubusercontent.com/alemes7" width="115px;" alt="Foto_Alexandre"/><br>
            <sub>
            <b>Alexandre</b>
            </sub>
        </a>
        </td>
        <td align="center" >
        <a href="https://github.com/TH4YSZ">
            <img src="https://avatars.githubusercontent.com/TH4YSZ" width="115px;" alt="Foto_Thaina"/><br>
            <sub>
            <b>Thaina</b>
            </sub>
        </a>
        </td>
        <td align="center" >
        <a href="https://github.com/yRuanz">
            <img src="https://avatars.githubusercontent.com/yRuanz" width="115px;" alt="Foto_Ruan"/><br>
            <sub>
            <b>Ruan</b>
            </sub>
        </a>
        </td>
        <td align="center" >
        <a href="https://github.com/natinhaaa">
            <img src="https://avatars.githubusercontent.com/natinhaaa" width="115px;" alt="Foto_Natalia"/><br>
            <sub>
            <b>Natalia</b>
            </sub>
        </a>
        </td>
        <td align="center" >
        <a href="https://github.com/Allerim321">
            <img src="https://avatars.githubusercontent.com/Allerim321" width="115px;" alt="Foto_Mirella"/><br>
            <sub>
            <b>Mirella</b>
            </sub>
        </a>
        </td>   
    </tr>
    </table>
</div>
