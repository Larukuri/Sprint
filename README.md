# Tema: Segurança de redes: Conheça as vulnerabilidades de servidores e clientes
## 1. O que é um ataque DDoS e como posso me proteger?
**DDoS** é a sigla para *Distributed Denial of Service*, traduzindo do inglês seria algo como: Negação de Serviço Distribuído, é um tipo de ataque que gera uma sobrecarga num servidor deixando sites lentos ou indisponíveis.
Esse ataque usa diversos computadores que foram infectados anteriormente para serem controlados e direcionados a vítima (no caso um servidor). São muitas máquinas tentando acessar um mesmo site gerando uma sobrecarga no sistema que deixa o alvo indisponível, fora do ar.
Como os computadores infectados, chamados de *botnets*, estão em diversos locais espalhados, fica mais difícil de identificar pois o servidor acredita serem IP's válidos de pessoas de verdade tentando acessar o site. Apesar de ser difícil essa identificação de Ip's como válidos ou não, existem algumas formas de se proteger desses de ataques:
-Escolher servidores com um boa largura de banda. Servidores com uma largura de banda pequena não conseguem suprir muitos acessos ao mesmo tempo, então mesmo que você não esteja sob ataque considere ter uma largura de banda grande para um cenário onde várias pessoas estejam tentando acessar o seu site. No caso de um ataque seria necessário ter uma quantidade considerável de *botnets* para sobrecarregar o seu servidor.
-Usar um *firewall* que gerencia as conexões, um *firewall* pode gerenciar as solicitações de conexão ao seu site impedindo uma grande quantidade de acessos de origens duvidosas, por exemplo se seu site é um *e-commerce* brasileiro que está sendo acessado por diversos computadores localizados em diferentes países o seu firewall pode barrar esses IP's.
-Usar um sistema *reCAPTCHA*. Integrando esse sistema no seu site, que obriga o usuário a clicar em imagens, você garante que quem está tentando acessar o seu site é de fato um usuário.
-Ter vários servidores de acesso. Quando separamos estrategicamente os componentes de serviço em servidores diferentes mesmo que um dos componentes esteja sob ataque isso não vai prejudicar os demais.
Proteção nunca é demais, mas é importante estudar caso a caso para entender qual a melhor estratégia de ser usada em cada situação e para isso é imprescindível ser orientado por um profissional especializado.

Referências utilizadas:
https://www.hostinger.com.br/tutoriais/o-que-e-ddos-e-como-se-proteger-de-ataques
https://cursos.alura.com.br/course/seguranca-redes

## 2. Por que o firewall é uma ferramenta muito importante de proteção?
É um equipamento que separa nosa rede em seguranças distintas, ele pode estar embutido no roteador ou ser um equipamento dedicado. Ele pode separar a parte interna da rede bloqueando um tráfego que tem origem de fora de entrar na rede interna.

# Tema: Git e GitHub
## 3. Explique de forma sucinta, o fluxo e envio de um arquivo novo para o repositório do projeto.
    O fluxo é uma forma de organização das ramificações do *git* que facilita o fluxo de trabalho dos desenvolvedores. Ele atribui funções específicas para cada *branch* e define quando elas devem interagir (merge, rebase)
    Para cada alteração feita em um projeto podemos enviá-la para o nosso repositório, o *git* vai armazenar essas "versões" do trabalho e permitir que se navegue entre elas. Dentro do repositório o *git* armazena apenas as mudanças feitas e não o arquivo inteiro como forma de poupar memória.
    Para enviar um arquivo para um repositório, podemos seguir o seguinte passo a passo:
    -Abrir o *Git Bash*;
    -**mkdir meuprojeto** (para criar um novo repositório com o nome meu projeto);
    -**cd meuprojeto** (para entrar no repositório meuprojeto);
    -**git init** (para criar o repositório *git* nessa pasta);
    -Criar um arquivo e colocá-lo na pasta meuprojeto;
    -**ls** (para ver a lista de arquivos na pasta);
    -**git status** (para verificar o estatus dos arquivos na pasta);
    -**git add nomedoarquivo** (os arquivos vão para o estado *Stage*);
    - deve-se usar o **git add –all** quando se quer deixar todos as arquivos da pasta em *Staged*;
    -**git commit** (os arquivos passam do estado *Staged* para *commitados)*.
    -pronto, seu arquivo já está dentro do repositório.


