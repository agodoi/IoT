# IoT

## Processo de automação com dispositivos inteligentes comerciais.

## Assuntos relacionados
 - Computação móvel e ubíqua --> 5G OK!
 - Comunicação e sincronização de processos --> exemplo do NODE
 - Fundamentos de controle e automação --> malha fechada, necessidade, vantagens e desvantagens OK!
 - Interfaces de comunicação --> WiFi, ZigBee, LoraWAN OK!
 - Redes sem fio e IP móvel --> idem OK!
 - Introdução, histórico e aplicações de sistemas embarcados --> História dos microconcontoladores OK!
 - Invocação remota --> exemplo da tomada
 - Microcontroladores --> ESP-01... até ESP32
 - Modelagem de sistemas dinâmicos --> exemplo da Alexa
 - Programação de microcontroladores --> exemplo da Alexa
 - Sensores analógicos e digitais --> exemplo prático
 - Simulação de sistemas embarcados --> IDE e Sinric


## Comunicação Móvel e Ubíqua

A comunicação ubíqua, no contexto do IoT do Brasil é suportada oficialmente pela rede de celular 5G. 

Definição: comunicação móvel e ubíqua é a capacidade de estar conectado e se comunicar de forma contínua e onipresente em praticamente qualquer lugar e a qualquer momento, aproveitando as velocidades de transmissão de dados e a baixa latência oferecidas pela tecnologia 5G.

A latência do 5G é da ordem de 1ms.

## Pré-requisitos para um dispositivo ser IoT:

- Deve focar na economia de energia;
- Ter baixo processamento;
- Pacotes de alguns kbytes até algumas dezenas de kbytes;
- Precisa ter segurança e criptografia no payload;
- Precisa ser universal e compatível tecnologicamente, mas nem sempre isso acontece;
- Oferecer sincronismo com baixa latência;
- Oferecer a possibilidade de sleep;
- Oferecer ajuste automático da potência (alcance) para economia de energia.

## IoT em 7 camadas

Nessa sessão, vamos contruir e explicar o ecossistema IoT em 7 camadas, como uma referência ao velho amigo Modelo OSI. Se não lembra o que é Modelo OSI, clique [AQUI](https://www.alura.com.br/artigos/conhecendo-o-modelo-osi?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=111087461203&hsa_ad=645853715422&hsa_src=g&hsa_tgt=dsa-843358956400&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwjaWoBhAmEiwAXz8DBedgeYUj5V3VHeoVE5-Z9hSsrwzzzQjYkal41nFEAc1IDBSP9bZCoxoCQNEQAvD_BwE)

A imagem a seguir não é o modelo OSI tradicional, pois os nomes das camadas estão diferentes, mas sim, uma analogia, uma comparação para melhor entender as fases de um dispositivo IoT de uma ponta à outra:

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/iot-reference-model.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/iot-reference-model.png)">
</picture>

Entendendo...

### Camada 1: 

Onde estão os dispositivos físicos, os sensores, os microcontroladores, o Arduino, o ESP32, o Raspberry Pico, LoRaWAN, a Alexa, etc. Os pré-requisitos para um dispositivo ser IoT moram nessa camada.

#### História do microcontrolador

A história dos microcontroladores é uma jornada fascinante que abrange várias décadas e reflete o avanço constante da tecnologia na área da eletrônica embarcada. Os microcontroladores são dispositivos compactos e altamente integrados que incorporam CPU (Unidade Central de Processamento), memória, periféricos de entrada e saída, e muitas vezes um sistema operacional dedicado. Eles desempenham um papel crucial em uma ampla gama de aplicações, desde eletrodomésticos até veículos autônomos e dispositivos médicos. Vamos explorar a evolução dos microcontroladores ao longo do tempo:

**Década de 1970: Os Primeiros Passos**
- A história dos microcontroladores começa nos anos 1970, quando os primeiros dispositivos microcontroladores foram desenvolvidos por empresas como Intel e Texas Instruments.
- Esses microcontroladores eram bastante simples em termos de capacidade de processamento e memória, geralmente usando arquiteturas de 4 bits e 8 bits.
- Eles eram usados principalmente em aplicações simples, como relógios digitais, calculadoras e alguns sistemas de controle industrial.

