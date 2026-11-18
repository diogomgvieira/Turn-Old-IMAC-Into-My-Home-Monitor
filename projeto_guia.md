# 🖥️ Projeto: Conversão de iMac 27" (2011) em Monitor Externo

## 1. Porquê fazer este projeto? (Viabilidade e Comparação de Preços)

Um iMac de 27 polegadas antigo perde rapidamente suporte de software e capacidade de processamento para tarefas modernas, mas mantém um chassis de alumínio maquinado, colunas estéreo de boa qualidade e um painel IPS excelente (`2560×1440` QHD no modelo de 2011). Em vez de enviar o equipamento para reciclagem ou gastar centenas de euros num monitor novo com construção em plástico, converter o iMac permite obter um monitor de 27" com acabamento *premium* e suporte ergonómico integrado por uma fração do custo de mercado:

* **Conversão DIY (iMac 27" existente):** ~60 € – 120 € (apenas placa controladora, fonte, cabos e peças 3D).
* **Monitores 27" QHD (2K) equivalentes novos (ex: Dell UltraSharp / LG):** ~280 € – 450 €.
* **Apple Studio Display (27" 5K):** ~1.779 € (preço base oficial).

### O que é uma Placa Controladora (*Driver / Controller Board*)?
A placa controladora é o "cérebro" que substitui toda a *logic board* original do computador. Recebe sinais de vídeo padrão modernos (HDMI, DisplayPort ou USB-C) vindos de um portátil ou PC e converte-os no protocolo nativo que o painel LCD interno do iMac entende (**LVDS** no modelo de 2011; **eDP** nos modelos 5K), gerindo também a alimentação da retroiluminação (*backlight*), o menu de brilho/cor (OSD) e a amplificação de áudio.

---

## 2. Lista de Compras (*Bill of Materials*)

> Preenche a coluna **Link** à medida que fores escolhendo os fornecedores (AliExpress, eBay, Amazon, etc.). Confirma sempre o código exato na etiqueta traseira do teu painel LCD antes de encomendar.

| Componente | Especificação Técnica (iMac 27" 2011 - A1312) | Custo Est. | Link |
| :--- | :--- | :---: | :--- |
| **Placa Controladora (*Driver Board*)** | Compatível com painel `LM270WQ1` (confirmar sub-variante exata na etiqueta traseira do LCD) | ~35 € – 45 € | `[Inserir Link]` |
| **Fonte de Alimentação 12V** | Transformador DC 12V (5A a 7A), ficha 5.5mm × 2.5mm (centro positivo) — ou fonte industrial Meanwell | ~12 € – 20 € | `[Inserir Link]` |
| **Placa *Crossover* de Áudio** | Módulo para ligar as 2 colunas estéreo internas originais do iMac à saída de som da controladora | ~8 € – 10 € | `[Inserir Link]` |
| **Suporte Traseiro Impresso em 3D** | *iMac Studio Display Mod* (`iMac_RAM_Cover_Rear.stl` + `iMac_RAM_Cover_Buttons_and_DP_USB_C.stl`) impresso em **ABS ou ASA** | ~15 € – 24 € | `[Inserir Link]` |
| **Cabos *Panel-Mount* Curtos** | 1x HDMI macho-fêmea (com rosca de painel) + 1x DisplayPort macho-fêmea (~30 cm) | ~12 € – 18 € | `[Inserir Link]` |
| **Contrapesos de Equilíbrio** | ~650g de pesos adesivos de calibragem de rodas (compensa o peso da *motherboard* e GPU removidas na mola do pé) | ~5 € | `[Inserir Link]` |
| **Arrefecimento (Opcional/Avançado)** | Controlador PWM 12V com sensor termístor (para reaproveitar a ventoinha centrífuga original da Apple) | ~6 € – 10 € | `[Inserir Link]` |
| **Isolamento e Consumíveis** | Espaçadores adesivos de nylon (*PCB standoffs*), fita Kapton (alta temp.) e ligadores termorretráteis com solda (*solder seal*) | ~5 € – 8 € | `[Inserir Link]` |
| **Ferramentas Necessárias** | Ventosas (para o vidro magnético), chaves Torx (T8, T10), ferro de soldar e pistola de ar quente | Já tenho | — |

---

## 3. Guia Passo a Passo de Montagem e Soldadura

### ⚠️ Precauções de Segurança Antes de Começar
1. **Condensadores da Fonte Original (PSU):** Mesmo desligado da tomada, nunca toques nas pistas expostas da fonte de alimentação original do iMac ao desmontá-la; os condensadores retêm cargas elétricas perigosas.
2. **Isolamento Elétrico:** Nunca deixes a parte traseira da placa controladora, do transformador ou da placa de botões tocar diretamente no alumínio do chassis ou na traseira metálica do LCD (risco imediato de curto-circuito).
3. **Escolha de Filamento 3D:** O interior do chassis fechado aquece bastante. Peças impressas em **PLA ou PETG podem deformar com o calor**; usa sempre **ABS ou ASA** para os suportes internos e tampa da RAM.

---

### Passo 1: Abertura e Identificação do Painel (Vantagem do Modelo 2011)
* **Ação:** Ao contrário dos modelos 2012+ (colados com fita adesiva), no teu **iMac 27" de 2011** basta usar ventosas para puxar o vidro frontal magnético e desaparafusar os parafusos Torx que seguram o painel LCD. Desliga cuidadosamente os cabos *ribbon* e pousa o LCD virado para baixo numa toalha macia.
* **Verificação:** Lê a etiqueta branca na traseira do painel LCD e confirma a variante exata (ex: `LM270WQ1(SD)(E3)`) antes de encomendar a placa controladora.

### Passo 2: Esvaziar o Chassis (*Gutting*)
* **Ação:** Seguindo o guia do iFixit para o iMac 27" Mid 2011, remove a *logic board*, a fonte de alimentação original, o disco rígido, o leitor ótico (*SuperDrive*) e a cablagem interna desnecessária.
* **O que manter:** Deixa intactos no chassis **as duas colunas estéreo originais**, **o botão físico de ligar/desligar**, **a tomada de alimentação AC traseira** e (opcionalmente) **a ventoinha centrífuga original**.

### Passo 3: Teste de Bancada (Obrigatório Antes de Fechar)
* **Ação:** Com o painel LCD fora do chassis, liga o cabo de vídeo da placa controladora (atenção à orientação: ponto branco virado para cima, se aplicável) e o cabo de retroiluminação (*backlight*, fio vermelho do lado correto). Liga a fonte de 12V e um computador via HDMI ou DisplayPort.
* **Verificação:** O LED da placa de controlo (OSD) acende e o monitor exibe imagem estável na resolução nativa (`2560×1440` a 60Hz).

### Passo 4: Integração Elétrica e Soldadura (Abordagem "Studio Display Mod")
Para evitar transformadores externos e cabos soltos pela traseira, faz a integração interna:

1. **Fonte de Alimentação 12V Interna (*Caseless* ou Industrial):**
   * Abre cuidadosamente a caixa plástica do transformador de 12V que alimenta a placa controladora (reduz o volume ocupado e melhora a dissipação térmica dentro do alumínio) — ou usa uma fonte metálica compacta tipo Meanwell.
   * Envolve a base da placa da fonte com **fita Kapton** (isolante térmico/elétrico) e fixa-a no interior do chassis (antes de recolocar a coluna esquerda, caso interfira com os pontos de fixação).
   * Descarna os fios da entrada AC (230V) da tomada original do iMac e une-os diretamente aos terminais de entrada AC da fonte de 12V usando solda e manga retrátil (ou ligadores termorretráteis com anel de solda no interior).
2. **Reutilização do Botão *Power* Original do iMac:**
   * Na pequena placa de botões (OSD) que acompanha a controladora, identifica o interruptor correspondente ao botão **Power** (geralmente o último botão da fila).
   * Dessolda/remove esse botão físico da placa OSD (ou descarna os dois fios correspondentes no cabo *ribbon*).
   * Faz a emenda (*splice*) e soldadura desses dois fios diretamente aos dois contactos do botão físico original de alumínio na traseira do iMac (não tem polaridade, funciona como contacto momentâneo). Isola as soldaduras com manga retrátil.
3. **Áudio Interno (*Crossover*):**
   * Liga os fios das colunas esquerda e direita do iMac à pequena placa *crossover* e conecta a saída desta à ficha de áudio da placa controladora. *(Nota: verifica a polaridade dos fios das colunas, pois alguns kits chineses vêm com os fios invertidos de fábrica).*
4. **Arrefecimento Silencioso (Opcional):**
   * Se quiseres ligar a ventoinha original da Apple a um controlador PWM de 12V com termístor (programado para arrancar suavemente acima dos 30 °C junto à fonte), tem atenção à ordem invertida dos pinos da ficha da Apple (olhando para o lado cobreado, da esquerda para a direita: **PWM, Controlo/Tacómetro, Terra/GND, Voltagem/12V**).

### Passo 5: Montagem das Portas Traseiras em 3D (Tampa da RAM)
* **Ação:** Retira a tampa metálica original da memória RAM na traseira inferior do iMac e encaixa a peça impressa em 3D (`iMac_RAM_Cover_Rear.stl` + módulo de portas e botões).
* **Montagem:** Aparafusa as extremidades fêmea dos cabos curtos *panel-mount* (HDMI e DisplayPort) nos respetivos encaixes da peça 3D (usando *inserts* roscados de latão para maior durabilidade) e encaixa a placa OSD (agora sem o botão *power*) no alojamento dos botões.

### Passo 6: Fixação, Contrapesos e Fecho Final
* **Fixação:** Cola 4 espaçadores adesivos de nylon (*standoffs*) nos furos da placa controladora e fixa-a na traseira plana do painel LCD (ou no fundo do chassis), garantindo zero contacto com metal. Organiza os cabos internos com abraçadeiras.
* **Calibragem da Mola do Pé (Contrapesos):** Ao remover a *motherboard*, dissipadores e discos, o chassis perde bastante peso e a mola interna do suporte pode puxar o ecrã excessivamente para trás. Cola **~650g de contrapesos** (pesos adesivos de calibragem de jantes) na zona inferior interna abaixo da dobradiça para restaurar o equilíbrio original.
* **Fecho:** Liga todas as fichas à controladora, encaixa o painel LCD no chassis, aperta novamente os parafusos Torx originais e coloca o vidro frontal magnético no sítio.

---

## 💡 Curiosidades Técnicas (iMacs como Monitores)

* **Porque é que a Apple matou o *Target Display Mode* nos iMacs 5K?** Nos modelos até 2013/2014 (como o teu de 2011), era possível usar o iMac como monitor externo via cabo Mini DisplayPort/Thunderbolt através do *Target Display Mode*. Quando a Apple lançou o primeiro iMac 5K (`5120×2880`) em 2014, **nenhum cabo único no mercado tinha largura de banda suficiente** para transmitir 5K a 60Hz. A solução de engenharia da Apple foi criar um controlador interno proprietário (*Timing Controller*) que dividia o ecrã ao meio e enviava dois fluxos DisplayPort 1.2 simultâneos para cada metade do painel — o que tornou tecnicamente impossível receber sinal de vídeo externo pela porta Thunderbolt.
* **A Evolução Oculta dos Painéis LG da Apple:** Nem todos os painéis de 27" usados pela Apple são iguais:
  * *2011 (2K):* Painel IPS de 2560×1440 com retroiluminação LED de excelente fidelidade sRGB, muito valorizado por não ter o vidro laminado ao LCD (facilitando reparações e limpeza).
  * *2014 (5K):* Limitado a gama sRGB (~400 nits) e conhecido por sofrer de retenção temporária de imagem (*ghosting*).
  * *2015 (5K):* Introduziu a gama de cores DCI-P3, mas manteve o brilho abaixo dos 400 nits e desenvolveu frequentemente o fenómeno das "bordas rosadas" (*pink edges*) com o envelhecimento.
  * *2017 e 2019 (5K):* O "ponto doce" dos painéis usados — atingem **500 nits** de brilho (um salto real de 43% face a 2015), ficando muito próximos dos 600 nits do atual Apple Studio Display.
* **O Desafio do Áudio nos Modelos com Chip T2:** Nos iMac Pro (2017) e iMac 27" (2020), reutilizar as colunas internas numa conversão DIY é muito mais complexo do que nos modelos anteriores (como o teu de 2011), porque a Apple passou a fazer a separação de frequências (*crossover* entre *woofers* e *tweeters*) via software dentro do chip de segurança T2 em vez de usar circuitos analógicos simples.
* **Placas 5K Modernas com *Current Booster*:** As placas controladoras mais recentes para painéis 5K (como a **SA1**, baseada em chip MediaTek) não só permitem 5K a 60Hz por um único cabo USB-C com **90W de Power Delivery** (carregando um MacBook Pro enquanto transmite imagem e som), como incluem um circuito *current booster* capaz de puxar o brilho do painel até cerca de **550 nits**.