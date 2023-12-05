# HealthConnect + IOT device


 <h2>Problema:</h2>
 <p>A má conexão entre médicos e pacientes pode resultar em atrasos no atendimento, falta de coordenação de cuidados, dificuldade no compartilhamento de informações, perda de dados cruciais e ineficiência na gestão de ocorrências. O HealthConnect surge como uma solução para esses problemas, proporcionando uma conexão eficiente que agiliza o atendimento, melhora a coordenação de cuidados e facilita o compartilhamento de informações, contribuindo para uma prestação de serviços de saúde mais eficaz e ágil.</p>


<h2>Solução:</h2>
 
  <p>O HealthConnect veio com uma solução abrangente que utiliza o ESP32, sensores de pulso, temperatura e acelerômetro para fornecer monitoramento contínuo e em tempo real. Este dispositivo compacto e portátil é capaz de medir os batimentos cardíacos, a temperatura corporal, proporcionando informações cruciais para intervenções médicas oportunas.</p>


 <h3>Componentes</h3>
    <p>Para implementar a solução você precisará dos seguintes componentes que estão distribuídos em duas etapas, são elas a etapa física e virtual. Para a etapa física, será necessário:</p>
    
  | Componente                                              
  |---------------------------------------------------------|
  | Pulse Generator                                  
  | MP6050 - Acelerometro que mede Temepratura                                          
  | Display SSD1306                                                  
  | Real Time Clocker (RTC)                                            
  | ESP32                                                   
  | Fio microUSB para ligar o ESP                            
  | Protoboard                                              
   
 ![image](https://github.com/tavaloper/HealthConnect-IOT-device/blob/main/MontagemHealthConnection.png)
 
 <h2>Tecnologia usada e como iniciar o projeto</h2>
   
   <p>Para esse projeto, utilizamos a IDE do arduino para programar o ESP32, desse modo, toda a linguagem é em c++. Entretanto, primeiramente é preciso instalar o pacote do ESP32 da espressif. Agora para a aplicação do Fiware, ela é toda configurada em python para enviar os dados para o banco de dados;</p>
   <p>Para toda a configuração da Tela OLED e acelerômetro, utilizamos as bibliotecas disponíveis na IDE do arduino, como: Adafruit GFX Library, Adafruit SSD1306 e Adafruit MPU6050, já para configurar o sistema a internet e protocolo mqtt utilizamos a biblioteca PubSubClient(by nick o'lary). Terminado isso basta utilizar o códigos que disponibilizamos e gravar o código no ESP32.</p>
 
  <h2>Simulação no WOKWI</h2>
    <p>Wokwi é uma plataforma online que oferece simuladores de hardware para desenvolvimento e teste de projetos eletrônicos. Pensando nisso, foi realizado o mesmo projeto no WOKWI, para facilitar a compreensão e caso não seja possível a reprodução física.</p>
    <p>Caso queira verificar a simulação acesse esse link https://wokwi.com/projects/382307797964312577 ou Clique <a href="https://wokwi.com/projects/382307797964312577">aqui </a> 
  
  
  <h3>Referências</h3>
 <p>Buscando mais informações e aprimoramento, nossas referências foram:</p>
     <ol><li>Link: https://github.com/fabiocabrini/fiware</li>
         <li>Link: https://www.hapvida.com.br/site/</li>


# HealthConnect.py
[**Clique Aqui**](https://youtu.be/bQw-vOarQqo) para acessar o video de demonstracao

**Execute o arquivo tela_inicial.py**

## Processo de Cadastro

### Médicos

Médicos devem fornecer as seguintes informações durante o cadastro:

- Nome Completo
- Idade
- CPF
- CEP
- Hospital de Atuação ou Último Hospital Trabalhado
- Número de Telefone
- Senha

Após o cadastro, o software fornecerá um ID exclusivo que será usado para realizar o login na plataforma.

### Usuários Comuns

Usuários comuns devem fornecer as seguintes informações durante o cadastro:

- Nome Completo
- Idade
- CPF
- CEP
- Número de Telefone
- Senha

## Processo de Login

**Médicos:** O login é realizado com o ID fornecido durante o cadastro do médico e a senha escolhida anteriormente.

**Usuários Comuns:** O login é feito com o CPF do usuário e a senha escolhida anteriormente.

## Funcionalidades para Usuários Comuns

### 1. Ver Histórico de Ocorrências

Os usuários comuns podem visualizar um histórico detalhado de todas as ocorrências e atendimentos médicos anteriores que solicitaram.

### 2. Cadastrar Nova Ocorrência

Permite que os usuários registrem uma nova ocorrência, tornando-a visível para vários médicos. Essa funcionalidade visa proporcionar uma rápida conexão entre pacientes e profissionais de saúde.

## Funcionalidades para Médicos

### 1. Ver Histórico de Ocorrências

Médicos têm acesso ao histórico completo de todas as ocorrências e atendimentos que realizaram. Isso inclui detalhes relevantes sobre cada caso.

### 2. Nova Ocorrência

#### Buscar Ocorrências Ativas

Médicos podem visualizar todas as ocorrências ativas postadas por usuários comuns, facilitando a identificação de casos que necessitam de atendimento urgente.

#### Cadastrar Ocorrência do Zero

Permite que os médicos cadastrem manualmente uma nova ocorrência, independentemente de ter sido postada por um usuário comum. Neste caso, os médicos precisam preencher informações essenciais, como dados do paciente, nível de emergência e detalhes da ocorrência.

## Ocorrências Ativas

Para médicos, as ocorrências ativas ficam disponíveis com informações como CPF do usuário solicitante, número de celular e detalhes da ocorrência. Essa funcionalidade visa facilitar a rápida identificação e contato com os pacientes para atendimento imediato.

## Resolução de Ocorrências

Quando uma ocorrência é resolvida, o usuário comum tem a opção de marcá-la como solucionada, indicando o ID do médico responsável. Isso atualiza automaticamente o histórico tanto do paciente quanto do médico.

### Conclusão

O HealthConnect busca transformar a interação entre pacientes e médicos, proporcionando uma abordagem eficiente e transparente para o gerenciamento de ocorrências médicas. Sua interface intuitiva e funcionalidades específicas para cada tipo de usuário garantem uma experiência otimizada na área da saúde.

       