## 4. Descreva sobre os ganhos de se utilizar a funcionalidade da branch do git.
    As *branches* são uma forma de garantir uma linha de desenvolvimento que não impacte diretamente na *branch master*, ela permite que toda a equipe trabalhe simultaneamente em um mesmo projeto sem interferências e ao final podem juntar as partes para uma release. Podemos ter por exemplo uma branch separada apenas para correção de *bugs* que servirá tanto para uma versão já lançada como para dar continuidade ao projeto. 

## 5. Explique a diferença entre criar o repositório na nuvem e iniciar o repositório a partir de um código existente local.
    Quando criamos o repositório na nuvem os arquivos ali podem já ficar disponíveis para outros colaboradores e você pode acessá-los de outros locais e computadores. Quando o repositório é local os arquivos ficam armazenados na sua máquina e corre-se o risco de perde-los caso seu computador ou HD tenha algum problema, o ideal é adiciona-los posteriormente em um servidor online como o *git hub*.


## 6. Qual a diferença entre Git e GitHub?
    O *Git* é um sistema de controle de versionamentos, o *Github* é um repositório online onde você pode compartilhar e carregar seus arquivos, ele possui ferramentas que usam o *Git*.

#Tema: Fundamentos de Agilidade: seus primeiros passos para a transformação ágil
## 7. Quais as principais diferenças entre o modelo ágil e o waterfall (modelo em cascata)?
    *Waterfall* é o método tradicional de trabalho usado principalmente nas engenharias tradicionais, é dividido em etapas e cada etapa dependa da aprovação da anterior para avançar.
    Já o modelo ágil prioriza uma entrega rápida que desde o início agrega valor para o cliente, ele consegue se adequar mais rapidamente a mudanças e vai avançando conforme uma lista de prioridades. Além disso, possui *feedbacks* constantes que ajudam a equipe a evoluírem o projeto na direção correta.

# 8. Quais são as 3 perguntas que devem ser respondidas na daily?
    -O que você fez desde a última *daily* ?
    -O que você pretende fazer até a próxima *daily*?
    -Você teve algum impedimento?

## 9. Qual o intuito das seguintes cerimônias?
    • Daily:
    Atualizar a todos sobre o andamento das tarefas que estão sendo executadas de forma a evitar retrabalho e informar algum problema que está tendo para ser resolvido após a *daily*. 
    • Planning:
    É a primeira reunião no início de uma *sprint*, o *P.O.* começa apresentado o *product backlog* para a equipe começando com o item de maior prioridade, os desenvolvedores tiram dúvidas sobre o produto e quebram ele em itens menores e técnicos. Nessa reunião é decidido quais itens vão entrar na próxima *sprint*.
    • Refinamento
    Cabe ao *Product Owner* manter o *product backlog* e fazer o seu refinamento, ou seja, pegar os itens do *product backlog* e transformá-los em histórias que possuem uma complexidade e tamanho menores.
    • Review:
    A reunião de *review* é quando o time apresenta para o cliente e se possível um usuário tudo o que ficou pronto durante a *sprint* e recebe um *feedback* positivo ou negativo, é uma forma de o time medir se está indo para a direção correta.
    • Retrospectiva:
    É o último *timebox* dentro da *Sprint*, é o momento em que todo o time se reúne para levantar os pontos positivos e negativos da *sprint* e dessa forma manter o conceito de melhoria contínua. É importante que a lista de itens a fazer que sai dessa reunião contenha apenas ações e não reclamações, o time deve encontrar uma ação a se tomar para os problemas encontrados.

## 10. O que é a estimativa na metodologia ágil?
	É um cálculo aproximado do esforço do time para realizar uma determinada tarefa 

# Tema: Fundamentos HTTP
## 11. O que é o protocolo HTTP? Qual a diferença entre HTTP e HTTPS?
	**HTTP** = *HiperText Transfer Protocol* ou um Protocolo de Comunicação, basicamente é um conjunto de regras utilizadas para a comunicação entre cliente e servidor.
	O **HTTPS** é o **HTTP** + **SSL/TLS** (*Secure Sockets Layer/ Transport Layer Security*), o S significa a adição de uma camada extra de proteção nos dados, uma vez que o HTTP transporta o texto puro. O HTTPS funciona de forma criptografada dando mais segurança na comunicação entre cliente-servidor.

## 12. Cite 4 métodos HTTP.
	GET – para pesquisa (receber dados)
	POST - para adiciona dados no servidor
	DELETE – para apagar dados
	PUT/PATCH – para atualizar um dado