**Década de 1980: A Expansão da Complexidade**
- Nos anos 1980, houve um rápido avanço na complexidade dos microcontroladores. Arquiteturas de 16 bits e 32 bits começaram a aparecer.
- A introdução de memória flash programável permitiu que os desenvolvedores carregassem facilmente software nos microcontroladores, tornando-os mais flexíveis e adaptáveis.
- Os microcontroladores agora eram usados em uma variedade de aplicações, incluindo sistemas automotivos, dispositivos de comunicação e eletrodomésticos inteligentes.

**Década de 1990: Popularização e Proliferação**
- A década de 1990 viu uma ampla adoção de microcontroladores em diversas indústrias. Eles se tornaram componentes essenciais em eletrônicos de consumo, sistemas de automação industrial e dispositivos médicos.
- A capacidade de processamento continuou a aumentar, e os microcontroladores se tornaram mais poderosos, permitindo a execução de tarefas mais complexas.
- A integração de periféricos como conversores analógico-digitais (ADCs), interfaces de comunicação e timers tornou os microcontroladores ainda mais versáteis.

**Década de 2000: A Era da Conectividade**
- Com o surgimento da Internet e das redes de comunicação sem fio, os microcontroladores evoluíram para atender às demandas da conectividade.
- Surgiram microcontroladores dedicados à IoT (Internet das Coisas), que incluíam recursos como Wi-Fi, Bluetooth e conectividade de rede.
- Isso abriu as portas para a criação de dispositivos inteligentes interconectados, desde termostatos até câmeras de segurança e assistentes pessoais.

**Década de 2010 e Além: Microcontroladores de Alto Desempenho**
- Nos últimos anos, a evolução dos microcontroladores continuou com uma ênfase em desempenho e eficiência de energia.
- Microcontroladores de 32 bits e 64 bits se tornaram padrão em muitas aplicações.
- A integração de sensores avançados, acelerômetros, giroscópios e unidades de processamento de sinal digital (DSP) tornou-os ideais para aplicações como dispositivos de realidade virtual e automação residencial.

A evolução dos microcontroladores continua a um ritmo acelerado, impulsionada pelo avanço da tecnologia de semicondutores e pela demanda por dispositivos cada vez mais inteligentes e conectados. À medida que a IoT, a inteligência artificial e a automação desempenham papéis cada vez mais importantes em nossas vidas, os microcontroladores continuarão desempenhando um papel central na transformação da maneira como interagimos com o mundo ao nosso redor.

#### Exemplos de microcontroladores:

A ordem já indica a capacidade e velocidade de processamento e se tem WiFi nativo:

- Arduino Uno (o único que não tem WiFi nativo)
- ESP 8266
- ESP 32
- Raspberry Pi Pico
- Raspberry Pi

#### Exemplos de acesso IoT:

**Microcontrolador +**

- Bluetooth: alcance de até 10m, conexão segura, baixo consumo de energia, ótima taxa de transmissão, boa imunidade aos ruídos eletromagnéticos;
- ZigBee: alcance de até 40m com 1 dispositivo, mas ultrapassa centenas de metros se usado em rede Mesh ZigBee, conexão segura, recomendado para ambientes industriais, baixo consumo de energia, regular taxa de transmissão, excelente imunidade aos ruídos eletromagnéticos;
- LoRaWAN: concorrente ao celular, alcance de alguns km, conexão segura, baixo consumo de energia, regular taxa de transmissão, baixa imunidade aos ruídos eletromagnéticos;
- WiFi: alcance de até 20m, conexão segura, alto consumo de energia, excelente taxa de transmissão, baixa imunidade aos ruídos eletromagnéticos;
- 5G: alcance indeterminado (vai depender da cobertura 5G da região), médio consumo de energia, regular/ótima taxa de transmissão (vai depender da placa), boa imunidade aos ruídos eletromagnéticos.

## Camada 2: 

Onde estão os roteadores e gateways. Os gateways são importantíssimos, pois eles adaptam os diferentes protocolos dos end-devices ao pacote de protocolos da família TCP/IP. Aqui, o importante é garantir a intercomunicação entre os dispositivos de difentens fabricantes (o que não acontece com tanta facilidade, já que cada fabricante aposta em seu produto como sendo a melhor solução).

## Camada 3: 

Aqui tem-se a Computação Edge (borda) e Fog (névoa). A computação de borda e névoa são modelos de computação distribuída que visa melhorar o desempenho e a eficiência de sistemas de computação e redes, especialmente em ambientes de Internet das Coisas (IoT). Aqui vale pontuar diferenças entre Computação de Borda e Computação Névoa:

