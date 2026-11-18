# 🖥️ Projeto DIY: Conversão de iMac 27" em Monitor Externo

## 💡 Porquê fazer este projeto? (Viabilidade e Comparação de Mercado)

Os iMacs de 27 polegadas (mesmo os modelos mais antigos, como o de 2011 com resolução 2K `2560x1440`, ou os modelos Retina 5K) estão equipados com painéis IPS fabricados pela LG de qualidade excepcional, excelente reprodução de cores e um chassis de alumínio e vidro icónico. Quando o hardware interno (CPU, GPU ou *logic board*) fica obsoleto ou avaria, o ecrã continua perfeitamente funcional, mas acaba frequentemente desperdiçado como lixo eletrónico.

Para transformar este painel num monitor independente, utiliza-se uma **Placa Controladora LCD (*LCD Controller / Driver Board*)**. Na prática, esta placa substitui toda a *logic board* do Mac: recebe sinais de vídeo padrão de qualquer computador moderno (via HDMI, DisplayPort ou USB-C), descodifica-os e converte-os para o protocolo nativo do painel LCD da Apple (LVDS nos modelos de 2011 ou eDP nos modelos 5K), gerindo também a alimentação da retroiluminação (*backlight*) e o menu de controlo (brilho, contraste, seleção de entrada).

**Comparação de Custos:**
* **Custo desta conversão:** Entre **80 € e 130 €** em peças (assumindo que já tens o iMac).
* **Alternativas modernas equivalentes no mercado:** Um monitor moderno de 27" com construção em alumínio/vidro, painel IPS de alta precisão cromática e colunas integradas — como o **Apple Studio Display** (cerca de **1.799 €**) ou alternativas profissionais de gama alta como o **LG UltraFine** ou **ASUS ProArt** (entre **500 € e 900 €**) — custa facilmente **5 a 15 vezes mais** do que o investimento necessário para dar uma segunda vida ao teu iMac.

---

## 🛒 Lista de Compras (Shopping List)

> *Preenche os campos `[Link]` à medida que fores escolhendo os fornecedores (AliExpress, eBay, Amazon, etc.). Confirma sempre o código exato na etiqueta traseira do teu painel LCD (ex: `LM270WQ1` para 2011 2K ou `LM270QQ1` para 5K) antes de encomendar a placa.*

### Eletrónica Principal
* [ ] **Placa Controladora LCD (*Driver Board*) + Cabo LVDS/eDP + Teclado OSD:** [Inserir Link Aqui] — *Nota: Deve corresponder exatamente à sub-variante da etiqueta do painel.*
* [ ] **Fonte de Alimentação DC 12V (5A a 7A, ficha 5.5x2.5mm centro positivo):** [Inserir Link Aqui] — *(Muitas vezes vem incluída no kit da placa controladora).*

### Cabos e Conectividade (Escolher consoante a abordagem)
* [ ] **Cabos de Extensão Macho-Fêmea (30–45 cm) — Abordagem Simples:**
  * Cabo DisplayPort: [Inserir Link Aqui]
  * Cabo HDMI: [Inserir Link Aqui]
  * Cabo Extensão DC 12V (se a fonte ficar fora): [Inserir Link Aqui]
* [ ] **Cabos *Panel-Mount* (Aparafusáveis) — Abordagem Acabamento Limpo (3D):**
  * Cabo DisplayPort *Panel-Mount*: [Inserir Link Aqui]
  * Cabo HDMI *Panel-Mount*: [Inserir Link Aqui]

### Áudio e Acabamento Estético (Opcional / Recomendado)
* [ ] **Placa *Crossover* / Amplificador de Áudio (para reutilizar as colunas originais do iMac):** [Inserir Link Aqui]
* [ ] **Tampa Traseira da RAM Impressa em 3D (*Studio Display Mod*):** [Inserir Link Aqui] — *(Ficheiros STL: `iMac_RAM_Cover_Rear` e `iMac_RAM_Cover_Buttons_and_DP_USB_C`).*

