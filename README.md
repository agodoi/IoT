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

#### Exemplos de placas IoT:

- Bluetooth: alcance de até 10m, conexão segura, baixo consumo de energia, ótima taxa de transmissão, boa imunidade aos ruídos eletromagnéticos;
- ZigBee: alcance de até 40m com 1 dispositivo, mas ultrapassa centenas de metros se usado em rede Mesh ZigBee, conexão segura, recomendado para ambientes industriais, baixo consumo de energia, regular taxa de transmissão, excelente imunidade aos ruídos eletromagnéticos;
- LoRaWAN: concorrente ao celular, alcance de alguns km, conexão segura, baixo consumo de energia, regular taxa de transmissão, baixa imunidade aos ruídos eletromagnéticos;
- WiFi: alcance de até 20m, conexão segura, alto consumo de energia, excelente taxa de transmissão, baixa imunidade aos ruídos eletromagnéticos;
- 5G: alcance indeterminado (vai depender da cobertura 5G da região), médio consumo de energia, regular/ótima taxa de transmissão (vai depender da placa), boa imunidade aos ruídos eletromagnéticos.

#### Exemplos de microcontroladores:

A ordem já indica a capacidade e velocidade de processamento e se tem WiFi nativo:

- Arduino Uno (o único que não tem WiFi nativo)
- ESP 8266
- ESP 32
- Raspberry Pi Pico
- Raspberry Pi

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

### Camada 2: 

Onde estão os roteadores e gateways. Os gateways são importantíssimos, pois eles adaptam os diferentes protocolos dos end-devices ao pacote de protocolos da família TCP/IP. Aqui, o importante é garantir a intercomunicação entre os dispositivos de difentens fabricantes (o que não acontece com tanta facilidade, já que cada fabricante aposta em seu produto como sendo a melhor solução).

### Camada 3: 

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

### Camada 4:

Enquanto que no modelo OSI, a quarta camada é de Transporte, aqui no mundo do IoT entramos no Big Data.

O Big Data está intimimamente relacionado com o IoT, pois é ele que armazena os dados coletados pelos end-devices. Lembrando que os dispositivos lá da ponta, não possuem capacidade de armazenamento de informações. Portanto, em alguma camada, tem-se que armazenar esses dados. E o melhor lugar é na camada 4, pois nesse momento, os dados estão passando pela arquitetura de nuvem.

### Camada 5:

Integração e acesso na abstração de dados é necessidade de tratar e transformar um [Data Lake](https://www.alura.com.br/artigos/data-lake-conceitos-vantagens-desafios?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=111087461203&hsa_ad=645853715422&hsa_src=g&hsa_tgt=dsa-843358956400&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwjaWoBhAmEiwAXz8DBf8uOMxLgh2UV4QWoaxsF3MIKJS-tMMXg_dwNlYTRN5yb-T5NpESqBoCTBMQAvD_BwE) para que os dados se tornem informações relevantes. 

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/dados_informacao.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/dados_informacao.png)">
</picture>

Diversas fontes de dados são usadas e cruzadas no mundo IoT: sensores, cliques, fotos, posts, coordenadas de GPS, comportamentos de consumo, horários, etc.

É partir dessa camada que os dados vão auxiliar no crescimento do modelo de negócio. Exemplo: como gerenciar melhor cidades inteligentes, bem-estar na medicina, agricultura de precisão, monitoramento da natureza e ambientes, etc.

### Camada 6:

Camada da Aplicação, onde monta-se as dashboards após o tratamento dos dados. Aqui entra vários outros assuntos relacioados com UX, Machine Learnig, IA, frameworks de Big Data (Hadoop e Spark) para melhor extração e visualização de dados.

Um exemplo de dashboard para IoT é o [Ubidots](ubidots.com), como mostra a figura a seguir. Vários dados em diversos formatos de visualização para uma melhor compreensão.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/ubidots.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/ubidots.png)">
</picture>

### Camada 7:

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

# Práticas com IoT


## Prática-01: Sonoff

A ideia é usar uma API de um dispositivo muito famoso chamado Sonoff (uma combinação de Switch On Off). Essa API recebe uma intenção booleana simples: **On** ou **Off**.

Com esse On ou Off, você liga qualquer carga elétrica, tipo uma tomada automatizada por comandos de voz.

**Referência: [API eWelink](https://ewelink-api.vercel.app/docs/introduction)**

Objetivos da prática:

- Entender a mecânica da API eWelink;
- Entender o uso de microcontrolador na função de malha fechada;
- Entender 

# Passo-01:

a) Instalando a API no seu PC: abra o seu prompt de comando **CMD** no seu PC, e execute esse comando:

```
npm install ewelink-api
```

e aguarde alguns bons minutos.

b) Se der algum problema de instalação, você precisa instalar o Git no seu PC. Para isso, acesse [Git](https://git-scm.com/download/win) pegue a **64-bit Git for Windows Setup**. É um arquivo executável ***.exe**, portanto, execute-o e reinicie seu computador.

c) crie um arquivo **lista-dispositivos.js** e cole esse código:

```
const ewelink = require('ewelink-api');

/* instantiate class */
const connection = new ewelink({
  email: 'professorandregodoi@gmail.com',
  password: 'ad19052005',
  region: 'us',
});

/* get all devices */
async function listAllDevices(){
    const devices = await connection.getDevices();
    console.log(devices);
}

listAllDevices();
```

d) Crie um arquivo **package.json** e cole esse código:

```
{
  "dependencies": {
    "ewelink-api": "^3.1.1"
  }
}
```

e) Crie um arquivo **package-lock.json** e cole esse código:

