# Guia de Montagem: Conversão de iMac em Monitor (Abordagem Lewis Lovelock)

> **Resumo e Contexto:** Este guia foca-se numa conversão permanente (irreversível como Mac) de um iMac 27" 5K (2015), mas a arquitetura e as decisões de design aplicam-se diretamente ao teu **iMac 27" de 2011**, ajustando apenas a placa controladora ao painel 2K (`LM270WQ1`) desse ano e aproveitando os parafusos Torx em vez de fitas adesivas.

## ⚠️ Aviso de Segurança (Fonte Interna)

Ao desmontar o iMac, **nunca toques nas pistas expostas da fonte de alimentação interna (PSU)**. Mesmo com o cabo desligado da tomada, os condensadores retêm cargas elétricas perigosas.

## 🛠️ Componentes Principais

* **Placa Conversora (*Display Converter Board*):** Compatível com o conector interno do painel LCD (no caso do 5K, com entradas DisplayPort 1.4 e HDMI 2.0; para o 2011, placa compatível com eDP/LVDS do painel 2560x1440).

* **Fonte de Alimentação Externa:** Transformador `12V 6A` (mantido fora do chassis por opção de manutenção).

* **Placa de Controlo (OSD):** Pequena placa verde ligada por cabo *ribbon* à placa principal para controlar brilho, entradas e menu.

## 📋 Passo a Passo de Montagem

### 1. Desmontagem Completa do iMac

* **Ação:** Seguindo o guia específico do iFixit para o teu modelo, remove o ecrã e retira todos os componentes internos: *logic board*, armazenamento, ventoinhas, cablagem e a fonte de alimentação interna (com extremo cuidado).

* **Verificação:** Resta apenas a carcaça vazia de alumínio com os suportes de parafusos, a área VESA e o mecanismo do pé.

### 2. Ligação da Placa Conversora ao Painel

* **Ação:** Posiciona a placa conversora na traseira do painel LCD e liga-a utilizando o cabo de vídeo do painel e o cabo *ribbon* para a pequena placa verde de botões (OSD).

* **Verificação:** Ligações firmes sem tensão nos cabos *ribbon*.

### 3. Teste de Bancada (Antes de Fechar)

* **Ação:** Com o ecrã ainda fora do chassis, liga o cabo DisplayPort (ou HDMI) a um computador e alimenta a placa com o transformador de 12V 6A.

* **Verificação:** O painel acende, o sistema operativo reconhece o monitor na resolução nativa a 60Hz e os botões OSD respondem.

### 4. Passagem de Cabos e Decisão sobre a Fonte

* **Ação:** Encaminha o cabo de alimentação (12V) e o cabo de vídeo (DisplayPort/HDMI) diretamente para o exterior através da abertura traseira da tampa da memória RAM.

* **Decisão de Design (Fonte Externa vs. Interna):** O autor considerou esconder o transformador de 12V dentro do chassis e ligá-lo à tomada original do iMac para ter apenas um cabo visível, mas **optou por deixá-lo no exterior**. Se o transformador avariar no futuro, substitui-se em segundos sem ter de voltar a abrir o ecrã.

### 5. Fecho do Chassis

* **Ação:** Encaixa o painel LCD de volta na carcaça de alumínio (no guia 5K usa fitas adesivas próprias ou fita provisória; no teu **iMac 2011**, basta reapertar os parafusos Torx do painel e encaixar o vidro magnético).

* **Verificação:** Ecrã fixo e cabos a sair de forma limpa pela traseira sem ficarem entalados.