### Ferramentas e Material de Fixação
* [ ] **Espaçadores Adesivos em Nylon (*PCB Standoffs*):** [Inserir Link Aqui] — *(Essencial para evitar curto-circuitos no alumínio).*
* [ ] **Kit de Chaves Torx (T5, T8, T10) + Ventosas (para vidro frontal):** [Inserir Link Aqui]
* [ ] **Bases Adesivas e Abraçadeiras (*Zip Ties*):** [Inserir Link Aqui]
* [ ] **Tiras Adesivas para Ecrã (Apenas necessário para iMacs de 2012 ou mais recentes):** [Inserir Link Aqui]

---

## 🛠️ Instruções Resumidas de Montagem

### Fase 1: Desmontagem e Identificação
1. **Abrir o iMac:** 
   * *Modelos 2011 (e anteriores):* Usa ventosas para puxar o vidro frontal magnético e desaparafusa os parafusos Torx que seguram o painel LCD.
   * *Modelos 2012+:* Usa uma roda de corte para separar a fita adesiva perimetral seguindo o guia do iFixit.
2. **Identificar o Painel:** Desliga cuidadosamente os cabos *ribbon* do LCD, pousa-o numa superfície macia e tira foto à etiqueta branca na traseira para confirmar o modelo exato antes de comprar a placa.
3. **Esvaziar o Chassis:** Remove a *logic board*, discos rígidos, ventoinhas e a fonte de alimentação interna. *(⚠️ **Segurança:** Nunca toques nos contactos expostos da fonte interna do iMac, pois os condensadores retêm carga perigosa mesmo desligados).* Mantém as colunas originais e o botão de energia no lugar se quiseres reutilizá-los.

### Fase 2: Teste de Bancada (Antes de Montar)
1. **Ligar a Placa:** Com o painel LCD fora do chassis, liga o cabo de vídeo (LVDS/eDP) e o cabo de retroiluminação (*backlight*) entre o painel e a placa controladora. Liga também o pequeno teclado de controlo (OSD).
2. **Testar Sinal:** Liga a fonte de 12V e conecta um computador via HDMI ou DisplayPort. Confirma que o ecrã acende, a resolução nativa é detetada e os botões de menu/brilho funcionam.

### Fase 3: Integração Interna e Cablagem 
1. **Isolamento Elétrico:** Fixa a placa controladora na traseira plana do painel LCD (ou no interior do chassis) utilizando **espaçadores de nylon**. Nunca permitas que a parte de trás da placa toque no metal do LCD ou no alumínio do chassis.
2. **Encaminhar Portas e Energia (Escolher opção):**
   * *Opção A (Simples e Fácil Manutenção):* Passa os cabos de extensão (HDMI, DP, 12V) diretamente pela abertura traseira da memória RAM. Deixa o transformador de 12V no exterior (facilita a troca se avariar) e prende o teclado OSD na traseira com bases adesivas isoladas.
   * *Opção B (Acabamento "De Fábrica"):* Retira a caixa plástica da fonte de 12V, fixa-a dentro do chassis e liga-a à tomada AC original do iMac. Solda os fios do botão *power* da placa OSD ao botão físico original do iMac, liga as colunas via placa *crossover* e instala a tampa traseira impressa em 3D com as portas *panel-mount* aparafusadas.

### Fase 4: Teste Pré-Fecho e Montagem Final
1. **Validar Tudo:** Encaixa provisoriamente o LCD no chassis com os cabos já passados e testa todas as entradas (HDMI, DisplayPort, Áudio e botões).
2. **Fechar o Monitor:**
   * *Modelos 2011:* Reaperta todos os parafusos Torx do painel LCD, limpa o pó interior e encaixa o vidro magnético.
   * *Modelos 2012+:* Limpa os resíduos de cola antigos, aplica as novas tiras adesivas no chassis e pressiona o ecrã firmemente no lugar.


---
---
---

# Projeto: Conversão de iMac 27" (2011) em Monitor Externo

## 1. Porquê fazer este projeto? (Viabilidade e Comparação de Preços)
Um iMac de 27 polegadas antigo perde rapidamente suporte de software e capacidade de processamento para tarefas modernas, mas mantém um chassis de alumínio maquinado, colunas estéreo de boa qualidade e um painel IPS excelente (2560×1440 QHD no modelo de 2011). Em vez de enviar o equipamento para reciclagem ou gastar centenas de euros num monitor novo com construção em plástico, converter o iMac permite obter um monitor de 27" com acabamento *premium* e suporte ergonómico integrado por uma fração do custo de mercado:

