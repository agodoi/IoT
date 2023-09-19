# IoT

## Processo de automação com dispositivos inteligentes comerciais.

## Assuntos relacionados
 - Computação móvel e ubíqua --> 5G
 - Comunicação e sincronização de processos --> exemplo do NODE
 - Fundamentos de controle e automação --> malha fechada, necessidade, vantagens e desvantagens
 - Interfaces de comunicação --> WiFi, ZigBee, LoraWAN
 - Redes sem fio e IP móvel --> idem
 - Introdução, histórico e aplicações de sistemas embarcados --> História dos microconcontoladores
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

Integração e acesso na abstração de dados é necessidade de tratar um [Data Lake](https://www.alura.com.br/artigos/data-lake-conceitos-vantagens-desafios?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=111087461203&hsa_ad=645853715422&hsa_src=g&hsa_tgt=dsa-843358956400&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwjaWoBhAmEiwAXz8DBf8uOMxLgh2UV4QWoaxsF3MIKJS-tMMXg_dwNlYTRN5yb-T5NpESqBoCTBMQAvD_BwE) para que os dados se tornem informações relevantes. 

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/IoT/blob/main/imgs/dados_informacao.png">
   <img alt="Arquitetura Inicial" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/IoT/blob/main/imgs/dados_informacao.png)">
</picture>