A computação de borda (edge computing) e a computação de névoa (fog computing) são duas abordagens distintas para lidar com a computação em ambientes de Internet das Coisas (IoT). Embora ambas se concentrem em trazer processamento e armazenamento mais próximos dos dispositivos de IoT e dos usuários finais, elas têm algumas diferenças importantes:

**I. Localização dos Recursos Computacionais:**

   - **Computação de Borda (Edge Computing):** A computação de borda coloca os recursos computacionais diretamente nos dispositivos de borda, como sensores, câmeras, gateways IoT e outros dispositivos de IoT. Ela é altamente descentralizada e opera "na borda" da rede, próxima aos dispositivos.

   - **Computação de Névoa (Fog Computing):** A computação de névoa coloca os recursos computacionais em locais mais próximos dos dispositivos de borda, mas não necessariamente diretamente neles. Ela opera em pontos intermediários entre os dispositivos de borda e a nuvem, como servidores ou pontos de acesso na rede local.

**2. Escopo de Processamento:**

   - **Computação de Borda:** A computação de borda lida principalmente com o processamento local nos dispositivos de borda. Ela é adequada para tarefas que exigem baixa latência, alta velocidade de processamento e processamento de dados em tempo real diretamente nos dispositivos. Exemplo: [Coral](https://coral.ai/).

   - **Computação de Névoa:** A computação de névoa lida com uma variedade de tarefas, incluindo o processamento de dados na própria névoa, a coordenação de tarefas entre dispositivos de borda e a nuvem e a agregação de dados de vários dispositivos de borda antes de enviá-los para a nuvem. Ela atua como uma camada intermediária de processamento.

**3. Latência e Eficiência de Rede:**

   - **Computação de Borda:** A computação de borda é ideal quando a latência mínima é crítica, pois reduz a necessidade de enviar dados pela rede. Ela economiza largura de banda e melhora a eficiência da rede.

   - **Computação de Névoa:** A névoa também ajuda a reduzir a latência, mas pode envolver alguma comunicação de dados pela rede, especialmente quando a coordenação entre dispositivos é necessária. No entanto, ela geralmente é mais eficiente em termos de largura de banda do que o envio de todos os dados diretamente para a nuvem.

**4. Flexibilidade e Escalabilidade:**

   - **Computação de Borda:** A computação de borda pode ser altamente distribuída e escalável, mas requer recursos computacionais em cada dispositivo de borda. Isso pode ser desafiador em termos de gerenciamento em ambientes com muitos dispositivos.

   - **Computação de Névoa:** A computação de névoa é mais flexível em termos de dimensionamento, uma vez que os recursos de névoa podem ser compartilhados entre vários dispositivos de borda. Isso facilita o gerenciamento e a escalabilidade.

## Camada 4:

Enquanto que no modelo OSI, a quarta camada é de Transporte, aqui no mundo do IoT entramos no Big Data.

O Big Data está intimimamente relacionado com o IoT, pois é ele que armazena os dados coletados pelos end-devices. Lembrando que os dispositivos lá da ponta, não possuem capacidade de armazenamento de informações. Portanto, em alguma camada, tem-se que armazenar esses dados. E o melhor lugar é na camada 4, pois nesse momento, os dados estão passando pela arquitetura de nuvem.

## Camada 5:

Integração e acesso na abstração de dados é necessidade de tratar e transformar um [Data Lake](https://www.alura.com.br/artigos/data-lake-conceitos-vantagens-desafios?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=111087461203&hsa_ad=645853715422&hsa_src=g&hsa_tgt=dsa-843358956400&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwjaWoBhAmEiwAXz8DBf8uOMxLgh2UV4QWoaxsF3MIKJS-tMMXg_dwNlYTRN5yb-T5NpESqBoCTBMQAvD_BwE) para que os dados se tornem informações relevantes. 

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/dados_informacao.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/dados_informacao.png)">
</picture>

Diversas fontes de dados são usadas e cruzadas no mundo IoT: sensores, cliques, fotos, posts, coordenadas de GPS, comportamentos de consumo, horários, etc.

É partir dessa camada que os dados vão auxiliar no crescimento do modelo de negócio. Exemplo: como gerenciar melhor cidades inteligentes, bem-estar na medicina, agricultura de precisão, monitoramento da natureza e ambientes, etc.

## Camada 6:

Camada da Aplicação, onde monta-se as dashboards após o tratamento dos dados. Aqui entra vários outros assuntos relacioados com UX, Machine Learnig, IA, frameworks de Big Data (Hadoop e Spark) para melhor extração e visualização de dados.

Um exemplo de dashboard para IoT é o [Ubidots](ubidots.com), como mostra a figura a seguir. Vários dados em diversos formatos de visualização para uma melhor compreensão.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/ubidots.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/ubidots.png)">
</picture>

