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

A ideia é uma plataforma chamada Sinric para simular IoT em um microcontrolador com malha fechada. Essa plataforma Sinric disponibiliza uma API para linguagem Arduino.

### Lista de material necessária:

- 01 ESP32
- 01 protoboard
- 01 LED
- 01 resistor em série com LED
- jumpers

### Objetivos da prática:

- Desenvolver um sistema de malha fechada usando API Sinric + ESP32;
- Entender o uso de microcontrolador na função de malha fechada;
- O Sinric deve ligar o LED_BUILTIN do ESP32 com a 1ª intenção **On**, mas não deve religá-lo com a 2ª intenção **On**. Em outras palavras, o ESP32 não pode mandar ligar novamente o LED_BUILTIN se ele [o LED] já estiver ligado. O ESP32 deve inibir o 2º comando **On**. Para desligar o LED_BUILTIN, você manda a intenção **Off** ou clica em **desligar** no app Sinric.

### Entendimento do funcionamento:

O ESP32 precisa ter uma malha fechada para monitorar as intenções **On** e **Off**.

O ESP32 vai se conectar com a plataforma Sinric, que por sua vez, estará integrada ao ecossistema da Alexa.

**Portanto, você vai poder dar comandos de voz através do app Alexa do seu celular ou relógio e comandar um liga-desliga de um LED.**

## Passos:

1) Acesse [Sinric](https://sinric.pro/pt-index), abra uma conta gratuita. Você tem direito a controlar 3 dispositivos gratuitamente para sempre.

2) No menu esquerdo vertical, clique em **Credenciais**.

3) No menu esquerdo vertical, clique em **Dispositivos**, no campo **Nome do dispositivo** coloque um nome curto, tipo **Luz** ou **Carro** que será o comando de voz que você dará depois. No campo **Descrição** coloque o que quiser (é obrigatório uma descrição). No campo **Tipo do dispositivo** pode deixar **switch**. No campo **Chave de aplicação**, deixa **default** e em **Sala**, deixe como **Living room**.
   
5) Cliquem em **Próxima** até aparecer **Salvar**.

6) Tome nota de 3 dados de autenticação aí num bloco de notas porque você vai precisar disso:
   
   - Identificação do dispositivo
   - Chave do App
   - Senha do App

7) Agora, pegue esse exemplo de código abaixo, crie um novo **sketch** de Arduino IDE e atualize com as credenciais recém adquiridas:

```
#ifdef ENABLE_DEBUG
       #define DEBUG_ESP_PORT Serial
       #define NODEBUG_WEBSOCKETS
       #define NDEBUG
#endif 

#include <Arduino.h>
#ifdef ESP8266 
       #include <ESP8266WiFi.h>
#endif 
#ifdef ESP32   
       #include <WiFi.h>
#endif

#include "SinricPro.h"
#include "SinricProSwitch.h"

#define WIFI_SSID         "SSID da sua rede local WiFi"    
#define WIFI_PASS         "senha caso exista"
#define APP_KEY           "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
#define APP_SECRET        "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
#define SWITCH_ID         "xxxxxxxxxxxxxxxxxxxxxxxx"
#define BAUD_RATE         9600                //Munde o baudrate para sua necessidade

#define BUTTON_PIN 0   // GPIO for BUTTON (inverted: LOW = pressed, HIGH = released)
#define LED_PIN   2   // GPIO for LED (inverted)

bool myPowerState = true;
unsigned long lastBtnPress = 0;

bool onPowerState(const String &deviceId, bool &state) {
  Serial.printf("Dispositivo %s virado para %s (via app SinricPro) \r\n", deviceId.c_str(), state?"on":"off");
  myPowerState = state;
  
  //Caso precise, desenvolva sua lógica de malha fechada aqui monitorando
  
  if (myPowerState == 1) {
    Serial.println("tentou ligar");
  }
  else {
    Serial.println("tentou desligar");
  }
  digitalWrite(LED_PIN, myPowerState?LOW:HIGH);
  return true; // pedido atendido corretamente
}


// função de conexão e configuração do WiFi
void setupWiFi() {
  Serial.printf("\r\n[Wifi]: Conectando");
  WiFi.begin(WIFI_SSID, WIFI_PASS);

  while (WiFi.status() != WL_CONNECTED) {
    Serial.printf(".");
    delay(250);
  }
  Serial.printf("conectado!\r\n[WiFi]: IP-Address: %s\r\n", WiFi.localIP().toString().c_str());
}

// Função de configuração do Sinric
void setupSinricPro() {
  // adiciona o dispositivo
  SinricProSwitch& mySwitch = SinricPro[SWITCH_ID]; //criando um objeto mySwitch

  // cria a função de retorno do dispositivo
  mySwitch.onPowerState(onPowerState); //instanciando o objeto mySwitch com a função .onPowerState

  // configurações do SinricPro
  SinricPro.onConnected([](){ Serial.printf("Conectado no Sinric\r\n"); });  //linha padrão de conexão para o Sinric
  SinricPro.onDisconnected([](){ Serial.printf("Desconectado do SinricPro\r\n"); }); //linha padrão de conexão para o Sinric
  SinricPro.begin(APP_KEY, APP_SECRET); //linha padrão de conexão para o Sinric
}

// Função principal da estrutura Arduino
void setup() {
  pinMode(BUTTON_PIN, INPUT_PULLUP); // GPIO 0 as input, pulled high
  pinMode(LED_PIN, OUTPUT); // define LED GPIO as output
  digitalWrite(LED_PIN, LOW); // turn off LED on bootup

  Serial.begin(BAUD_RATE); Serial.printf("\r\n\r\n");
  setupWiFi();
  setupSinricPro();
}

void loop() {
  SinricPro.handle(); //função padrão para manter a conexão ativa
  //Caso precise, desenvolva sua lógica de malha fechada aqui monitorando 
  Serial.println(myPowerState);


}
```

Caso precise acessar a documentação desse código, aqui estão as fontes:

https://github.com/sinricpro/esp8266-esp32-sdk/blob/master/README.md

All dependent libraries are:

https://github.com/sinricpro/esp8266-esp32-sdk/blob/master/README.md#arduinoide

https://github.com/sinricpro/esp8266-esp32-sdk/blob/master/README.md#dependencies

Full user documentation at https://sinricpro.github.io/esp8266-esp32-sdk

Visit https://github.com/sinricpro/esp8266-esp32-sdk/issues and check for existing issues or open a new one
   
9) Você precisa instalar o ESP32 na sua IDE. Na sua IDE, vá no menu principal, clique **Arquivo**, depois **Preferência** e cole na campo URL esse link **https://dl.espressif.com/dl/package_esp32_index.json**. Depois, vá no gerenciador de placas, e instale o pacote da família ESP32.

10) Adicione essas bibliocas de suporte ao **Sinric** na sua pasta padrão de libraries do Arduino IDE que geralmente fica em **user/documentos/arduino/libraries/**. [Download](https://drive.google.com/drive/folders/1rGWvi1gbaM4NJnbkaKrzHWv2EPoJwPj1?usp=sharing)

11) Agora sua missão é adaptar esse código para fazer uma malha fechada, em especial a função **bool onPowerState(const String &deviceId, bool &state)** e/ou **void loop()**. A variável que possui o status do LED é **myPowerState**.
    