* **Conversão DIY (iMac 27" existente):** ~55€ – 110€ (apenas placa controladora, fonte, cabos e peças 3D)[cite: 1, 3].
* **Monitores 27" QHD (2K) equivalentes novos (ex: Dell UltraSharp / LG):** ~280€ – 450€.
* **Apple Studio Display (27" 5K):** ~1.779€ (preço base oficial).

### O que é uma Placa Controladora (*Driver / Controller Board*)?
A placa controladora é o "cérebro" que substitui toda a *logic board* original do computador. Ela recebe sinais de vídeo padrão modernos (HDMI, DisplayPort ou USB-C) vindos de um portátil ou PC e converte-os no protocolo nativo que o painel LCD interno do iMac entende (LVDS no modelo de 2011; eDP nos modelos 5K), gerindo também a alimentação da retroiluminação (*backlight*), o menu de brilho/cor (OSD) e a amplificação de áudio[cite: 1, 2, 3].

---

## 2. Lista de Compras (*Bill of Materials*)
> Preenche a coluna **Link** à medida que fores escolhendo os fornecedores.

| Componente | Especificação Técnica (iMac 27" 2011 - A1312) | Custo Est. | Link |
| :--- | :--- | :---: | :--- |
| **Placa Controladora (*Driver Board*)** | Compatível com painel `LM270WQ1` (confirmar código exato na etiqueta traseira do LCD) | ~35€ – 45€ | `[Inserir Link]` |
| **Fonte de Alimentação 12V** | Transformador DC 12V (5A a 7A), ficha 5.5mm × 2.5mm (centro positivo) — ou incluído no kit | ~12€ – 18€ | `[Inserir Link]` |
| **Placa *Crossover* de Áudio** | Módulo pequeno para ligar as 2 colunas internas originais do iMac à saída de som da controladora | ~8€ – 10€ | `[Inserir Link]` |
| **Suporte Traseiro Impresso em 3D** | *iMac Studio Display Mod* (`iMac_RAM_Cover_Rear.stl` + `iMac_RAM_Cover_Buttons_and_DP_USB_C.stl`) em ABS/ASA | ~15€ – 24€ | `[Inserir Link]` |
| **Cabos *Panel-Mount* Curtos** | 1x HDMI macho-fêmea (com rosca de painel) + 1x DisplayPort macho-fêmea (~30cm) | ~12€ – 18€ | `[Inserir Link]` |
| **Isolamento e Fixação** | Espaçadores adesivos de nylon para PCB (*standoffs*), fita Kapton (alta temp.) e ligadores com solda (*solder seal*) | ~5€ – 8€ | `[Inserir Link]` |
| **Contrapesos (Opcional)** | ~650g de pesos adesivos de calibragem de jantes (compensa o peso da *motherboard* removida na mola do pé) | ~5€ | `[Inserir Link]` |
| **Ferramentas Necessárias** | Ventosas (para o vidro magnético), chaves Torx (T8, T10), ferro de soldar e pistola de ar quente | Já tenho | — |

---

## 3. Guia Passo a Passo de Montagem e Soldadura

### ⚠️ Precauções de Segurança Antes de Começar
1. **Condensadores da Fonte Original (PSU):** Mesmo desligado da tomada, nunca toques nas pistas expostas da fonte de alimentação original do iMac ao desmontá-la; retêm cargas perigosas[cite: 2].
2. **Isolamento Elétrico:** Nunca deixes a parte traseira da placa controladora, do transformador ou da placa de botões tocar diretamente no alumínio do chassis ou na traseira metálica do LCD (risco imediato de curto-circuito)[cite: 3].

---

### Passo 1: Abertura e Identificação do Painel (Vantagem do Modelo 2011)
* **Ação:** Ao contrário dos modelos 2012+ (colados com fita adesiva), no teu **iMac 27" de 2011** basta usar ventosas para puxar o vidro frontal magnético e desaparafusar os parafusos Torx que seguram o painel LCD[cite: 1, 3]. Desliga cuidadosamente os cabos *ribbon* e pousa o LCD virado para baixo numa toalha macia[cite: 1, 3].
* **Verificação:** Lê a etiqueta branca na traseira do painel LCD e confirma a variante exata (ex: `LM270WQ1(SD)(E3)`) antes de encomendar a placa controladora[cite: 1, 3].

### Passo 2: Esvaziar o Chassis (*Gutting*)
* **Ação:** Seguindo o guia do iFixit para o iMac 27" Mid 2011, remove a *logic board*, a fonte de alimentação original, o disco rígido, o leitor ótico (*SuperDrive*), as ventoinhas e a cablagem interna desnecessária[cite: 2, 3].
* **O que manter:** Deixa intactos no chassis **as duas colunas estéreo originais**, **o botão físico de ligar/desligar** e **a tomada de alimentação AC traseira**.

### Passo 3: Teste de Bancada (Obrigatório Antes de Fechar)
* **Ação:** Com o painel LCD fora do chassis, liga o cabo de vídeo da placa controladora (atenção à orientação: ponto branco virado para cima, se aplicável) e o cabo de retroiluminação (*backlight*, fio vermelho do lado correto)[cite: 3]. Liga a fonte de 12V e um computador via HDMI ou DisplayPort[cite: 2, 3].
* **Verificação:** O LED da placa de controlo (OSD) acende e o monitor exibe imagem estável na resolução nativa (`2560×1440` a 60Hz)[cite: 2, 3].

### Passo 4: Integração Elétrica e Soldadura (Abordagem Jozef Cipa)
Para evitar transformadores externos e cabos soltos pela traseira, faz a integração interna em três frentes:

1. **Fonte de Alimentação 12V Interna (*Caseless*):**
   * Abre cuidadosamente a caixa plástica do transformador de 12V que alimenta a placa controladora (reduz o volume ocupado e melhora a dissipação térmica dentro do alumínio)[cite: 1].
   * Envolve a base da placa da fonte com fita Kapton (isolante térmico/elétrico) e fixa-a no interior do chassis.
   * Corta/descarnar os fios da entrada AC (230V) da tomada original do iMac e une-os diretamente aos terminais de entrada AC da fonte de 12V usando solda e manga retrátil (ou ligadores termorretráteis com anel de solda no interior)[cite: 1].
2. **Reutilização do Botão *Power* Original do iMac:**
   * Na pequena placa de botões (OSD) que acompanha a controladora, identifica o interruptor correspondente ao botão **Power** (geralmente o último botão da fila)[cite: 1].
   * Dessolda/remove esse botão físico da placa OSD (ou descarnar os dois fios que vão para esse pino no cabo *ribbon*)[cite: 1].
   * Faz a emenda (*splice*) e soldadura desses dois fios diretamente aos dois contactos do botão físico original de alumínio na traseira do iMac[cite: 1] (não tem polaridade, funciona como contacto momentâneo). Isola as soldaduras com manga retrátil.
3. **Áudio Interno (*Crossover*):**
   * Liga os fios das colunas esquerda e direita do iMac à pequena placa *crossover* (respeitando a polaridade dos canais) e conecta a saída desta à ficha de áudio da placa controladora[cite: 1].

### Passo 5: Montagem das Portas Traseiras em 3D (Tampa da RAM)
* **Ação:** Retira a tampa metálica original da memória RAM na traseira inferior do iMac e encaixa a peça impressa em 3D (`iMac_RAM_Cover_Rear.stl` + módulo de portas e botões)[cite: 1].
* **Montagem:** Aparafusa as extremidades fêmea dos cabos curtos *panel-mount* (HDMI e DisplayPort) nos respetivos encaixes da peça 3D e encaixa a placa OSD (agora sem o botão *power*) no alojamento dos botões[cite: 1].

### Passo 6: Fixação da Controladora, Contrapesos e Fecho Final
* **Fixação:** Cola 4 espaçadores adesivos de nylon (*standoffs*) nos furos da placa controladora e fixa-a na traseira plana do painel LCD (ou no fundo do chassis), garantindo zero contacto com metal[cite: 3]. Organiza os cabos internos com abraçadeiras[cite: 3].
* **Equilíbrio (Opcional):** Se sentires que a mola do pé ficou demasiado forte por falta do peso da *motherboard* e dissipador, cola os contrapesos na zona inferior interna abaixo da dobradiça.
* **Fecho:** Liga todas as fichas à controladora, encaixa o painel LCD no chassis, aperta novamente os parafusos Torx originais e coloca o vidro frontal magnético no sítio[cite: 1, 3].