## Camada 7:

É nessa camada que se justifica o investimento de todo o ecossistema IoT. O IoT precisa suportar o modelo de negócio para manter o investimento contínuo.

Se o IoT não faz o negócio crescer, então não faz sentido adotá-lo.

Portanto, nessa camada, tem-se o envolvimento de pessoas, de processos, de diferentens áreas de conhecimento (jurídica, medicinal, TI, engenharia, política, social, etc). Todos envolvidos em pró de um conforto e bem-estar humano, animal e ambiental.

## Fundamentos de Controle e Automação

Dispostivos IoT atuam na área de automação e controle de forma direta. 

E um item importantíssimo no Controle e Automação é a **malha fechada** (ou sistema de controle em malha fechada). 

Trata-se da medição e o ajuste contínuo de um processo com base em informações de retorno.

Veja a figura a seguir para melhor entender o que é **malha aberta** e **malha fechada**.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/malhas.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/malhas.png)">
</picture>

Explicação:

1. **Controlador:** é um componente crítico de um sistema de controle em malha fechada. Ele recebe feedback do processo ou sistema controlado e toma decisões para ajustar as saídas e manter o sistema próximo ao valor desejado (setpoint). Na prática, o controlador é um microcontrolador.

2. **Setpoint:** é o valor desejado para a variável controlada. O controlador compara o *setpoint* com o feedback atual do sistema e calcula o erro, que é a diferença entre eles.

3. **Erro:** O erro é a diferença entre o valor do *setpoint* e o valor real ou medido do processo. O controlador usa o erro para tomar decisões sobre como ajustar as saídas.

4. **Feedback (ou Retroalimentação):** A retroalimentação refere-se às informações contínuas e em tempo real sobre o estado do processo que são fornecidas ao controlador. Essas informações ajudam o controlador a tomar decisões de controle.

5. **Ação de Controle:** A ação de controle é a resposta do controlador para corrigir o erro. Pode ser uma mudança nas variáveis de controle, como ajuste de válvulas, aumento ou redução de potência, etc.

6. **Loop de Controle:** O loop de controle é a estrutura completa de um sistema de controle em malha fechada, que inclui o processo ou sistema controlado, o sensor de feedback, o controlador e os atuadores que realizam a ação de controle.

7. **Sistema de Controle PID:** O controle PID (Proporcional-Integral-Derivativo) é um dos métodos mais comuns usados em sistemas de controle em malha fechada. Ele combina três componentes - proporção, integral e derivativo - para ajustar a ação de controle com base no erro e na história passada do erro.

8. **Tempo de Resposta:** O tempo de resposta é a medida de quanto tempo leva para o sistema de controle em malha fechada atingir uma resposta estável após uma perturbação.

9. **Estabilidade:** A estabilidade é uma característica crítica de sistemas de controle em malha fechada. Um sistema é considerado estável quando, após uma perturbação, ele retorna ao estado desejado sem oscilações excessivas ou instabilidade.

10. **Malha Fechada vs. Malha Aberta:** Em sistemas de malha fechada, o feedback é usado para ajustar continuamente o sistema com base nas condições reais. Em sistemas de malha aberta, não há feedback; os comandos são enviados sem levar em consideração o estado real do sistema.

## Pergunta - 01: o projeto em que você está envolvido agora, possui malha aberta ou malha fechada?

## Pergunta - 02: seu projeto precisa de malha fechada?

## 10 min para o grupo discutir e apresentar uma resposta.

# Prática com IoT

A ideia é usar uma API chamada Sonoff (uma combinação de Switch On Off). Essa API recebe uma intenção booleana simples: **On** ou **Off** e ativa um relé interno da caixinha que por sua vez, libera 127V.

Com esse On ou Off, você liga qualquer carga elétrica, tipo uma tomada automatizada por comandos de voz.