```
{
  "name": "teste-minir2",
  "lockfileVersion": 2,
  "requires": true,
  "packages": {
    "": {
      "dependencies": {
        "ewelink-api": "^3.1.1"
      }
    },
    "node_modules/arpping": {
      "version": "0.3.1",
      "resolved": "git+ssh://git@github.com/skydiver/arpping.git#ae65410343bdcbddb64b37ac9f674c65af1fe92c",
      "license": "MIT",
      "dependencies": {
        "child_process": "^1.0.2",
        "os": "^0.1.1"
      }
    },
    "node_modules/array-buffer-byte-length": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/array-buffer-byte-length/-/array-buffer-byte-length-1.0.0.tgz",
      "integrity": "sha512-LPuwb2P+NrQw3XhxGc36+XSvuBPopovXYTR9Ew++Du9Yb/bx5AzBfrIsBoj0EZUifjQU+sHL21sseZ3jerWO/A==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "is-array-buffer": "^3.0.1"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/available-typed-arrays": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/available-typed-arrays/-/available-typed-arrays-1.0.5.tgz",
      "integrity": "sha512-DMD0KiN46eipeziST1LPP/STfDU0sufISXmjSgvVsoU2tqxctQeASejWcfNtxYKqETM1UxQ8sp2OrSBWpHY6sw==",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/babel-runtime": {
      "version": "6.26.0",
      "resolved": "https://registry.npmjs.org/babel-runtime/-/babel-runtime-6.26.0.tgz",
      "integrity": "sha512-ITKNuq2wKlW1fJg9sSW52eepoYgZBggvOAHC0u/CYu/qxQ9EVzThCgR69BnSXLHjy2f7SY5zaQ4yt7H9ZVxY2g==",
      "dependencies": {
        "core-js": "^2.4.0",
        "regenerator-runtime": "^0.11.0"
      }
    },
    "node_modules/bufferutil": {
      "version": "4.0.7",
      "resolved": "https://registry.npmjs.org/bufferutil/-/bufferutil-4.0.7.tgz",
      "integrity": "sha512-kukuqc39WOHtdxtw4UScxF/WVnMFVSQVKhtx3AjZJzhd0RGZZldcrfSEbVsWWe6KNH253574cq5F+wpv0G9pJw==",
      "hasInstallScript": true,
      "dependencies": {
        "node-gyp-build": "^4.3.0"
      },
      "engines": {
        "node": ">=6.14.2"
      }
    },
    "node_modules/call-bind": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/call-bind/-/call-bind-1.0.2.tgz",
      "integrity": "sha512-7O+FbCihrB5WGbFYesctwmTKae6rOiIzmz1icreWJ+0aA7LJfuqhEso2T9ncpcFtzMQtzXf2QGGueWJGTYsqrA==",
      "dependencies": {
        "function-bind": "^1.1.1",
        "get-intrinsic": "^1.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/child_process": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/child_process/-/child_process-1.0.2.tgz",
      "integrity": "sha512-Wmza/JzL0SiWz7kl6MhIKT5ceIlnFPJX+lwUGj7Clhy5MMldsSoJR0+uvRzOS5Kv45Mq7t1PoE8TsOA9bzvb6g=="
    },
    "node_modules/chnl": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/chnl/-/chnl-1.2.0.tgz",
      "integrity": "sha512-g5gJb59edwCliFbX2j7G6sBfY4sX9YLy211yctONI2GRaiX0f2zIbKWmBm+sPqFNEpM7Ljzm7IJX/xrjiEbPrw=="
    },
    "node_modules/core-js": {
      "version": "2.6.12",
      "resolved": "https://registry.npmjs.org/core-js/-/core-js-2.6.12.tgz",
      "integrity": "sha512-Kb2wC0fvsWfQrgk8HU5lW6U/Lcs8+9aaYcy4ZFc6DDlo4nZ7n70dEgE5rtR0oG6ufKDUnrwfWL1mXR5ljDatrQ==",
      "deprecated": "core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.",
      "hasInstallScript": true
    },
    "node_modules/crypto-js": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/crypto-js/-/crypto-js-4.1.1.tgz",
      "integrity": "sha512-o2JlM7ydqd3Qk9CA0L4NL6mTzU2sdx96a+oOfPu8Mkl/PK51vSyoi8/rQ8NknZtk44vq15lmhAj9CIAGwgeWKw=="
    },
    "node_modules/d": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/d/-/d-1.0.1.tgz",
      "integrity": "sha512-m62ShEObQ39CfralilEQRjH6oAMtNCV1xJyEx5LpRYUVN+EviphDgUc/F3hnYbADmkiNs67Y+3ylmlG7Lnu+FA==",
      "dependencies": {
        "es5-ext": "^0.10.50",
        "type": "^1.0.1"
      }
    },
    "node_modules/debug": {
      "version": "2.6.9",
      "resolved": "https://registry.npmjs.org/debug/-/debug-2.6.9.tgz",
      "integrity": "sha512-bC7ElrdJaJnPbAP+1EotYvqZsb3ecl5wi6Bfi6BJTUcNowp6cvspg0jXznRTKDjm/E7AdgFBVeAPVMNcKGsHMA==",
      "dependencies": {
        "ms": "2.0.0"
      }
    },
    "node_modules/define-properties": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/define-properties/-/define-properties-1.2.0.tgz",
      "integrity": "sha512-xvqAVKGfT1+UAvPwKTVw/njhdQ8ZhXK4lI0bCIuCMrp2up9nPnaDftrLtmpTazqd1o+UY4zgzU+avtMbDP+ldA==",
      "dependencies": {
        "has-property-descriptors": "^1.0.0",
        "object-keys": "^1.1.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/delay": {
      "version": "4.4.1",
      "resolved": "https://registry.npmjs.org/delay/-/delay-4.4.1.tgz",
      "integrity": "sha512-aL3AhqtfhOlT/3ai6sWXeqwnw63ATNpnUiN4HL7x9q+My5QtHlO3OIkasmug9LKzpheLdmUKGRKnYXYAS7FQkQ==",
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/es-abstract": {
      "version": "1.21.2",
      "resolved": "https://registry.npmjs.org/es-abstract/-/es-abstract-1.21.2.tgz",
      "integrity": "sha512-y/B5POM2iBnIxCiernH1G7rC9qQoM77lLIMQLuob0zhp8C56Po81+2Nj0WFKnd0pNReDTnkYryc+zhOzpEIROg==",
      "dependencies": {
        "array-buffer-byte-length": "^1.0.0",
        "available-typed-arrays": "^1.0.5",
        "call-bind": "^1.0.2",
        "es-set-tostringtag": "^2.0.1",
        "es-to-primitive": "^1.2.1",
        "function.prototype.name": "^1.1.5",
        "get-intrinsic": "^1.2.0",
        "get-symbol-description": "^1.0.0",
        "globalthis": "^1.0.3",
        "gopd": "^1.0.1",
        "has": "^1.0.3",
        "has-property-descriptors": "^1.0.0",
        "has-proto": "^1.0.1",
        "has-symbols": "^1.0.3",
        "internal-slot": "^1.0.5",
        "is-array-buffer": "^3.0.2",
        "is-callable": "^1.2.7",
        "is-negative-zero": "^2.0.2",
        "is-regex": "^1.1.4",
        "is-shared-array-buffer": "^1.0.2",
        "is-string": "^1.0.7",
        "is-typed-array": "^1.1.10",
        "is-weakref": "^1.0.2",
        "object-inspect": "^1.12.3",
        "object-keys": "^1.1.1",
        "object.assign": "^4.1.4",
        "regexp.prototype.flags": "^1.4.3",
        "safe-regex-test": "^1.0.0",
        "string.prototype.trim": "^1.2.7",
        "string.prototype.trimend": "^1.0.6",
        "string.prototype.trimstart": "^1.0.6",
        "typed-array-length": "^1.0.4",
        "unbox-primitive": "^1.0.2",
        "which-typed-array": "^1.1.9"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/es-set-tostringtag": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/es-set-tostringtag/-/es-set-tostringtag-2.0.1.tgz",
      "integrity": "sha512-g3OMbtlwY3QewlqAiMLI47KywjWZoEytKr8pf6iTC8uJq5bIAH52Z9pnQ8pVL6whrCto53JZDuUIsifGeLorTg==",
      "dependencies": {
        "get-intrinsic": "^1.1.3",
        "has": "^1.0.3",
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/es-to-primitive": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/es-to-primitive/-/es-to-primitive-1.2.1.tgz",
      "integrity": "sha512-QCOllgZJtaUo9miYBcLChTUaHNjJF3PYs1VidD7AwiEj1kYxKeQTctLAezAOH5ZKRH0g2IgPn6KwB4IT8iRpvA==",
      "dependencies": {
        "is-callable": "^1.1.4",
        "is-date-object": "^1.0.1",
        "is-symbol": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/es5-ext": {
      "version": "0.10.62",
      "resolved": "https://registry.npmjs.org/es5-ext/-/es5-ext-0.10.62.tgz",
      "integrity": "sha512-BHLqn0klhEpnOKSrzn/Xsz2UIW8j+cGmo9JLzr8BiUapV8hPL9+FliFqjwr9ngW7jWdnxv6eO+/LqyhJVqgrjA==",
      "hasInstallScript": true,
      "dependencies": {
        "es6-iterator": "^2.0.3",
        "es6-symbol": "^3.1.3",
        "next-tick": "^1.1.0"
      },
      "engines": {
        "node": ">=0.10"
      }
    },
    "node_modules/es6-iterator": {
      "version": "2.0.3",
      "resolved": "https://registry.npmjs.org/es6-iterator/-/es6-iterator-2.0.3.tgz",
      "integrity": "sha512-zw4SRzoUkd+cl+ZoE15A9o1oQd920Bb0iOJMQkQhl3jNc03YqVjAhG7scf9C5KWRU/R13Orf588uCC6525o02g==",
      "dependencies": {
        "d": "1",
        "es5-ext": "^0.10.35",
        "es6-symbol": "^3.1.1"
      }
    },
    "node_modules/es6-symbol": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/es6-symbol/-/es6-symbol-3.1.3.tgz",
      "integrity": "sha512-NJ6Yn3FuDinBaBRWl/q5X/s4koRHBrgKAu+yGI6JCBeiu3qrcbJhwT2GeR/EXVfylRk8dpQVJoLEFhK+Mu31NA==",
      "dependencies": {
        "d": "^1.0.1",
        "ext": "^1.1.2"
      }
    },
    "node_modules/ewelink-api": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/ewelink-api/-/ewelink-api-3.1.1.tgz",
      "integrity": "sha512-MJyVrEoAKFVbSJhlYeBqb6B5EFVIkMZG4L95CeF4YmjUO5/wr2mtfZkZfBwBwrJKUHqAI4qKJiTZeSXEQlzwgA==",
      "dependencies": {
        "arpping": "github:skydiver/arpping",
        "crypto-js": "^4.0.0",
        "delay": "^4.4.0",
        "node-fetch": "^2.6.1",
        "random": "^2.2.0",
        "websocket": "^1.0.32",
        "websocket-as-promised": "^1.0.1"
      }
    },
    "node_modules/ext": {
      "version": "1.7.0",
      "resolved": "https://registry.npmjs.org/ext/-/ext-1.7.0.tgz",
      "integrity": "sha512-6hxeJYaL110a9b5TEJSj0gojyHQAmA2ch5Os+ySCiA1QGdS697XWY1pzsrSjqA9LDEEgdB/KypIlR59RcLuHYw==",
      "dependencies": {
        "type": "^2.7.2"
      }
    },
    "node_modules/ext/node_modules/type": {
      "version": "2.7.2",
      "resolved": "https://registry.npmjs.org/type/-/type-2.7.2.tgz",
      "integrity": "sha512-dzlvlNlt6AXU7EBSfpAscydQ7gXB+pPGsPnfJnZpiNJBDj7IaJzQlBZYGdEi4R9HmPdBv2XmWJ6YUtoTa7lmCw=="
    },
    "node_modules/for-each": {
      "version": "0.3.3",
      "resolved": "https://registry.npmjs.org/for-each/-/for-each-0.3.3.tgz",
      "integrity": "sha512-jqYfLp7mo9vIyQf8ykW2v7A+2N4QjeCeI5+Dz9XraiO1ign81wjiH7Fb9vSOWvQfNtmSa4H2RoQTrrXivdUZmw==",
      "dependencies": {
        "is-callable": "^1.1.3"
      }
    },
    "node_modules/function-bind": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/function-bind/-/function-bind-1.1.1.tgz",
      "integrity": "sha512-yIovAzMX49sF8Yl58fSCWJ5svSLuaibPxXQJFLmBObTuCr0Mf1KiPopGM9NiFjiYBCbfaa2Fh6breQ6ANVTI0A=="
    },
    "node_modules/function.prototype.name": {
      "version": "1.1.5",
      "resolved": "https://registry.npmjs.org/function.prototype.name/-/function.prototype.name-1.1.5.tgz",
      "integrity": "sha512-uN7m/BzVKQnCUF/iW8jYea67v++2u7m5UgENbHRtdDVclOUP+FMPlCNdmk0h/ysGyo2tavMJEDqJAkJdRa1vMA==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.3",
        "es-abstract": "^1.19.0",
        "functions-have-names": "^1.2.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/functions-have-names": {
      "version": "1.2.3",
      "resolved": "https://registry.npmjs.org/functions-have-names/-/functions-have-names-1.2.3.tgz",
      "integrity": "sha512-xckBUXyTIqT97tq2x2AMb+g163b5JFysYk0x4qxNFwbfQkmNZoiRHb6sPzI9/QV33WeuvVYBUIiD4NzNIyqaRQ==",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/get-intrinsic": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/get-intrinsic/-/get-intrinsic-1.2.1.tgz",
      "integrity": "sha512-2DcsyfABl+gVHEfCOaTrWgyt+tb6MSEGmKq+kI5HwLbIYgjgmMcV8KQ41uaKz1xxUcn9tJtgFbQUEVcEbd0FYw==",
      "dependencies": {
        "function-bind": "^1.1.1",
        "has": "^1.0.3",
        "has-proto": "^1.0.1",
        "has-symbols": "^1.0.3"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/get-symbol-description": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/get-symbol-description/-/get-symbol-description-1.0.0.tgz",
      "integrity": "sha512-2EmdH1YvIQiZpltCNgkuiUnyukzxM/R6NDJX31Ke3BG1Nq5b0S2PhX59UKi9vZpPDQVdqn+1IcaAwnzTT5vCjw==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "get-intrinsic": "^1.1.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/globalthis": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/globalthis/-/globalthis-1.0.3.tgz",
      "integrity": "sha512-sFdI5LyBiNTHjRd7cGPWapiHWMOXKyuBNX/cWJ3NfzrZQVa8GI/8cofCl74AOVqq9W5kNmguTIzJ/1s2gyI9wA==",
      "dependencies": {
        "define-properties": "^1.1.3"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/gopd": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/gopd/-/gopd-1.0.1.tgz",
      "integrity": "sha512-d65bNlIadxvpb/A2abVdlqKqV563juRnZ1Wtk6s1sIR8uNsXR70xqIzVqxVf1eTqDunwT2MkczEeaezCKTZhwA==",
      "dependencies": {
        "get-intrinsic": "^1.1.3"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has/-/has-1.0.3.tgz",
      "integrity": "sha512-f2dvO0VU6Oej7RkWJGrehjbzMAjFp5/VKPp5tTpWIV4JHHZK1/BxbFRtf/siA2SWTe09caDmVtYYzWEIbBS4zw==",
      "dependencies": {
        "function-bind": "^1.1.1"
      },
      "engines": {
        "node": ">= 0.4.0"
      }
    },
    "node_modules/has-bigints": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/has-bigints/-/has-bigints-1.0.2.tgz",
      "integrity": "sha512-tSvCKtBr9lkF0Ex0aQiP9N+OpV4zi2r/Nee5VkRDbaqv35RLYMzbwQfFSZZH0kR+Rd6302UJZ2p/bJCEoR3VoQ==",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has-property-descriptors": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/has-property-descriptors/-/has-property-descriptors-1.0.0.tgz",
      "integrity": "sha512-62DVLZGoiEBDHQyqG4w9xCuZ7eJEwNmJRWw2VY84Oedb7WFcA27fiEVe8oUQx9hAUJ4ekurquucTGwsyO1XGdQ==",
      "dependencies": {
        "get-intrinsic": "^1.1.1"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has-proto": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/has-proto/-/has-proto-1.0.1.tgz",
      "integrity": "sha512-7qE+iP+O+bgF9clE5+UoBFzE65mlBiVj3tKCrlNQ0Ogwm0BjpT/gK4SlLYDMybDh5I3TCTKnPPa0oMG7JDYrhg==",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has-symbols": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has-symbols/-/has-symbols-1.0.3.tgz",
      "integrity": "sha512-l3LCuF6MgDNwTDKkdYGEihYjt5pRPbEg46rtlmnSPlUbgmB8LOIrKJbYYFBSbnPaJexMKtiPO8hmeRjRz2Td+A==",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has-tostringtag": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/has-tostringtag/-/has-tostringtag-1.0.0.tgz",
      "integrity": "sha512-kFjcSNhnlGV1kyoGk7OXKSawH5JOb/LzUc5w9B02hOTO0dfFRjbHQKvg1d6cf3HbeUmtU9VbbV3qzZ2Teh97WQ==",
      "dependencies": {
        "has-symbols": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/internal-slot": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/internal-slot/-/internal-slot-1.0.5.tgz",
      "integrity": "sha512-Y+R5hJrzs52QCG2laLn4udYVnxsfny9CpOhNhUvk/SSSVyF6T27FzRbF0sroPidSu3X8oEAkOn2K804mjpt6UQ==",
      "dependencies": {
        "get-intrinsic": "^1.2.0",
        "has": "^1.0.3",
        "side-channel": "^1.0.4"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/is-array-buffer": {
      "version": "3.0.2",
      "resolved": "https://registry.npmjs.org/is-array-buffer/-/is-array-buffer-3.0.2.tgz",
      "integrity": "sha512-y+FyyR/w8vfIRq4eQcM1EYgSTnmHXPqaF+IgzgraytCFq5Xh8lllDVmAZolPJiZttZLeFSINPYMaEJ7/vWUa1w==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "get-intrinsic": "^1.2.0",
        "is-typed-array": "^1.1.10"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-bigint": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/is-bigint/-/is-bigint-1.0.4.tgz",
      "integrity": "sha512-zB9CruMamjym81i2JZ3UMn54PKGsQzsJeo6xvN3HJJ4CAsQNB6iRutp2To77OfCNuoxspsIhzaPoO1zyCEhFOg==",
      "dependencies": {
        "has-bigints": "^1.0.1"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-boolean-object": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/is-boolean-object/-/is-boolean-object-1.1.2.tgz",
      "integrity": "sha512-gDYaKHJmnj4aWxyj6YHyXVpdQawtVLHU5cb+eztPGczf6cjuTdwve5ZIEfgXqH4e57An1D1AKf8CZ3kYrQRqYA==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-callable": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/is-callable/-/is-callable-1.2.7.tgz",
      "integrity": "sha512-1BC0BVFhS/p0qtw6enp8e+8OD0UrK0oFLztSjNzhcKA3WDuJxxAPXzPuPtKkjEY9UUoEWlX/8fgKeu2S8i9JTA==",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-date-object": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/is-date-object/-/is-date-object-1.0.5.tgz",
      "integrity": "sha512-9YQaSxsAiSwcvS33MBk3wTCVnWK+HhF8VZR2jRxehM16QcVOdHqPn4VPHmRK4lSr38n9JriurInLcP90xsYNfQ==",
      "dependencies": {
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-negative-zero": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/is-negative-zero/-/is-negative-zero-2.0.2.tgz",
      "integrity": "sha512-dqJvarLawXsFbNDeJW7zAz8ItJ9cd28YufuuFzh0G8pNHjJMnY08Dv7sYX2uF5UpQOwieAeOExEYAWWfu7ZZUA==",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-number-object": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/is-number-object/-/is-number-object-1.0.7.tgz",
      "integrity": "sha512-k1U0IRzLMo7ZlYIfzRu23Oh6MiIFasgpb9X76eqfFZAqwH44UI4KTBvBYIZ1dSL9ZzChTB9ShHfLkR4pdW5krQ==",
      "dependencies": {
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-regex": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/is-regex/-/is-regex-1.1.4.tgz",
      "integrity": "sha512-kvRdxDsxZjhzUX07ZnLydzS1TU/TJlTUHHY4YLL87e37oUA49DfkLqgy+VjFocowy29cKvcSiu+kIv728jTTVg==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-shared-array-buffer": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/is-shared-array-buffer/-/is-shared-array-buffer-1.0.2.tgz",
      "integrity": "sha512-sqN2UDu1/0y6uvXyStCOzyhAjCSlHceFoMKJW8W9EU9cvic/QdsZ0kEU93HEy3IUEFZIiH/3w+AH/UQbPHNdhA==",
      "dependencies": {
        "call-bind": "^1.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-string": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/is-string/-/is-string-1.0.7.tgz",
      "integrity": "sha512-tE2UXzivje6ofPW7l23cjDOMa09gb7xlAqG6jG5ej6uPV32TlWP3NKPigtaGeHNu9fohccRYvIiZMfOOnOYUtg==",
      "dependencies": {
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-symbol": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/is-symbol/-/is-symbol-1.0.4.tgz",
      "integrity": "sha512-C/CPBqKWnvdcxqIARxyOh4v1UUEOCHpgDa0WYgpKDFMszcrPcffg5uhwSgPCLD2WWxmq6isisz87tzT01tuGhg==",
      "dependencies": {
        "has-symbols": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-typed-array": {
      "version": "1.1.10",
      "resolved": "https://registry.npmjs.org/is-typed-array/-/is-typed-array-1.1.10.tgz",
      "integrity": "sha512-PJqgEHiWZvMpaFZ3uTc8kHPM4+4ADTlDniuQL7cU/UDA0Ql7F70yGfHph3cLNe+c9toaigv+DFzTJKhc2CtO6A==",
      "dependencies": {
        "available-typed-arrays": "^1.0.5",
        "call-bind": "^1.0.2",
        "for-each": "^0.3.3",
        "gopd": "^1.0.1",
        "has-tostringtag": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-typedarray": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/is-typedarray/-/is-typedarray-1.0.0.tgz",
      "integrity": "sha512-cyA56iCMHAh5CdzjJIa4aohJyeO1YbwLi3Jc35MmRU6poroFjIGZzUzupGiRPOjgHg9TLu43xbpwXk523fMxKA=="
    },
    "node_modules/is-weakref": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/is-weakref/-/is-weakref-1.0.2.tgz",
      "integrity": "sha512-qctsuLZmIQ0+vSSMfoVvyFe2+GSEvnmZ2ezTup1SBse9+twCCeial6EEi3Nc2KFcf6+qz2FBPnjXsk8xhKSaPQ==",
      "dependencies": {
        "call-bind": "^1.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/ms": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/ms/-/ms-2.0.0.tgz",
      "integrity": "sha512-Tpp60P6IUJDTuOq/5Z8cdskzJujfwqfOTkrwIwj7IRISpnkJnT6SyJ4PCPnGMoFjC9ddhal5KVIYtAt97ix05A=="
    },
    "node_modules/next-tick": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/next-tick/-/next-tick-1.1.0.tgz",
      "integrity": "sha512-CXdUiJembsNjuToQvxayPZF9Vqht7hewsvy2sOWafLvi2awflj9mOC6bHIg50orX8IJvWKY9wYQ/zB2kogPslQ=="
    },
    "node_modules/node-fetch": {
      "version": "2.6.11",
      "resolved": "https://registry.npmjs.org/node-fetch/-/node-fetch-2.6.11.tgz",
      "integrity": "sha512-4I6pdBY1EthSqDmJkiNk3JIT8cswwR9nfeW/cPdUagJYEQG7R95WRH74wpz7ma8Gh/9dI9FP+OU+0E4FvtA55w==",
      "dependencies": {
        "whatwg-url": "^5.0.0"
      },
      "engines": {
        "node": "4.x || >=6.0.0"
      },
      "peerDependencies": {
        "encoding": "^0.1.0"
      },
      "peerDependenciesMeta": {
        "encoding": {
          "optional": true
        }
      }
    },
    "node_modules/node-gyp-build": {
      "version": "4.6.0",
      "resolved": "https://registry.npmjs.org/node-gyp-build/-/node-gyp-build-4.6.0.tgz",
      "integrity": "sha512-NTZVKn9IylLwUzaKjkas1e4u2DLNcV4rdYagA4PWdPwW87Bi7z+BznyKSRwS/761tV/lzCGXplWsiaMjLqP2zQ==",
      "bin": {
        "node-gyp-build": "bin.js",
        "node-gyp-build-optional": "optional.js",
        "node-gyp-build-test": "build-test.js"
      }
    },
    "node_modules/object-inspect": {
      "version": "1.12.3",
      "resolved": "https://registry.npmjs.org/object-inspect/-/object-inspect-1.12.3.tgz",
      "integrity": "sha512-geUvdk7c+eizMNUDkRpW1wJwgfOiOeHbxBR/hLXK1aT6zmVSO0jsQcs7fj6MGw89jC/cjGfLcNOrtMYtGqm81g==",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/object-keys": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/object-keys/-/object-keys-1.1.1.tgz",
      "integrity": "sha512-NuAESUOUMrlIXOfHKzD6bpPu3tYt3xvjNdRIQ+FeT0lNb4K8WR70CaDxhuNguS2XG+GjkyMwOzsN5ZktImfhLA==",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/object.assign": {
      "version": "4.1.4",
      "resolved": "https://registry.npmjs.org/object.assign/-/object.assign-4.1.4.tgz",
      "integrity": "sha512-1mxKf0e58bvyjSCtKYY4sRe9itRk3PJpquJOjeIkz885CczcI4IvJJDLPS72oowuSh+pBxUFROpX+TU++hxhZQ==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "has-symbols": "^1.0.3",
        "object-keys": "^1.1.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/os": {
      "version": "0.1.2",
      "resolved": "https://registry.npmjs.org/os/-/os-0.1.2.tgz",
      "integrity": "sha512-ZoXJkvAnljwvc56MbvhtKVWmSkzV712k42Is2mA0+0KTSRakq5XXuXpjZjgAt9ctzl51ojhQWakQQpmOvXWfjQ=="
    },
    "node_modules/ow": {
      "version": "0.4.0",
      "resolved": "https://registry.npmjs.org/ow/-/ow-0.4.0.tgz",
      "integrity": "sha512-kJNzxUgVd6EF5LoGs+s2/etJPwjfRDLXPTCfEgV8At77sRrV+PSFA8lcoW2HF15Qd455mIR2Stee/2MzDiFBDA==",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/ow-lite": {
      "version": "0.0.2",
      "resolved": "https://registry.npmjs.org/ow-lite/-/ow-lite-0.0.2.tgz",
      "integrity": "sha512-5PorMvUhPJACq2HOX54idr9TkRKPhzXIEu7DlM1iiVQoKC4rR8FAJND3bkOOiyGOgq6Ve7vh32o8Pfimr7tM4Q==",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/promise-controller": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/promise-controller/-/promise-controller-1.0.0.tgz",
      "integrity": "sha512-goA0zA9L91tuQbUmiMinSYqlyUtEgg4fxJcjYnLYOQnrktb4o4UqciXDNXiRUPiDBPACmsr1k8jDW4r7UDq9Qw==",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/promise.prototype.finally": {
      "version": "3.1.4",
      "resolved": "https://registry.npmjs.org/promise.prototype.finally/-/promise.prototype.finally-3.1.4.tgz",
      "integrity": "sha512-nNc3YbgMfLzqtqvO/q5DP6RR0SiHI9pUPGzyDf1q+usTwCN2kjvAnJkBb7bHe3o+fFSBPpsGMoYtaSi+LTNqng==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/random": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/random/-/random-2.2.0.tgz",
      "integrity": "sha512-4HBR4Xye4jJ41QBi6RfIaO1yKQpxVUZafQtdE6NvvjzirNlwWgsk3tkGLTbQtWUarF4ofZsUVEmWqB1TDQlkwA==",
      "dependencies": {
        "babel-runtime": "^6.26.0",
        "ow": "^0.4.0",
        "ow-lite": "^0.0.2",
        "seedrandom": "^3.0.5"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/regenerator-runtime": {
      "version": "0.11.1",
      "resolved": "https://registry.npmjs.org/regenerator-runtime/-/regenerator-runtime-0.11.1.tgz",
      "integrity": "sha512-MguG95oij0fC3QV3URf4V2SDYGJhJnJGqvIIgdECeODCT98wSWDAJ94SSuVpYQUoTcGUIL6L4yNB7j1DFFHSBg=="
    },
    "node_modules/regexp.prototype.flags": {
      "version": "1.5.0",
      "resolved": "https://registry.npmjs.org/regexp.prototype.flags/-/regexp.prototype.flags-1.5.0.tgz",
      "integrity": "sha512-0SutC3pNudRKgquxGoRGIz946MZVHqbNfPjBdxeOhBrdgDKlRoXmYLQN9xRbrR09ZXWeGAdPuif7egofn6v5LA==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.2.0",
        "functions-have-names": "^1.2.3"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/safe-regex-test": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/safe-regex-test/-/safe-regex-test-1.0.0.tgz",
      "integrity": "sha512-JBUUzyOgEwXQY1NuPtvcj/qcBDbDmEvWufhlnXZIm75DEHp+afM1r1ujJpJsV/gSM4t59tpDyPi1sd6ZaPFfsA==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "get-intrinsic": "^1.1.3",
        "is-regex": "^1.1.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/seedrandom": {
      "version": "3.0.5",
      "resolved": "https://registry.npmjs.org/seedrandom/-/seedrandom-3.0.5.tgz",
      "integrity": "sha512-8OwmbklUNzwezjGInmZ+2clQmExQPvomqjL7LFqOYqtmuxRgQYqOD3mHaU+MvZn5FLUeVxVfQjwLZW/n/JFuqg=="
    },
    "node_modules/side-channel": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/side-channel/-/side-channel-1.0.4.tgz",
      "integrity": "sha512-q5XPytqFEIKHkGdiMIrY10mvLRvnQh42/+GoBlFW3b2LXLE2xxJpZFdm94we0BaoV3RwJyGqg5wS7epxTv0Zvw==",
      "dependencies": {
        "call-bind": "^1.0.0",
        "get-intrinsic": "^1.0.2",
        "object-inspect": "^1.9.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/string.prototype.trim": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/string.prototype.trim/-/string.prototype.trim-1.2.7.tgz",
      "integrity": "sha512-p6TmeT1T3411M8Cgg9wBTMRtY2q9+PNy9EV1i2lIXUN/btt763oIfxwN3RR8VU6wHX8j/1CFy0L+YuThm6bgOg==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/string.prototype.trimend": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/string.prototype.trimend/-/string.prototype.trimend-1.0.6.tgz",
      "integrity": "sha512-JySq+4mrPf9EsDBEDYMOb/lM7XQLulwg5R/m1r0PXEFqrV0qHvl58sdTilSXtKOflCsK2E8jxf+GKC0T07RWwQ==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/string.prototype.trimstart": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/string.prototype.trimstart/-/string.prototype.trimstart-1.0.6.tgz",
      "integrity": "sha512-omqjMDaY92pbn5HOX7f9IccLA+U1tA9GvtU4JrodiXFfYB7jPzzHpRzpglLAjtUV6bB557zwClJezTqnAiYnQA==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/tr46": {
      "version": "0.0.3",
      "resolved": "https://registry.npmjs.org/tr46/-/tr46-0.0.3.tgz",
      "integrity": "sha512-N3WMsuqV66lT30CrXNbEjx4GEwlow3v6rr4mCcv6prnfwhS01rkgyFdjPNBYd9br7LpXV1+Emh01fHnq2Gdgrw=="
    },
    "node_modules/type": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/type/-/type-1.2.0.tgz",
      "integrity": "sha512-+5nt5AAniqsCnu2cEQQdpzCAh33kVx8n0VoFidKpB1dVVLAN/F+bgVOqOJqOnEnrhp222clB5p3vUlD+1QAnfg=="
    },
    "node_modules/typed-array-length": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/typed-array-length/-/typed-array-length-1.0.4.tgz",
      "integrity": "sha512-KjZypGq+I/H7HI5HlOoGHkWUUGq+Q0TPhQurLbyrVrvnKTBgzLhIJ7j6J/XTQOi0d1RjyZ0wdas8bKs2p0x3Ng==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "for-each": "^0.3.3",
        "is-typed-array": "^1.1.9"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/typedarray-to-buffer": {
      "version": "3.1.5",
      "resolved": "https://registry.npmjs.org/typedarray-to-buffer/-/typedarray-to-buffer-3.1.5.tgz",
      "integrity": "sha512-zdu8XMNEDepKKR+XYOXAVPtWui0ly0NtohUscw+UmaHiAWT8hrV1rr//H6V+0DvJ3OQ19S979M0laLfX8rm82Q==",
      "dependencies": {
        "is-typedarray": "^1.0.0"
      }
    },
    "node_modules/unbox-primitive": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/unbox-primitive/-/unbox-primitive-1.0.2.tgz",
      "integrity": "sha512-61pPlCD9h51VoreyJ0BReideM3MDKMKnh6+V9L08331ipq6Q8OFXZYiqP6n/tbHx4s5I9uRhcye6BrbkizkBDw==",
      "dependencies": {
        "call-bind": "^1.0.2",
        "has-bigints": "^1.0.2",
        "has-symbols": "^1.0.3",
        "which-boxed-primitive": "^1.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/utf-8-validate": {
      "version": "5.0.10",
      "resolved": "https://registry.npmjs.org/utf-8-validate/-/utf-8-validate-5.0.10.tgz",
      "integrity": "sha512-Z6czzLq4u8fPOyx7TU6X3dvUZVvoJmxSQ+IcrlmagKhilxlhZgxPK6C5Jqbkw1IDUmFTM+cz9QDnnLTwDz/2gQ==",
      "hasInstallScript": true,
      "dependencies": {
        "node-gyp-build": "^4.3.0"
      },
      "engines": {
        "node": ">=6.14.2"
      }
    },
    "node_modules/webidl-conversions": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/webidl-conversions/-/webidl-conversions-3.0.1.tgz",
      "integrity": "sha512-2JAn3z8AR6rjK8Sm8orRC0h/bcl/DqL7tRPdGZ4I1CjdF+EaMLmYxBHyXuKL849eucPFhvBoxMsflfOb8kxaeQ=="
    },
    "node_modules/websocket": {
      "version": "1.0.34",
      "resolved": "https://registry.npmjs.org/websocket/-/websocket-1.0.34.tgz",
      "integrity": "sha512-PRDso2sGwF6kM75QykIesBijKSVceR6jL2G8NGYyq2XrItNC2P5/qL5XeR056GhA+Ly7JMFvJb9I312mJfmqnQ==",
      "dependencies": {
        "bufferutil": "^4.0.1",
        "debug": "^2.2.0",
        "es5-ext": "^0.10.50",
        "typedarray-to-buffer": "^3.1.5",
        "utf-8-validate": "^5.0.2",
        "yaeti": "^0.0.6"
      },
      "engines": {
        "node": ">=4.0.0"
      }
    },
    "node_modules/websocket-as-promised": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/websocket-as-promised/-/websocket-as-promised-1.1.0.tgz",
      "integrity": "sha512-agq8bPsPFKBWinKQkoXwY7LoBYe+2fQ7Gnuxx964+BTIiyAdL130FnB60bXuVQdUCdaS17R/MyRaaO4WIqtl4Q==",
      "dependencies": {
        "chnl": "^1.2.0",
        "promise-controller": "^1.0.0",
        "promise.prototype.finally": "^3.1.2"
      },
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/whatwg-url": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/whatwg-url/-/whatwg-url-5.0.0.tgz",
      "integrity": "sha512-saE57nupxk6v3HY35+jzBwYa0rKSy0XR8JSxZPwgLr7ys0IBzhGviA1/TUGJLmSVqs8pb9AnvICXEuOHLprYTw==",
      "dependencies": {
        "tr46": "~0.0.3",
        "webidl-conversions": "^3.0.0"
      }
    },
    "node_modules/which-boxed-primitive": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/which-boxed-primitive/-/which-boxed-primitive-1.0.2.tgz",
      "integrity": "sha512-bwZdv0AKLpplFY2KZRX6TvyuN7ojjr7lwkg6ml0roIy9YeuSr7JS372qlNW18UQYzgYK9ziGcerWqZOmEn9VNg==",
      "dependencies": {
        "is-bigint": "^1.0.1",
        "is-boolean-object": "^1.1.0",
        "is-number-object": "^1.0.4",
        "is-string": "^1.0.5",
        "is-symbol": "^1.0.3"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/which-typed-array": {
      "version": "1.1.9",
      "resolved": "https://registry.npmjs.org/which-typed-array/-/which-typed-array-1.1.9.tgz",
      "integrity": "sha512-w9c4xkx6mPidwp7180ckYWfMmvxpjlZuIudNtDf4N/tTAUB8VJbX25qZoAsrtGuYNnGw3pa0AXgbGKRB8/EceA==",
      "dependencies": {
        "available-typed-arrays": "^1.0.5",
        "call-bind": "^1.0.2",
        "for-each": "^0.3.3",
        "gopd": "^1.0.1",
        "has-tostringtag": "^1.0.0",
        "is-typed-array": "^1.1.10"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/yaeti": {
      "version": "0.0.6",
      "resolved": "https://registry.npmjs.org/yaeti/-/yaeti-0.0.6.tgz",
      "integrity": "sha512-MvQa//+KcZCUkBTIC9blM+CU9J2GzuTytsOUwf2lidtvkx/6gnEp1QvJv34t9vdjhFmha/mUiNDbN0D0mJWdug==",
      "engines": {
        "node": ">=0.10.32"
      }
    }
  },
  "dependencies": {
    "arpping": {
      "version": "git+ssh://git@github.com/skydiver/arpping.git#ae65410343bdcbddb64b37ac9f674c65af1fe92c",
      "from": "arpping@github:skydiver/arpping",
      "requires": {
        "child_process": "^1.0.2",
        "os": "^0.1.1"
      }
    },
    "array-buffer-byte-length": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/array-buffer-byte-length/-/array-buffer-byte-length-1.0.0.tgz",
      "integrity": "sha512-LPuwb2P+NrQw3XhxGc36+XSvuBPopovXYTR9Ew++Du9Yb/bx5AzBfrIsBoj0EZUifjQU+sHL21sseZ3jerWO/A==",
      "requires": {
        "call-bind": "^1.0.2",
        "is-array-buffer": "^3.0.1"
      }
    },
    "available-typed-arrays": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/available-typed-arrays/-/available-typed-arrays-1.0.5.tgz",
      "integrity": "sha512-DMD0KiN46eipeziST1LPP/STfDU0sufISXmjSgvVsoU2tqxctQeASejWcfNtxYKqETM1UxQ8sp2OrSBWpHY6sw=="
    },
    "babel-runtime": {
      "version": "6.26.0",
      "resolved": "https://registry.npmjs.org/babel-runtime/-/babel-runtime-6.26.0.tgz",
      "integrity": "sha512-ITKNuq2wKlW1fJg9sSW52eepoYgZBggvOAHC0u/CYu/qxQ9EVzThCgR69BnSXLHjy2f7SY5zaQ4yt7H9ZVxY2g==",
      "requires": {
        "core-js": "^2.4.0",
        "regenerator-runtime": "^0.11.0"
      }
    },
    "bufferutil": {
      "version": "4.0.7",
      "resolved": "https://registry.npmjs.org/bufferutil/-/bufferutil-4.0.7.tgz",
      "integrity": "sha512-kukuqc39WOHtdxtw4UScxF/WVnMFVSQVKhtx3AjZJzhd0RGZZldcrfSEbVsWWe6KNH253574cq5F+wpv0G9pJw==",
      "requires": {
        "node-gyp-build": "^4.3.0"
      }
    },
    "call-bind": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/call-bind/-/call-bind-1.0.2.tgz",
      "integrity": "sha512-7O+FbCihrB5WGbFYesctwmTKae6rOiIzmz1icreWJ+0aA7LJfuqhEso2T9ncpcFtzMQtzXf2QGGueWJGTYsqrA==",
      "requires": {
        "function-bind": "^1.1.1",
        "get-intrinsic": "^1.0.2"
      }
    },
    "child_process": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/child_process/-/child_process-1.0.2.tgz",
      "integrity": "sha512-Wmza/JzL0SiWz7kl6MhIKT5ceIlnFPJX+lwUGj7Clhy5MMldsSoJR0+uvRzOS5Kv45Mq7t1PoE8TsOA9bzvb6g=="
    },
    "chnl": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/chnl/-/chnl-1.2.0.tgz",
      "integrity": "sha512-g5gJb59edwCliFbX2j7G6sBfY4sX9YLy211yctONI2GRaiX0f2zIbKWmBm+sPqFNEpM7Ljzm7IJX/xrjiEbPrw=="
    },
    "core-js": {
      "version": "2.6.12",
      "resolved": "https://registry.npmjs.org/core-js/-/core-js-2.6.12.tgz",
      "integrity": "sha512-Kb2wC0fvsWfQrgk8HU5lW6U/Lcs8+9aaYcy4ZFc6DDlo4nZ7n70dEgE5rtR0oG6ufKDUnrwfWL1mXR5ljDatrQ=="
    },
    "crypto-js": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/crypto-js/-/crypto-js-4.1.1.tgz",
      "integrity": "sha512-o2JlM7ydqd3Qk9CA0L4NL6mTzU2sdx96a+oOfPu8Mkl/PK51vSyoi8/rQ8NknZtk44vq15lmhAj9CIAGwgeWKw=="
    },
    "d": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/d/-/d-1.0.1.tgz",
      "integrity": "sha512-m62ShEObQ39CfralilEQRjH6oAMtNCV1xJyEx5LpRYUVN+EviphDgUc/F3hnYbADmkiNs67Y+3ylmlG7Lnu+FA==",
      "requires": {
        "es5-ext": "^0.10.50",
        "type": "^1.0.1"
      }
    },
    "debug": {
      "version": "2.6.9",
      "resolved": "https://registry.npmjs.org/debug/-/debug-2.6.9.tgz",
      "integrity": "sha512-bC7ElrdJaJnPbAP+1EotYvqZsb3ecl5wi6Bfi6BJTUcNowp6cvspg0jXznRTKDjm/E7AdgFBVeAPVMNcKGsHMA==",
      "requires": {
        "ms": "2.0.0"
      }
    },
    "define-properties": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/define-properties/-/define-properties-1.2.0.tgz",
      "integrity": "sha512-xvqAVKGfT1+UAvPwKTVw/njhdQ8ZhXK4lI0bCIuCMrp2up9nPnaDftrLtmpTazqd1o+UY4zgzU+avtMbDP+ldA==",
      "requires": {
        "has-property-descriptors": "^1.0.0",
        "object-keys": "^1.1.1"
      }
    },
    "delay": {
      "version": "4.4.1",
      "resolved": "https://registry.npmjs.org/delay/-/delay-4.4.1.tgz",
      "integrity": "sha512-aL3AhqtfhOlT/3ai6sWXeqwnw63ATNpnUiN4HL7x9q+My5QtHlO3OIkasmug9LKzpheLdmUKGRKnYXYAS7FQkQ=="
    },
    "es-abstract": {
      "version": "1.21.2",
      "resolved": "https://registry.npmjs.org/es-abstract/-/es-abstract-1.21.2.tgz",
      "integrity": "sha512-y/B5POM2iBnIxCiernH1G7rC9qQoM77lLIMQLuob0zhp8C56Po81+2Nj0WFKnd0pNReDTnkYryc+zhOzpEIROg==",
      "requires": {
        "array-buffer-byte-length": "^1.0.0",
        "available-typed-arrays": "^1.0.5",
        "call-bind": "^1.0.2",
        "es-set-tostringtag": "^2.0.1",
        "es-to-primitive": "^1.2.1",
        "function.prototype.name": "^1.1.5",
        "get-intrinsic": "^1.2.0",
        "get-symbol-description": "^1.0.0",
        "globalthis": "^1.0.3",
        "gopd": "^1.0.1",
        "has": "^1.0.3",
        "has-property-descriptors": "^1.0.0",
        "has-proto": "^1.0.1",
        "has-symbols": "^1.0.3",
        "internal-slot": "^1.0.5",
        "is-array-buffer": "^3.0.2",
        "is-callable": "^1.2.7",
        "is-negative-zero": "^2.0.2",
        "is-regex": "^1.1.4",
        "is-shared-array-buffer": "^1.0.2",
        "is-string": "^1.0.7",
        "is-typed-array": "^1.1.10",
        "is-weakref": "^1.0.2",
        "object-inspect": "^1.12.3",
        "object-keys": "^1.1.1",
        "object.assign": "^4.1.4",
        "regexp.prototype.flags": "^1.4.3",
        "safe-regex-test": "^1.0.0",
        "string.prototype.trim": "^1.2.7",
        "string.prototype.trimend": "^1.0.6",
        "string.prototype.trimstart": "^1.0.6",
        "typed-array-length": "^1.0.4",
        "unbox-primitive": "^1.0.2",
        "which-typed-array": "^1.1.9"
      }
    },
    "es-set-tostringtag": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/es-set-tostringtag/-/es-set-tostringtag-2.0.1.tgz",
      "integrity": "sha512-g3OMbtlwY3QewlqAiMLI47KywjWZoEytKr8pf6iTC8uJq5bIAH52Z9pnQ8pVL6whrCto53JZDuUIsifGeLorTg==",
      "requires": {
        "get-intrinsic": "^1.1.3",
        "has": "^1.0.3",
        "has-tostringtag": "^1.0.0"
      }
    },
    "es-to-primitive": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/es-to-primitive/-/es-to-primitive-1.2.1.tgz",
      "integrity": "sha512-QCOllgZJtaUo9miYBcLChTUaHNjJF3PYs1VidD7AwiEj1kYxKeQTctLAezAOH5ZKRH0g2IgPn6KwB4IT8iRpvA==",
      "requires": {
        "is-callable": "^1.1.4",
        "is-date-object": "^1.0.1",
        "is-symbol": "^1.0.2"
      }
    },
    "es5-ext": {
      "version": "0.10.62",
      "resolved": "https://registry.npmjs.org/es5-ext/-/es5-ext-0.10.62.tgz",
      "integrity": "sha512-BHLqn0klhEpnOKSrzn/Xsz2UIW8j+cGmo9JLzr8BiUapV8hPL9+FliFqjwr9ngW7jWdnxv6eO+/LqyhJVqgrjA==",
      "requires": {
        "es6-iterator": "^2.0.3",
        "es6-symbol": "^3.1.3",
        "next-tick": "^1.1.0"
      }
    },
    "es6-iterator": {
      "version": "2.0.3",
      "resolved": "https://registry.npmjs.org/es6-iterator/-/es6-iterator-2.0.3.tgz",
      "integrity": "sha512-zw4SRzoUkd+cl+ZoE15A9o1oQd920Bb0iOJMQkQhl3jNc03YqVjAhG7scf9C5KWRU/R13Orf588uCC6525o02g==",
      "requires": {
        "d": "1",
        "es5-ext": "^0.10.35",
        "es6-symbol": "^3.1.1"
      }
    },
    "es6-symbol": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/es6-symbol/-/es6-symbol-3.1.3.tgz",
      "integrity": "sha512-NJ6Yn3FuDinBaBRWl/q5X/s4koRHBrgKAu+yGI6JCBeiu3qrcbJhwT2GeR/EXVfylRk8dpQVJoLEFhK+Mu31NA==",
      "requires": {
        "d": "^1.0.1",
        "ext": "^1.1.2"
      }
    },
    "ewelink-api": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/ewelink-api/-/ewelink-api-3.1.1.tgz",
      "integrity": "sha512-MJyVrEoAKFVbSJhlYeBqb6B5EFVIkMZG4L95CeF4YmjUO5/wr2mtfZkZfBwBwrJKUHqAI4qKJiTZeSXEQlzwgA==",
      "requires": {
        "arpping": "github:skydiver/arpping",
        "crypto-js": "^4.0.0",
        "delay": "^4.4.0",
        "node-fetch": "^2.6.1",
        "random": "^2.2.0",
        "websocket": "^1.0.32",
        "websocket-as-promised": "^1.0.1"
      }
    },
    "ext": {
      "version": "1.7.0",
      "resolved": "https://registry.npmjs.org/ext/-/ext-1.7.0.tgz",
      "integrity": "sha512-6hxeJYaL110a9b5TEJSj0gojyHQAmA2ch5Os+ySCiA1QGdS697XWY1pzsrSjqA9LDEEgdB/KypIlR59RcLuHYw==",
      "requires": {
        "type": "^2.7.2"
      },
      "dependencies": {
        "type": {
          "version": "2.7.2",
          "resolved": "https://registry.npmjs.org/type/-/type-2.7.2.tgz",
          "integrity": "sha512-dzlvlNlt6AXU7EBSfpAscydQ7gXB+pPGsPnfJnZpiNJBDj7IaJzQlBZYGdEi4R9HmPdBv2XmWJ6YUtoTa7lmCw=="
        }
      }
    },
    "for-each": {
      "version": "0.3.3",
      "resolved": "https://registry.npmjs.org/for-each/-/for-each-0.3.3.tgz",
      "integrity": "sha512-jqYfLp7mo9vIyQf8ykW2v7A+2N4QjeCeI5+Dz9XraiO1ign81wjiH7Fb9vSOWvQfNtmSa4H2RoQTrrXivdUZmw==",
      "requires": {
        "is-callable": "^1.1.3"
      }
    },
    "function-bind": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/function-bind/-/function-bind-1.1.1.tgz",
      "integrity": "sha512-yIovAzMX49sF8Yl58fSCWJ5svSLuaibPxXQJFLmBObTuCr0Mf1KiPopGM9NiFjiYBCbfaa2Fh6breQ6ANVTI0A=="
    },
    "function.prototype.name": {
      "version": "1.1.5",
      "resolved": "https://registry.npmjs.org/function.prototype.name/-/function.prototype.name-1.1.5.tgz",
      "integrity": "sha512-uN7m/BzVKQnCUF/iW8jYea67v++2u7m5UgENbHRtdDVclOUP+FMPlCNdmk0h/ysGyo2tavMJEDqJAkJdRa1vMA==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.3",
        "es-abstract": "^1.19.0",
        "functions-have-names": "^1.2.2"
      }
    },
    "functions-have-names": {
      "version": "1.2.3",
      "resolved": "https://registry.npmjs.org/functions-have-names/-/functions-have-names-1.2.3.tgz",
      "integrity": "sha512-xckBUXyTIqT97tq2x2AMb+g163b5JFysYk0x4qxNFwbfQkmNZoiRHb6sPzI9/QV33WeuvVYBUIiD4NzNIyqaRQ=="
    },
    "get-intrinsic": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/get-intrinsic/-/get-intrinsic-1.2.1.tgz",
      "integrity": "sha512-2DcsyfABl+gVHEfCOaTrWgyt+tb6MSEGmKq+kI5HwLbIYgjgmMcV8KQ41uaKz1xxUcn9tJtgFbQUEVcEbd0FYw==",
      "requires": {
        "function-bind": "^1.1.1",
        "has": "^1.0.3",
        "has-proto": "^1.0.1",
        "has-symbols": "^1.0.3"
      }
    },
    "get-symbol-description": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/get-symbol-description/-/get-symbol-description-1.0.0.tgz",
      "integrity": "sha512-2EmdH1YvIQiZpltCNgkuiUnyukzxM/R6NDJX31Ke3BG1Nq5b0S2PhX59UKi9vZpPDQVdqn+1IcaAwnzTT5vCjw==",
      "requires": {
        "call-bind": "^1.0.2",
        "get-intrinsic": "^1.1.1"
      }
    },
    "globalthis": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/globalthis/-/globalthis-1.0.3.tgz",
      "integrity": "sha512-sFdI5LyBiNTHjRd7cGPWapiHWMOXKyuBNX/cWJ3NfzrZQVa8GI/8cofCl74AOVqq9W5kNmguTIzJ/1s2gyI9wA==",
      "requires": {
        "define-properties": "^1.1.3"
      }
    },
    "gopd": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/gopd/-/gopd-1.0.1.tgz",
      "integrity": "sha512-d65bNlIadxvpb/A2abVdlqKqV563juRnZ1Wtk6s1sIR8uNsXR70xqIzVqxVf1eTqDunwT2MkczEeaezCKTZhwA==",
      "requires": {
        "get-intrinsic": "^1.1.3"
      }
    },
    "has": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has/-/has-1.0.3.tgz",
      "integrity": "sha512-f2dvO0VU6Oej7RkWJGrehjbzMAjFp5/VKPp5tTpWIV4JHHZK1/BxbFRtf/siA2SWTe09caDmVtYYzWEIbBS4zw==",
      "requires": {
        "function-bind": "^1.1.1"
      }
    },
    "has-bigints": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/has-bigints/-/has-bigints-1.0.2.tgz",
      "integrity": "sha512-tSvCKtBr9lkF0Ex0aQiP9N+OpV4zi2r/Nee5VkRDbaqv35RLYMzbwQfFSZZH0kR+Rd6302UJZ2p/bJCEoR3VoQ=="
    },
    "has-property-descriptors": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/has-property-descriptors/-/has-property-descriptors-1.0.0.tgz",
      "integrity": "sha512-62DVLZGoiEBDHQyqG4w9xCuZ7eJEwNmJRWw2VY84Oedb7WFcA27fiEVe8oUQx9hAUJ4ekurquucTGwsyO1XGdQ==",
      "requires": {
        "get-intrinsic": "^1.1.1"
      }
    },
    "has-proto": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/has-proto/-/has-proto-1.0.1.tgz",
      "integrity": "sha512-7qE+iP+O+bgF9clE5+UoBFzE65mlBiVj3tKCrlNQ0Ogwm0BjpT/gK4SlLYDMybDh5I3TCTKnPPa0oMG7JDYrhg=="
    },
    "has-symbols": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has-symbols/-/has-symbols-1.0.3.tgz",
      "integrity": "sha512-l3LCuF6MgDNwTDKkdYGEihYjt5pRPbEg46rtlmnSPlUbgmB8LOIrKJbYYFBSbnPaJexMKtiPO8hmeRjRz2Td+A=="
    },
    "has-tostringtag": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/has-tostringtag/-/has-tostringtag-1.0.0.tgz",
      "integrity": "sha512-kFjcSNhnlGV1kyoGk7OXKSawH5JOb/LzUc5w9B02hOTO0dfFRjbHQKvg1d6cf3HbeUmtU9VbbV3qzZ2Teh97WQ==",
      "requires": {
        "has-symbols": "^1.0.2"
      }
    },
    "internal-slot": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/internal-slot/-/internal-slot-1.0.5.tgz",
      "integrity": "sha512-Y+R5hJrzs52QCG2laLn4udYVnxsfny9CpOhNhUvk/SSSVyF6T27FzRbF0sroPidSu3X8oEAkOn2K804mjpt6UQ==",
      "requires": {
        "get-intrinsic": "^1.2.0",
        "has": "^1.0.3",
        "side-channel": "^1.0.4"
      }
    },
    "is-array-buffer": {
      "version": "3.0.2",
      "resolved": "https://registry.npmjs.org/is-array-buffer/-/is-array-buffer-3.0.2.tgz",
      "integrity": "sha512-y+FyyR/w8vfIRq4eQcM1EYgSTnmHXPqaF+IgzgraytCFq5Xh8lllDVmAZolPJiZttZLeFSINPYMaEJ7/vWUa1w==",
      "requires": {
        "call-bind": "^1.0.2",
        "get-intrinsic": "^1.2.0",
        "is-typed-array": "^1.1.10"
      }
    },
    "is-bigint": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/is-bigint/-/is-bigint-1.0.4.tgz",
      "integrity": "sha512-zB9CruMamjym81i2JZ3UMn54PKGsQzsJeo6xvN3HJJ4CAsQNB6iRutp2To77OfCNuoxspsIhzaPoO1zyCEhFOg==",
      "requires": {
        "has-bigints": "^1.0.1"
      }
    },
    "is-boolean-object": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/is-boolean-object/-/is-boolean-object-1.1.2.tgz",
      "integrity": "sha512-gDYaKHJmnj4aWxyj6YHyXVpdQawtVLHU5cb+eztPGczf6cjuTdwve5ZIEfgXqH4e57An1D1AKf8CZ3kYrQRqYA==",
      "requires": {
        "call-bind": "^1.0.2",
        "has-tostringtag": "^1.0.0"
      }
    },
    "is-callable": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/is-callable/-/is-callable-1.2.7.tgz",
      "integrity": "sha512-1BC0BVFhS/p0qtw6enp8e+8OD0UrK0oFLztSjNzhcKA3WDuJxxAPXzPuPtKkjEY9UUoEWlX/8fgKeu2S8i9JTA=="
    },
    "is-date-object": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/is-date-object/-/is-date-object-1.0.5.tgz",
      "integrity": "sha512-9YQaSxsAiSwcvS33MBk3wTCVnWK+HhF8VZR2jRxehM16QcVOdHqPn4VPHmRK4lSr38n9JriurInLcP90xsYNfQ==",
      "requires": {
        "has-tostringtag": "^1.0.0"
      }
    },
    "is-negative-zero": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/is-negative-zero/-/is-negative-zero-2.0.2.tgz",
      "integrity": "sha512-dqJvarLawXsFbNDeJW7zAz8ItJ9cd28YufuuFzh0G8pNHjJMnY08Dv7sYX2uF5UpQOwieAeOExEYAWWfu7ZZUA=="
    },
    "is-number-object": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/is-number-object/-/is-number-object-1.0.7.tgz",
      "integrity": "sha512-k1U0IRzLMo7ZlYIfzRu23Oh6MiIFasgpb9X76eqfFZAqwH44UI4KTBvBYIZ1dSL9ZzChTB9ShHfLkR4pdW5krQ==",
      "requires": {
        "has-tostringtag": "^1.0.0"
      }
    },
    "is-regex": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/is-regex/-/is-regex-1.1.4.tgz",
      "integrity": "sha512-kvRdxDsxZjhzUX07ZnLydzS1TU/TJlTUHHY4YLL87e37oUA49DfkLqgy+VjFocowy29cKvcSiu+kIv728jTTVg==",
      "requires": {
        "call-bind": "^1.0.2",
        "has-tostringtag": "^1.0.0"
      }
    },
    "is-shared-array-buffer": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/is-shared-array-buffer/-/is-shared-array-buffer-1.0.2.tgz",
      "integrity": "sha512-sqN2UDu1/0y6uvXyStCOzyhAjCSlHceFoMKJW8W9EU9cvic/QdsZ0kEU93HEy3IUEFZIiH/3w+AH/UQbPHNdhA==",
      "requires": {
        "call-bind": "^1.0.2"
      }
    },
    "is-string": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/is-string/-/is-string-1.0.7.tgz",
      "integrity": "sha512-tE2UXzivje6ofPW7l23cjDOMa09gb7xlAqG6jG5ej6uPV32TlWP3NKPigtaGeHNu9fohccRYvIiZMfOOnOYUtg==",
      "requires": {
        "has-tostringtag": "^1.0.0"
      }
    },
    "is-symbol": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/is-symbol/-/is-symbol-1.0.4.tgz",
      "integrity": "sha512-C/CPBqKWnvdcxqIARxyOh4v1UUEOCHpgDa0WYgpKDFMszcrPcffg5uhwSgPCLD2WWxmq6isisz87tzT01tuGhg==",
      "requires": {
        "has-symbols": "^1.0.2"
      }
    },
    "is-typed-array": {
      "version": "1.1.10",
      "resolved": "https://registry.npmjs.org/is-typed-array/-/is-typed-array-1.1.10.tgz",
      "integrity": "sha512-PJqgEHiWZvMpaFZ3uTc8kHPM4+4ADTlDniuQL7cU/UDA0Ql7F70yGfHph3cLNe+c9toaigv+DFzTJKhc2CtO6A==",
      "requires": {
        "available-typed-arrays": "^1.0.5",
        "call-bind": "^1.0.2",
        "for-each": "^0.3.3",
        "gopd": "^1.0.1",
        "has-tostringtag": "^1.0.0"
      }
    },
    "is-typedarray": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/is-typedarray/-/is-typedarray-1.0.0.tgz",
      "integrity": "sha512-cyA56iCMHAh5CdzjJIa4aohJyeO1YbwLi3Jc35MmRU6poroFjIGZzUzupGiRPOjgHg9TLu43xbpwXk523fMxKA=="
    },
    "is-weakref": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/is-weakref/-/is-weakref-1.0.2.tgz",
      "integrity": "sha512-qctsuLZmIQ0+vSSMfoVvyFe2+GSEvnmZ2ezTup1SBse9+twCCeial6EEi3Nc2KFcf6+qz2FBPnjXsk8xhKSaPQ==",
      "requires": {
        "call-bind": "^1.0.2"
      }
    },
    "ms": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/ms/-/ms-2.0.0.tgz",
      "integrity": "sha512-Tpp60P6IUJDTuOq/5Z8cdskzJujfwqfOTkrwIwj7IRISpnkJnT6SyJ4PCPnGMoFjC9ddhal5KVIYtAt97ix05A=="
    },
    "next-tick": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/next-tick/-/next-tick-1.1.0.tgz",
      "integrity": "sha512-CXdUiJembsNjuToQvxayPZF9Vqht7hewsvy2sOWafLvi2awflj9mOC6bHIg50orX8IJvWKY9wYQ/zB2kogPslQ=="
    },
    "node-fetch": {
      "version": "2.6.11",
      "resolved": "https://registry.npmjs.org/node-fetch/-/node-fetch-2.6.11.tgz",
      "integrity": "sha512-4I6pdBY1EthSqDmJkiNk3JIT8cswwR9nfeW/cPdUagJYEQG7R95WRH74wpz7ma8Gh/9dI9FP+OU+0E4FvtA55w==",
      "requires": {
        "whatwg-url": "^5.0.0"
      }
    },
    "node-gyp-build": {
      "version": "4.6.0",
      "resolved": "https://registry.npmjs.org/node-gyp-build/-/node-gyp-build-4.6.0.tgz",
      "integrity": "sha512-NTZVKn9IylLwUzaKjkas1e4u2DLNcV4rdYagA4PWdPwW87Bi7z+BznyKSRwS/761tV/lzCGXplWsiaMjLqP2zQ=="
    },
    "object-inspect": {
      "version": "1.12.3",
      "resolved": "https://registry.npmjs.org/object-inspect/-/object-inspect-1.12.3.tgz",
      "integrity": "sha512-geUvdk7c+eizMNUDkRpW1wJwgfOiOeHbxBR/hLXK1aT6zmVSO0jsQcs7fj6MGw89jC/cjGfLcNOrtMYtGqm81g=="
    },
    "object-keys": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/object-keys/-/object-keys-1.1.1.tgz",
      "integrity": "sha512-NuAESUOUMrlIXOfHKzD6bpPu3tYt3xvjNdRIQ+FeT0lNb4K8WR70CaDxhuNguS2XG+GjkyMwOzsN5ZktImfhLA=="
    },
    "object.assign": {
      "version": "4.1.4",
      "resolved": "https://registry.npmjs.org/object.assign/-/object.assign-4.1.4.tgz",
      "integrity": "sha512-1mxKf0e58bvyjSCtKYY4sRe9itRk3PJpquJOjeIkz885CczcI4IvJJDLPS72oowuSh+pBxUFROpX+TU++hxhZQ==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "has-symbols": "^1.0.3",
        "object-keys": "^1.1.1"
      }
    },
    "os": {
      "version": "0.1.2",
      "resolved": "https://registry.npmjs.org/os/-/os-0.1.2.tgz",
      "integrity": "sha512-ZoXJkvAnljwvc56MbvhtKVWmSkzV712k42Is2mA0+0KTSRakq5XXuXpjZjgAt9ctzl51ojhQWakQQpmOvXWfjQ=="
    },
    "ow": {
      "version": "0.4.0",
      "resolved": "https://registry.npmjs.org/ow/-/ow-0.4.0.tgz",
      "integrity": "sha512-kJNzxUgVd6EF5LoGs+s2/etJPwjfRDLXPTCfEgV8At77sRrV+PSFA8lcoW2HF15Qd455mIR2Stee/2MzDiFBDA=="
    },
    "ow-lite": {
      "version": "0.0.2",
      "resolved": "https://registry.npmjs.org/ow-lite/-/ow-lite-0.0.2.tgz",
      "integrity": "sha512-5PorMvUhPJACq2HOX54idr9TkRKPhzXIEu7DlM1iiVQoKC4rR8FAJND3bkOOiyGOgq6Ve7vh32o8Pfimr7tM4Q=="
    },
    "promise-controller": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/promise-controller/-/promise-controller-1.0.0.tgz",
      "integrity": "sha512-goA0zA9L91tuQbUmiMinSYqlyUtEgg4fxJcjYnLYOQnrktb4o4UqciXDNXiRUPiDBPACmsr1k8jDW4r7UDq9Qw=="
    },
    "promise.prototype.finally": {
      "version": "3.1.4",
      "resolved": "https://registry.npmjs.org/promise.prototype.finally/-/promise.prototype.finally-3.1.4.tgz",
      "integrity": "sha512-nNc3YbgMfLzqtqvO/q5DP6RR0SiHI9pUPGzyDf1q+usTwCN2kjvAnJkBb7bHe3o+fFSBPpsGMoYtaSi+LTNqng==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      }
    },
    "random": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/random/-/random-2.2.0.tgz",
      "integrity": "sha512-4HBR4Xye4jJ41QBi6RfIaO1yKQpxVUZafQtdE6NvvjzirNlwWgsk3tkGLTbQtWUarF4ofZsUVEmWqB1TDQlkwA==",
      "requires": {
        "babel-runtime": "^6.26.0",
        "ow": "^0.4.0",
        "ow-lite": "^0.0.2",
        "seedrandom": "^3.0.5"
      }
    },
    "regenerator-runtime": {
      "version": "0.11.1",
      "resolved": "https://registry.npmjs.org/regenerator-runtime/-/regenerator-runtime-0.11.1.tgz",
      "integrity": "sha512-MguG95oij0fC3QV3URf4V2SDYGJhJnJGqvIIgdECeODCT98wSWDAJ94SSuVpYQUoTcGUIL6L4yNB7j1DFFHSBg=="
    },
    "regexp.prototype.flags": {
      "version": "1.5.0",
      "resolved": "https://registry.npmjs.org/regexp.prototype.flags/-/regexp.prototype.flags-1.5.0.tgz",
      "integrity": "sha512-0SutC3pNudRKgquxGoRGIz946MZVHqbNfPjBdxeOhBrdgDKlRoXmYLQN9xRbrR09ZXWeGAdPuif7egofn6v5LA==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.2.0",
        "functions-have-names": "^1.2.3"
      }
    },
    "safe-regex-test": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/safe-regex-test/-/safe-regex-test-1.0.0.tgz",
      "integrity": "sha512-JBUUzyOgEwXQY1NuPtvcj/qcBDbDmEvWufhlnXZIm75DEHp+afM1r1ujJpJsV/gSM4t59tpDyPi1sd6ZaPFfsA==",
      "requires": {
        "call-bind": "^1.0.2",
        "get-intrinsic": "^1.1.3",
        "is-regex": "^1.1.4"
      }
    },
    "seedrandom": {
      "version": "3.0.5",
      "resolved": "https://registry.npmjs.org/seedrandom/-/seedrandom-3.0.5.tgz",
      "integrity": "sha512-8OwmbklUNzwezjGInmZ+2clQmExQPvomqjL7LFqOYqtmuxRgQYqOD3mHaU+MvZn5FLUeVxVfQjwLZW/n/JFuqg=="
    },
    "side-channel": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/side-channel/-/side-channel-1.0.4.tgz",
      "integrity": "sha512-q5XPytqFEIKHkGdiMIrY10mvLRvnQh42/+GoBlFW3b2LXLE2xxJpZFdm94we0BaoV3RwJyGqg5wS7epxTv0Zvw==",
      "requires": {
        "call-bind": "^1.0.0",
        "get-intrinsic": "^1.0.2",
        "object-inspect": "^1.9.0"
      }
    },
    "string.prototype.trim": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/string.prototype.trim/-/string.prototype.trim-1.2.7.tgz",
      "integrity": "sha512-p6TmeT1T3411M8Cgg9wBTMRtY2q9+PNy9EV1i2lIXUN/btt763oIfxwN3RR8VU6wHX8j/1CFy0L+YuThm6bgOg==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      }
    },
    "string.prototype.trimend": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/string.prototype.trimend/-/string.prototype.trimend-1.0.6.tgz",
      "integrity": "sha512-JySq+4mrPf9EsDBEDYMOb/lM7XQLulwg5R/m1r0PXEFqrV0qHvl58sdTilSXtKOflCsK2E8jxf+GKC0T07RWwQ==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      }
    },
    "string.prototype.trimstart": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/string.prototype.trimstart/-/string.prototype.trimstart-1.0.6.tgz",
      "integrity": "sha512-omqjMDaY92pbn5HOX7f9IccLA+U1tA9GvtU4JrodiXFfYB7jPzzHpRzpglLAjtUV6bB557zwClJezTqnAiYnQA==",
      "requires": {
        "call-bind": "^1.0.2",
        "define-properties": "^1.1.4",
        "es-abstract": "^1.20.4"
      }
    },
    "tr46": {
      "version": "0.0.3",
      "resolved": "https://registry.npmjs.org/tr46/-/tr46-0.0.3.tgz",
      "integrity": "sha512-N3WMsuqV66lT30CrXNbEjx4GEwlow3v6rr4mCcv6prnfwhS01rkgyFdjPNBYd9br7LpXV1+Emh01fHnq2Gdgrw=="
    },
    "type": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/type/-/type-1.2.0.tgz",
      "integrity": "sha512-+5nt5AAniqsCnu2cEQQdpzCAh33kVx8n0VoFidKpB1dVVLAN/F+bgVOqOJqOnEnrhp222clB5p3vUlD+1QAnfg=="
    },
    "typed-array-length": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/typed-array-length/-/typed-array-length-1.0.4.tgz",
      "integrity": "sha512-KjZypGq+I/H7HI5HlOoGHkWUUGq+Q0TPhQurLbyrVrvnKTBgzLhIJ7j6J/XTQOi0d1RjyZ0wdas8bKs2p0x3Ng==",
      "requires": {
        "call-bind": "^1.0.2",
        "for-each": "^0.3.3",
        "is-typed-array": "^1.1.9"
      }
    },
    "typedarray-to-buffer": {
      "version": "3.1.5",
      "resolved": "https://registry.npmjs.org/typedarray-to-buffer/-/typedarray-to-buffer-3.1.5.tgz",
      "integrity": "sha512-zdu8XMNEDepKKR+XYOXAVPtWui0ly0NtohUscw+UmaHiAWT8hrV1rr//H6V+0DvJ3OQ19S979M0laLfX8rm82Q==",
      "requires": {
        "is-typedarray": "^1.0.0"
      }
    },
    "unbox-primitive": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/unbox-primitive/-/unbox-primitive-1.0.2.tgz",
      "integrity": "sha512-61pPlCD9h51VoreyJ0BReideM3MDKMKnh6+V9L08331ipq6Q8OFXZYiqP6n/tbHx4s5I9uRhcye6BrbkizkBDw==",
      "requires": {
        "call-bind": "^1.0.2",
        "has-bigints": "^1.0.2",
        "has-symbols": "^1.0.3",
        "which-boxed-primitive": "^1.0.2"
      }
    },
    "utf-8-validate": {
      "version": "5.0.10",
      "resolved": "https://registry.npmjs.org/utf-8-validate/-/utf-8-validate-5.0.10.tgz",
      "integrity": "sha512-Z6czzLq4u8fPOyx7TU6X3dvUZVvoJmxSQ+IcrlmagKhilxlhZgxPK6C5Jqbkw1IDUmFTM+cz9QDnnLTwDz/2gQ==",
      "requires": {
        "node-gyp-build": "^4.3.0"
      }
    },
    "webidl-conversions": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/webidl-conversions/-/webidl-conversions-3.0.1.tgz",
      "integrity": "sha512-2JAn3z8AR6rjK8Sm8orRC0h/bcl/DqL7tRPdGZ4I1CjdF+EaMLmYxBHyXuKL849eucPFhvBoxMsflfOb8kxaeQ=="
    },
    "websocket": {
      "version": "1.0.34",
      "resolved": "https://registry.npmjs.org/websocket/-/websocket-1.0.34.tgz",
      "integrity": "sha512-PRDso2sGwF6kM75QykIesBijKSVceR6jL2G8NGYyq2XrItNC2P5/qL5XeR056GhA+Ly7JMFvJb9I312mJfmqnQ==",
      "requires": {
        "bufferutil": "^4.0.1",
        "debug": "^2.2.0",
        "es5-ext": "^0.10.50",
        "typedarray-to-buffer": "^3.1.5",
        "utf-8-validate": "^5.0.2",
        "yaeti": "^0.0.6"
      }
    },
    "websocket-as-promised": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/websocket-as-promised/-/websocket-as-promised-1.1.0.tgz",
      "integrity": "sha512-agq8bPsPFKBWinKQkoXwY7LoBYe+2fQ7Gnuxx964+BTIiyAdL130FnB60bXuVQdUCdaS17R/MyRaaO4WIqtl4Q==",
      "requires": {
        "chnl": "^1.2.0",
        "promise-controller": "^1.0.0",
        "promise.prototype.finally": "^3.1.2"
      }
    },
    "whatwg-url": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/whatwg-url/-/whatwg-url-5.0.0.tgz",
      "integrity": "sha512-saE57nupxk6v3HY35+jzBwYa0rKSy0XR8JSxZPwgLr7ys0IBzhGviA1/TUGJLmSVqs8pb9AnvICXEuOHLprYTw==",
      "requires": {
        "tr46": "~0.0.3",
        "webidl-conversions": "^3.0.0"
      }
    },
    "which-boxed-primitive": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/which-boxed-primitive/-/which-boxed-primitive-1.0.2.tgz",
      "integrity": "sha512-bwZdv0AKLpplFY2KZRX6TvyuN7ojjr7lwkg6ml0roIy9YeuSr7JS372qlNW18UQYzgYK9ziGcerWqZOmEn9VNg==",
      "requires": {
        "is-bigint": "^1.0.1",
        "is-boolean-object": "^1.1.0",
        "is-number-object": "^1.0.4",
        "is-string": "^1.0.5",
        "is-symbol": "^1.0.3"
      }
    },
    "which-typed-array": {
      "version": "1.1.9",
      "resolved": "https://registry.npmjs.org/which-typed-array/-/which-typed-array-1.1.9.tgz",
      "integrity": "sha512-w9c4xkx6mPidwp7180ckYWfMmvxpjlZuIudNtDf4N/tTAUB8VJbX25qZoAsrtGuYNnGw3pa0AXgbGKRB8/EceA==",
      "requires": {
        "available-typed-arrays": "^1.0.5",
        "call-bind": "^1.0.2",
        "for-each": "^0.3.3",
        "gopd": "^1.0.1",
        "has-tostringtag": "^1.0.0",
        "is-typed-array": "^1.1.10"
      }
    },
    "yaeti": {
      "version": "0.0.6",
      "resolved": "https://registry.npmjs.org/yaeti/-/yaeti-0.0.6.tgz",
      "integrity": "sha512-MvQa//+KcZCUkBTIC9blM+CU9J2GzuTytsOUwf2lidtvkx/6gnEp1QvJv34t9vdjhFmha/mUiNDbN0D0mJWdug=="
    }
  }
}

```

## Prática-02: Sinric

# Passo-01:

a) Acesse o site [Sinric](https://sinric.pro/) e faça o seu cadastro gratuito

b) Confirme seu cadastro acessando o seu e-mail e acesse o ambiente **Sinric**

c) No menu esquerdo, clique em Dispositivos...





