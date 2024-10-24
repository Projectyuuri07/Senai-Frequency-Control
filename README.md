# Senai-Frequency-Control

## <span style="color: #8000FF;">Índice</span>

1. **<span style="color: #9A2EFE;">Introdução</span>**
   - [Sobre a documentação](#sobre-a-documentação)
   - [Problemática](#problemática)
   - [Objetivos](#objetivos)
   - [Justificativa](#justificativa)

2. **<span style="color: #9A2EFE;">Metodologia</span>**
   - [Ferramentas a serem utilizadas](#ferramentas-a-serem-utilizadas)
   - [Linguagens de programação](#linguagens-de-programação)
   - [Linguagens de marcação](#linguagens-de-marcação)
   - [Linguagens de estilo](#linguagens-de-estilo)
   - [Frameworks](#frameworks)
   - [Banco de dados](#banco-de-dados)
   - [Metodologia para desenvolvimento](#metodologia-para-desenvolvimento)

3. **<span style="color: #9A2EFE;">Implementação</span>**
   - [v0.0 - Configuração do ambiente de desenvolvimento](#v00---configuração-do-ambiente-de-desenvolvimento)
   - [v0.1 - Criação do aplicativo](#v01---criação-do-aplicativo)
   - [v0.2 - Criação das URLs e Views](#v02---criação-das-urls-e-views)
   - [v1.0 - Início do desenvolvimento das funcionalidades](#v1.0---Início-do-desenvolvimento-das-páginas)
   - [Temas claro e escuro](#temas-claro-e-escuro)
   - [Elaboração das classes](#elaboração-das-classes)
   - [Lógica de mostrar e esconder senha](#lógica-de-mostrar-e-esconder-senha)

4. **<span style="color: #9A2EFE;">Manual do usuário</span>**
   - [Iniciando](#iniciando)

---

## <span style="color: #8000FF;">Introdução</span>

### <span style="color: #9A2EFE;">Sobre a documentação</span>

A presente documentação, realizada pelo grupo 03 do Curso Técnico de Desenvolvimento de Sistemas**,** da instituição Senai Conde Alexandre Siciliano da cidade de Jundiaí, visa explicar o funcionamento do projeto de TCC “Gestão de Frequência Automatizada: Simplificando a Rotina Administrativa”.

### <span style="color: #9A2EFE;">Problemática</span>

Não há dúvidas de que o processo manual na averiguação de frequência dos alunos da instituição Senai é um tanto cansativo, bem como um desperdício de tempo e esforço. Conforme algum aluno entra após o horário tolerável, ele recebe um papel de autorização que deve ser assinado por algum membro da gestão escolar, a fim de ser permitida a entrada do mesmo em sua respectiva sala de aula. Ao entrar, deve entregar ao professor, que verificará a assinatura e, em seguida, guardará o papel.

Levando em conta que uma quantidade considerável de alunos atrasa-se por dia, esse processo toma tempo e esforço dos profissionais envolvidos, bem como interfere no rendimento das aulas conforme o aluno interrompe a explicação do instrutor para entregá-lo o papel.
Não bastasse isso, o desperdício de papel é outro fator a ser considerado, visto que após seu uso é guardado e, posteriormente, jogado fora.

Os argumentos citados provam que seja não só benéfica como necessária a automação desse procedimento.

### <span style="color: #9A2EFE;">Objetivos</span>

Nosso objetivo em solucionar este problema visa em automatizar os processos para o gerenciamento dos atrasos, diminuindo assim, o tempo gasto para gerencia-los, reduzindo o consumo de papel que seriam gastos com a autorização para a entrada em sala de aula além de diminuir a interferência dos estudantes durante as orientações do instrutor.
Ademais, na plataforma, os coordenadores serão notificados após o estudante ter atrasado três vezes ou mais, tendo como requisito para a adição, a entrada superior a 10 minutos do horário da ingressão do aluno a instituição. Com isso, eles poderão tomar as devidas medidas para resolver o problema com o aluno.

Em nosso sistema, em cada sala de aula constará uma lista dos alunos e do responsável da turma bem como a quantidade dos atrasos no semestre. No final de cada mês, será gerado um relatório com uma visão geral dos atrasos e frequências do período.
Por fim, na plataforma terá uma ferramenta de busca para a pesquisa de salas de aula e de alunos, facilitando o acesso rápido e eficiente às informações necessárias para a gestão escolar.
Como passo inicial para o desenvolvimento do projeto, a equipe focará em pesquisas relacionadas ao tema, como a geração de relatórios, integração do sistema com a catraca para elaborar as regras de negócio e levantamento de requisitos para que, posteriormente, possamos desenvolver a etapa de design com as dúvidas esclarecidas e maior segurança.

Além do objetivo principal de gerenciamento dos atrasos, implementaremos uma lógica para administrar a frequência dos alunos, utilizando os dados de entrada e saída dos estudantes para melhor visualização do desempenho escolar.

Para a etapa de implementação, a primeira e a mais importante meta é coletar os dados da catraca de maneira automatizada e armazená-los no banco de dados para mostrá-los de forma visual e simplificada ao usuário. Todavia, devido às restrições impostas pela Lei Geral de Proteção de Dados (LGPD - Lei 13.709/2018), que tem como objetivo **proteger os** direitos fundamentais de liberdade, privacidade e o livre desenvolvimento da personalidade da pessoa natural, não foi possível ter acesso a essas informações, impactando assim, com todo o cronograma, obrigando-nos a replanejar todo o roteiro de desenvolvimento. Outro alvo que planejamos desenvolver com maestria, é colocar em prática as regras de negócio relacionadas à frequência. Atualmente, esse é o segundo maior desafio a ser enfrentado do projeto como um todo.

### <span style="color: #9A2EFE;">Justificativa</span>

A falta de controle da frequência dos alunos tem sido uma preocupação recorrente relatada por professores e coordenadores do SENAI. Muitos alunos chegam atrasados e entram no meio das aulas com um papel assinado pela coordenação, interrompendo as aulas e causando transtornos. Este problema não só prejudica a concentração e o andamento das aulas, mas também gera uma carga administrativa excessiva para os coordenadores, que precisam lidar com uma grande quantidade de papelada e autorizações manuais.

A situação atual, onde alunos atrasados precisam de autorização manual para entrar em sala, provoca múltiplos problemas:

1. **<span style="color: #4682B4;">Interrupção das Aulas</span>**: Cada vez que um aluno entra atrasado, a aula é interrompida, afetando a concentração de todos e reduzindo o tempo útil de ensino;
2. **<span style="color: #4682B4;">Carga Administrativa</span>**: Coordenadores gastam um tempo significativo assinando permissões de entrada para alunos atrasados, tempo este que poderia ser dedicado a outras tarefas mais produtivas;
3. **<span style="color: #4682B4;">3. Falta de Disciplina</span>**: A ausência de um sistema de controle eficaz incentiva a falta de disciplina entre os alunos, que não enfrentam consequências significativas por seus atrasos frequentes.
4. **<span style="color: #4682B4;">Dificuldade de Monitoramento</span>**: Professores e coordenadores têm dificuldade em monitorar e registrar manualmente todas as ocorrências de atraso, o que pode levar a uma subestimação do problema e à falta de ações corretivas.
5. **<span style="color: #4682B4;">Comunicação Ineficiente</span>**: Os responsáveis pelos alunos não são prontamente informados sobre a frequência de atrasos, dificultando o acompanhamento e a intervenção necessária para corrigir o comportamento dos estudantes.


Nosso sistema permitirá que a gestão monitore os atrasos e a frequência dos alunos de maneira mais eficaz, diminuindo esforços manuais e simplificando a rotina administrativa. A implementação dessas estratégias melhorará significativamente a comunicação interna e a solução de problemas de forma eficiente.

### <span style="color: #9A2EFE;">Observação</span>

Durante as primeiras etapas de desenvolvimento, passamos por uma mudança de planos inesperada, vinda de um esclarecimento sobre o projeto com a Analista de Qualidade de Vida. Tal processo nos explanou sobre nossas limitações em relação ao acesso dos dados dos estudantes que passariam pela catraca. A partir disso, nos reorganizamos em função de seguir com o projeto nos baseando nessas modificações.

---

## <span style="color: #8000FF;">Metodologia</span>

### **<span style="color: #9A2EFE;">Ferramentas utilizadas</span>**

- **<span style="color: #4682B4;">Trello:</span>** É um aplicativo de gerenciamento de projeto baseado na web;
- **<span style="color: #4682B4;">Visual Studio Code:</span>** É um editor de código-fonte desenvolvido pela Microsoft para Windows, Linux e macOS. Ele inclui suporte para depuração, controle de versionamento Git incorporado, realce de sintaxe, complementação inteligente de código, snippets e refatoração de código. Utilizamos a versão 1.91.1-x64;
- **<span style="color: #4682B4;">Git:</span>** É um sistema de controle de versões distribuído, usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo. Utilizamos a versão 2.46.0-x64;
- **<span style="color: #4682B4;">HostGator:</span>** É um provedor de hospedagem compartilhada, revendedor, virtual privado e hospedagem dedicada;
- **<span style="color: #4682B4;">Figma:</span>** É um editor gráfico de vetor e prototipagem de projetos de design baseado principalmente no navegador web, com ferramentas offline adicionais para aplicações desktop para GNU/Linux, macOS e Windows.

### **<span style="color: #9A2EFE;">Linguagens de Programação</span>**

### **<span style="color: #9A2EFE;">Python v3.12.3</span>**
Python é uma linguagem de programação interpretada, orientada a objetos, funcional, de tipagem dinâmica e forte.

Sua sintaxe é direta e fácil de entender, o que permite que desenvolvedores de qualquer nível de habilidade possam acessá-la, simplificando a compreensão e a manutenção do código. A linguagem é uma das mais populares do mundo e é amplamente utilizada em diversos setores, como desenvolvimento web, ciência de dados e inteligência artificial, garantindo uma variedade de recursos - incluindo documentação, tutoriais e fóruns – que ajudam a aprimorar as habilidades dos desenvolvedores.

Tratando-se de desempenho, o Python pode não superar outras linguagens como C ou C++ em termos de velocidade. Contudo, o Django fornece uma estrutura robusta para a construção de sistemas web utilizando a linguagem, pois a decisão de adotá-la como base para plataformas de backend, ela está fortemente ligada ao surgimento do framework, dispensando a necessidade de reescrever códigos comuns a todos os projetos web em Python.

### **<span style="color: #9A2EFE;">JavaScript</span>**
JavaScript é uma linguagem de programação interpretada e orientada a objetos, conhecida como linguagem de script para páginas Web, mas também utilizada em muitos ambientes fora dos navegadores.

A linguagem roda no _lado do cliente_ da web, ou pode ser usado para projetar/programar o comportamento de uma página web a partir da ocorrência de um evento. JavaScript é uma linguagem fácil de aprender, mas também poderosa, sendo amplamente utilizada para controlar o comportamento de páginas da web.

As capacidades dinâmicas de JavaScript incluem construção de objetos em tempo de execução, listas de variáveis de parâmetros, variáveis de funções, criação dinâmica de scripts, introspecção de objetos, e recuperação de código (programas escritos em JavaScript podem descompilar funções de volta aos seus textos originais).

### **<span style="color: #9A2EFE;">Linguagens de Marcação</span>**

#### **<span style="color: #AC58FA;">HTML 5</span>**
A Linguagem de Marcação de Hipertexto (HTML) é uma linguagem utilizada na construção de páginas na Web, podendo ser interpretada por navegadores. O HTML não é considerado uma linguagem de programação, já que ele não pode criar funcionalidades dinâmicas. Ao invés disso, com o HTML, os usuários podem criar e estruturar seções, parágrafos e links usando elementos, tags e atributos.

### **<span style="color: #9A2EFE;">Linguagens de Estilo</span>**

#### **<span style="color: #AC58FA;">CSS</span>**
Cascading Style Sheets  **ou Folhas de Estilo em Cascata, é um mecanismo para adicionar estilos a uma página web, aplicado diretamente nas tags HTML ou ficar contido dentro das tags `<style>`. Também é possível adicionar estilos adicionando um link para um arquivo CSS que contém os estilos.**

### **<span style="color: #9A2EFE;">Frameworks</span>**

#### **<span style="color: #AC58FA;">Bootstrap</span>**
O Bootstrap é um framework front-end  e de código-fonte aberto, que disponibiliza componentes prontos para utilização, ganhando muita produtividade no desenvolviento. Com ele, é possível criar e personalizar sites responsivos para dispositivos móveis, desktops e notebooks, com componentes pré-projetados e com plugins JavaScript poderosos, que facilitam a customização desses componentes. O framework segue os princípios de usabilidade e tendências de design para interfaces. Além disso, sua padronização permite que os sites obtenham uma aparência atraente.

#### **<span style="color: #AC58FA;">Django</span>**
O Django é um framework web Python de código aberto, no qual destaca-se por oferecer um ambiente simplificado para a criação de soluções web escaláveis, além proporcionar ferramentas robustas e eficientes aos desenvolvedores, dispensando a necessidade de reescrever códigos comuns a todos os projetos web em Python. Ele disponibiliza, portanto, uma estrutura pré-configurada e bibliotecas com código pronto, melhorando a produtividade e organização do desenvolvimento.

O framework utiliza a arquitetura MVT _(Model-View-Template)_, representando respectivamente, a lógica de negócios, a lógica de rederização e a de exibição da interface do usuário, facilitando a criação de aplicações e promovendo a separação das atividades e reutilização de partes do código. Essa abordagem é uma variação do tradicional padrão MVC _(Model-View-Controller)_, amplamente adotada em diversos frameworks e sistemas.

Além disso, esta estrutura prioriza a segurança, oferecendo recursos projetados para impedir ameaças como CSRF, XSS e SQL Injections. Também conta com proteções como validação automática de formulários e gerenciamento de autenticação, entre outros serviços.

Com a implementação do mapeamento “Objeto-Relacional”, o Django permite a interação do banco de dados através de classes e objetos Python, eliminando a necessidade de escrita SQL direta. Isso não apenas simplifica o acesso aos dados, mas também reduz os riscos de segurança e, ao mesmo tempo, melhora a legibilidade do código. Além disso, a estrutura facilita o mapeamento de URLs, vinculando _URLs_ específicos às suas _View_ correspondentes dentro dos aplicativos. Essa abordagem organizada direciona as solicitações do usuário para as seções apropriadas do código e agiliza a criação de URLs que são semânticos e fáceis de usar, melhorando, em última análise, a experiência do usuário e otimizando o desempenho do mecanismo de pesquisa.

O Django disponibiliza um painel administrativo pronto para uso, facilitando o gerenciamento de dados da aplicação, sendo gerado de forma automática a partir dos modelos definidos no projeto, além de vários outros recursos, sendo um framework completo sem a necessidade de recorrer a soluções externas.

### **<span style="color: #9A2EFE;">Bibliotecas</span>**

#### **<span style="color: #AC58FA;">Selenium</span>**
O Selenium é um conjunto de ferramentas de código aberto multiplataforma, usado para testar aplicações web pelo browser de forma automatizada. Ele executa testes de funcionalidades da aplicação web e testes de compatibilidade entre browser e plataformas diferentes. Suportando diversas linguagens de programação, como por exemplo C#, Java e Python, além de vários navegadores web como o Chrome e o Firefox.

### **<span style="color: #9A2EFE;">Banco de dados</span>**

#### **<span style="color: #AC58FA;">PostgreSQL</span>**
Escolher o PostgreSQL como banco de dados para o nosso sistema de gerenciamento de atrasos e frequência traz diversas vantagens que garantem a eficiência e a robustez do projeto.
Primeiramente, o PostgreSQL é conhecido por seu alto desempenho e escalabilidade, o que é essencial para lidar com o grande volume de dados gerados pelo sistema, incluindo registros de entrada e saída dos alunos, onde o banco de dados cresce juntamente com o aumento da quantidade de alunos ou de informações armazenadas, sem comprometer a performance.
Além disso, o PostgreSQL oferece suporte a uma ampla gama de tipos de dados, o que permite a realização de consultas complexas, possibilitando a criação de relatórios detalhados e análises aprofundadas do comportamento dos alunos, algo crucial para o acompanhamento de frequência e atrasos.

Outro ponto forte é a conformidade do PostgreSQL com o modelo ACID (Atomicidade, Consistência, Isolamento, Durabilidade), garantindo a integridade e segurança dos dados, protegendo informações sensíveis.

Por fim, a integração nativa com Django, o framework utilizado no desenvolvimento do projeto, facilita a implementação do PostgreSQL, aproveitando ao máximo suas funcionalidades avançadas.
Essas características fazem do PostgreSQL uma escolha sólida e eficiente para o sistema de gerenciamento de atrasos, oferecendo uma base confiável e segura para o projeto.

### **<span style="color: #9A2EFE;">Metodologia para o Desenvolvimento</span>**

Traduzido do inglês - Scrum é uma estrutura ágil de colaboração em equipe comumente usada no desenvolvimento de software e em outros setores. O Scrum prescreve que as equipes dividam o trabalho em metas a serem concluídas dentro de iterações com limite de tempo, chamadas sprints. Para desenvolver o projeto, utilizaremos a metodologia ágil Scrum, que nos permitirá organizar o trabalho em sprints curtos e interativos, garantindo entregas contínuas e adaptáveis.

---

## <span style="color: #8000FF;">Implementação</span>

### <span style="color: #AC58FA;">**v0.0 - Configuração do Ambiente de Desenvolvimento</span>**

Iniciamos a preparação do ambiente de desenvolvimento criando o ambiente virtual (_venv_), instalando as dependências Django e Pillow e criando o projeto. Em seguida, fizemos a instalação do PostgreSQL localmente e o configuramos como banco de dados do projeto realizando os seguintes passos:

Primeiramente, fomos na documentação oficial do [PostgreSQL](https://www.postgresql.org/download/) e em seguida, para a página do instalador [EDB](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads) na sessão de downloads e baixamos a versão 16.4 para arquitetura Windows x86-64. Posteriormente, iniciamos a pré-instalação e quando solicitado para escolher os componentes, desmarcamos a opção _Stack Builder_.

Quando necessário, inserimos a senha para o super usuário e aceitamos as configurações padrão do instalador. Após o término da instalação, demos início à configuração do servidor.
Na barra de pesquisa do Windows, buscamos por pgAdmin 4, que é uma aplicação instalada em conjunto com o PostgreSQL e permite a configuração e interação com o banco de dados com uma aparência amigável para o usuário.

Para registrar o servidor, é preciso selecionar a opção _Service_ e clicar com o botão direito sobre ela, selecionando, em seguida, a opção _Register_ e _Server_.
Na aba _General_, na opção de nome, inserimos o nome do servidor. Logo após, na aba de _Connection_, no campo _Host name/address_, digitamos o nome do host, e posteriormente, a senha que escolhemos na pré-instalação do PostgreSQL. Por fim, clicamos em _Save password_ e depois em _Save_.

Para criar uma base de dados, com o botão direito, clicamos no nome do servidor e depois em Create e Database. Na caixa de diálogo que será aberta, inserimos o nome para o banco de dados e salvamos. A base de dados já foi criada com as tabelas padrão do Django. Com ela criada, o último passo é configurar os arquivos do framework.

Com o ambiente de desenvolvimento já criado e o ambiente virtual (venv) ativado, instalamos os pacotes _psycopg_ e _python-decouple_. Digitamos os seguintes comandos no terminal:

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

Em seguida, criamos um arquivo _.env_ contendo as informações (nome, usuário, senha, host e porta) do banco de dados que não serão exibidas na documentação por motivos de segurança. Por fim, gravamos as configurações da base de dados e criamos o super usuário.

### <span style="color: #AC58FA;">v0.1 - Criação do Aplicativo</span>

Após a criação do projeto e as configurações iniciais do ambiente, criamos o aplicativo (ou módulo) dentro do diretório do projeto.

#### <span style="color: #AC58FA;">**Um projeto em Django?**</span>
O projeto é a estrutura que comportará nossos módulos e todos os demais arquivos da aplicação.

#### <span style="color: #AC58FA;">**Um módulo em Django?**</span>
Podemos facilmente exemplificar pensando num e-commerce que tenha um blog. Um dos módulos seria o e-commerce e o outro o blog, assim sendo nesta estrutura teremos um projeto e dois módulos. Em outras palavras, são aplicações que não interagem umas com as outras, mas fazem parte de um mesmo projeto.

</aside>

Posteriormente, criamos as pastas _Templates_ e _Static_, contendo os arquivos HTMl e subpastas que terá os arquivos de imagem, estilização e _JavaScript_, respectivamente. A estrutura do projeto ficou assim:

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

Com a estrutura pronta, demos início à criação das Urls e Views.

### <span style="color: #AC58FA;">v0.2 - Criação das URLs e Views</span>

Com o módulo criado, iniciamos a criação das URLs. Para isso, fizemos alguns procedimentos para configurar o projeto com o novo aplicativo, a fim de deixa-lo apto a recebe-las. Primeiro, registramos o módulo no arquivo [settings.py](http://settings.py). É importante ressaltar que todo aplicativo criado deve ser registrado para que a aplicação reconheça-o.

No arquivo `frequency_management/settings.py` :

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

Depois, criamos um arquivo chamado _[urls.py](http://urls.py)_ dentro da pasta “web”, e neste arquivo inserimos o seguinte código:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.homepage, name='homepage'),
    path('/login', views.login, name='login'),
    path('/cadastro', views.cadastro, name='cadastro'),
    path('/cursos', views.cursos, name='cursos'),
    path('/relatorio', views.relatorio, name='relatorio'),
    path('/alunos', views.alunos, name='alunos'),
]
```

Este arquivo vai conter todas as _urls_ do aplicativo. Note que importamos uma _view_, chamada homepage, que posteriormente, a criamos.

Logo após, no arquivo de urls principal, registramos as rotas do módulo criado.

No arquivo `frequency_management/web/urls.py`:

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('web.urls'))
]
```

Primeiramente, são importados alguns componentes:

- **<span style="color: #4682B4;">admin:</span>** é uma interface de administração automática que fornece uma interface poderosa para produção para adicionar conteúdo ao site
- **<span style="color: #4682B4;">path:</span>** este método cria as _urls_, recebe parâmetros como o próprio path e a _view_ ou conjunto de _views_ que serão acessadas;
- **<span style="color: #4682B4;">include:</span>** serve para incluirmos um conjunto de _views_, como é feito nas do módulo;

Este arquivo representa todas as _rotas_ do projeto (todas as criadas no módulo), onde serão importadas para o projeto a partir da linha:

```
path('', include('web.urls'))
```

Para finalizar, criamos as _views_.

No arquivo `frequency_manegement/web/views.py` :

```python
from django.shortcuts import render, redirect
from django.urls import reverse

def homepage(request):
    return render(request, 'homepage.html')

def login(request):
    return render(request, 'login.html')

def cadastro(request):
    return render(request, 'cadastro.html')

def cursos(request):
    return render(request, 'cursos.html')

def relatorio(request):
    return render(request, 'relatorio.html')
```

Com as URLs e Views criadas, demos início ao desenvolvimento das páginas.

### <span style="color: #AC58FA;">v1.0 - Início do desenvolvimento das páginas</span>

Inicialmente, desenvolvemos a página Home.

### <span style="color: #AC58FA;">Temas claro e escuro</span>

Para a estilização dos temas claro e escuro, utilizamos as ferramentas:

- **<span style="color: #4682B4;">JavaScript</span>**;
- **<span style="color: #4682B4;">HTML</span>**;
- **<span style="color: #4682B4;">CSS</span>**.

### <span style="color: #AC58FA;">Elaboração das classes</span>

A elaboração das classes foi realizada no arquivo `models.py`, como é solicitado na documentação do Django.

### <span style="color: #AC58FA;">Lógica de mostrar e esconder senha</span>

Na página de login, para o melhor desempenho do site em relação ao usuário, foi adicionada uma lógica que possibilita esconder e mostrar a senha, de acordo com a preferência de quem estiver inserindo suas informações.

Os arquivos usados para a realização dessa tarefa foram:

- **<span style="color: #4682B4;">HTML</span>** - base da parte visual, contendo os elementos (tags) responsáveis pelos itens do site.
    
- **<span style="color: #4682B4;">JavaScript</span>** - responsável pela lógica.

_**<span style="color: orange;">obs:** a estilização foi usada na tag `<style></style>` dentro do arquivo HTML._

### **<span style="color: #9A2EFE;">Passo a passo do processo:</span>**

<span style="color: #4682B4;">1- Base no HTML</span>

---

## <span style="color: #8000FF;">Manual do usuário</span>

Este manual visa auxiliar o usuário a interagir com o sistema da melhor forma possível, aproveitando ao máximo seus recursos e funcionalidades.

### <span style="color: #9A2EFE;">Iniciando</span>

Começaremos com a página inicial. Ao clicar no botão ‘login’, nos deparamos com uma página requerendo o nome e a senha do usuário. Tais dados são previamente cadastrados, de acordo com as suas informações pessoais. Ao inserir os dados corretamente, seremos direcionados a uma página.


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