**Referência: [API eWelink](https://ewelink-api.vercel.app/docs/introduction)**

### Objetivos da prática:

- Desenvolver um sistema de malha fechada usando API eWeLink + Arduino Uno;
- Entender o uso de microcontrolador na função de malha fechada;
- O Sonoff deve ligar o LED_BUILTIN com a intenção **On**, mas não deve desligá-lo com o **Off**. O Arduino não pode mandar ligar novamente o LED_BUILTIN se ele [o LED] já estiver ligado. O Arduino deve inibir o 2º comando **On**. Para desligar o LED_BUILTIN, você pressionar o reset do Arduino.

### Entendimento:

O fato do Arduino não permitir religar o LED, é uma malha fechada, porque o Arduino vai monitorar a *input* de 5V.

### Material necessário:

- 01 tomada Sonoff;
- 01 Arduino Uno;
- 01 fonte de 5V;
- fios e conectores já na bancada.

### Limitação:

Apenas 1 celular por vez consegue se conectar com o dispositivo Sonoff. Cada bancada possui 3 Sonoff, portanto, organizem-se em dupla (ou trio em alguns casos).

# Passos:

a) Crie uma pasta no seu PC onde a API será instalada. Sugestão: use nome de pasta sem acentos, espaços ou caracteres especiais.

b) Abra o seu prompt de comando **CMD** no seu PC, entre na pasta recém criada, e instale a API eWeLink:

```
npm install ewelink-api
```

e aguarde alguns bons minutos.

b.1) Se der algum problema de instalação, você precisa instalar o Git no seu PC. Para isso, acesse [Git](https://git-scm.com/download/win) pegue a **64-bit Git for Windows Setup**. É um arquivo executável ***.exe**, portanto, execute-o e reinicie seu computador.

c) Para começar a usar a tomada automatizada, precisa-se adicioná-la no seu perfil do eWeLink. Então, você precisa criar um perfil no eWeLink. Por meio do seu celular, baixe e instale o app **eWeLink Smart Home** usando a loja oficial de apps e crie uma conta no app.

d) Para adicionar a tomada Sonoff no seu perfil faça o seguinte:

d.1) Pressione o botão branco da caixinha por 5s até o LED azul piscar  2 x 1 (tipo * * __ * * __). Solte o botão, e pressione novamente para entrar em modo de piscada contínuo * * * * * ...

d.2) Conecte o seu celular no WiFi local. Pode ser com senha ou sem senha.

d.3) Agora, vá no seu app eWeLink e sinal de **+** no canto direito superior, depois clique em **adicionar dispositivo**.

d.4) Clique em **próximo** e daí vai aparecer o nome **SONOFF MINI**

d.5) Mude o WiFi do seu celular, para **ITEAD-100XXXXXX** clicando no botão **Ir para conexão**. E use a senha padrão **12345678** quando lhe solicitar. O que você está fazendo é se conectando via WiFi exclusivo da caixinha para autenticar seu end-device com seu app. Cuidado que pode aparecer um **pop-up** lhe pedindo uma confirmação de conexão.

d.6) Volta para app eWeLink e você terá um giro de 0 a 100% indicando quase o fim do processo de emparelhamento, isto é, o device estará pronto para uso. Caso não esteja habilitado, tire-o da tomada e retorne e aguarde uns instantes para ele se conectar no WiFi local.

d.7) Qualquer etapa que refizer, remova o device da tomada antes para zerar a memória e feche e abra seu app eWeLink.


e) A partir de agora, você criará vários arquivos java para rodar a API, onde todos os arquivos precisam estar numa mesma pasta. Portanto, comece criando uma pasta **inteli** qualquer e armazene os arquivos a seguir: 

e.1) Crie um arquivo **lista-dispositivos.js** e cole esse código e preencha com o e-mail e senha que cadastrou no app:

```
const ewelink = require('ewelink-api');

/* instantiate class */
const connection = new ewelink({
  email: 'seu e-mail', //**ALTERAR**
  password: 'sua senha', //**ALTERAR**
  region: 'us',
});

/* get all devices */
async function listAllDevices(){
    const devices = await connection.getDevices();
    console.log(devices);
}

listAllDevices();
```

e.2) Crie um arquivo **pega-dados-dispositivos.js** e cole esse código. Altere os valores das variáveis indicadas:

```
const ewelink = require('ewelink-api');

/* instantiate class */
const connection = new ewelink({
  email: 'seu email', //**ALTERAR**
  password: 'sua senha', //**ALTERAR**
  region: 'us',
});

/* get all devices */
async function listDeviceInfo(deviceId){
    const devices = await connection.getDevice(deviceId);
    console.log(devices);
}

listDeviceInfo('coloque seu ID do DISPOSTIVO'); //Pegue esse ID nos 3 pontinhos de configurações do seu SONOFF MINI
```

e.3) Crie um arquivo **pega-estado-dispositivos.js** e cole esse código. Altere os valores das variáveis indicadas:

```
const ewelink = require('ewelink-api');
const myDeviceId = 'ID do seu device' //**ALTERAR**

/* instantiate class */
const connection = new ewelink({
  email: 'e-mail', //**ALTERAR**
  password: 'senha', //**ALTERAR**
  region: 'us',
});

/* get all devices */
async function listDeviceInfo(deviceId){
    const status = await connection.getDevicePowerState(deviceId);
    console.log(status);
}

//listDeviceInfo(myDeviceId);
console.log(listDeviceInfo(myDeviceId));

//Retorno
// { status: 'ok', state: 'off', channel: 1 }
```

e.4) Crie um arquivo **seta-estado-dispositivo.js** e cole esse código. Altere os valores das variáveis indicadas:

```
const ewelink = require('ewelink-api');
const myDeviceId = 'coloque seu ID do DISPOSTIVO' //**ALTERAR**

/* instantiate class */
const connection = new ewelink({
  email: 'e-mail', //**ALTERAR**
  password: 'senha', //**ALTERAR**
  region: 'us',
});

/* get all devices */
async function listDeviceInfo(deviceId){
    const status = await connection.setDevicePowerState(deviceId, 'toggle'); //**ALTERAR** 'on', 'of' ou 'toggle'
    console.log(status);
}

listDeviceInfo(myDeviceId);

//Retorna o estado que foi a modificação enviada para o dispositivo
//Estados: 'on', 'off', 'toggle'
```

Entendendo as ligações elétricas, sua tomada eWeLink está energizada na tomada da bancada, e essa tomada eWeLink está energizando uma fonte de bancada de saída de 5V. A saída de 5V está se comportando como **On** e **Off** para o Arduino Uno.

Ligue o Arduino Uno na porta USB do seu PC. Agora, desenvolveremos uma lógica que se comporte como malha fechada.

### Lógica:

O Sonoff deve ligar o LED_BUILTIN com a intenção **On**, mas não deve desligá-lo com o **Off**. O Arduino não pode mandar ligar novamente o LED_BUILTIN se ele [o LED] já estiver ligado. O Arduino deve inibir o 2º comando **On**. Para desligar o LED_BUILTIN, você pressionar o reset do Arduino. 

Nossa missão agora é: desenvolver um projetinho em Arduino que se comporte como malha fechada do tipo:

**você deve inibir uma segunda intenção caso o LED_Builtin da placa Uno já esteja aceso**

- Usando o loop infinito, monitore o pino que está recebendo o 5V;
- Caso seja Off, não ative o LED_BUILTIN;
- Caso seja True, ative o LED_BUILTIN;
  - Caso seja True 2x, não ative o LED_BUILTIN.
  - Para desligar o LED, pressione o reset da placa.

### Código Arduino:

f) Esse código é um início e está incompleto. A partir dele, o grupo deve elaborar um algoritmo em Arduino que execute a lógica solicitada.

```
#define pinoEntrada 3 //pino fonte 5V conectada

void setup() {
  Serial.begin(9600); //indica o baudrate da comunicação serial do Arduino IDE
  pinMode(LED_BUILTIN, OUTPUT); //indica a função do pino do LED
  pinMode(LED_BUILTIN, LOW); //inicia o LED apagado
  
  // put your setup code here, to run once:

}

void loop() {
  bool entradaBool = digitalRead(pinoEntrada); //captura dados do pino
  if(entradaBool == True){ //testa o status do pinoEntrada
    digitalWrite(LED_BUILTIN, HIGH); //liga LED_BUILTIN se True
    Serial.println("Mensagem X"); //imprime mensagem no Monitor Serial
  }
  else{
    digitalWrite(LED_BUILTIN, LOW); //desliga LED_BUILTIN se false
    Serial.println("Mensagem Y"); //imprime mensagem no Monitor Serial
  }
  //elabore o seu código
}
```

g) Após finalizar seu código Arduino, execute o programa Java: dentro da pasta raiz do seu projeto no CMD, digite **node lista-dispositivos.js** [enter]

h) Quando você manda o comando On Off pelo prompt CMD, o que acontece no Monitor Serial do Arduino?
