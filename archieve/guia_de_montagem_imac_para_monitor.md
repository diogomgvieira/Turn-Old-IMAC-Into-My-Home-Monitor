# Guia de Montagem: Conversão de iMac em Monitor Externo

> **Nota de Adaptação (iMac 27" 2011 vs. 5K):** O guia original (*Oh My Pizza*) baseia-se num modelo 5K selado com fita adesiva. No teu **iMac 27" de 2011**, o vidro frontal é magnético e o painel LCD é fixo com parafusos Torx, o que simplifica a abertura e dispensa a compra de tiras adesivas. Além disso, o painel do modelo 2011 tem resolução 2560x1440 (2K), exigindo uma placa controladora específica para esse painel.

---

## ⚠️ Aviso de Segurança Elétrica
Nunca deixes a parte traseira exposta da placa controladora (*driver board*) ou do teclado de controlo (*OSD keypad*) tocar no chassis de alumínio ou na traseira metálica do painel LCD. Isso causará um curto-circuito imediato. Usa sempre espaçadores de nylon ou isolamento não condutor.

---

## 📋 Passo a Passo de Montagem

### 1. Identificar os Modelos do iMac e do Painel LCD
* **Ação:** Verifica o modelo exato do iMac nas informações do sistema. Remove o vidro frontal (ventosas no modelo 2011), desaparafusa o painel LCD e pousa-o virado para baixo numa superfície macia.
* **Verificação:** Anota o código exato da etiqueta branca na traseira do painel LCD (ex: `LM270WQ1` para modelos 2011 27" ou `LM270QQ1` para 5K).

### 2. Adquirir Componentes e Ferramentas
* **Placa Controladora (*Driver Board*):** Pesquisar no eBay/AliExpress pelo código exato do painel LCD + `driver board` (confirmar a sub-variante exata).
* **Alimentação:** Transformador DC 12V (5A a 7A, ficha 5.5mm x 2.5mm, centro positivo).
* **Cabos de Extensão (30 a 45 cm, Macho-Fêmea):** HDMI, DisplayPort, Áudio 3.5mm e extensão DC para encaminhar as portas para o exterior através da tampa traseira da memória RAM.
* **Fixação e Ferramentas:** Chaves Torx (T8, T10), espaçadores adesivos em nylon para PCB (*standoffs*), abraçadeiras (*zip ties*) e bases adesivas.

### 3. Teste de Bancada (Antes da Montagem)
* **Ação:** Com o painel fora do chassis, liga o cabo de dados LCD (ponto branco virado para cima) e o cabo de retroiluminação (*backlight*, fio vermelho à direita) à placa controladora. Liga a fonte de 12V e um computador via HDMI ou DisplayPort.
* **Verificação:** O LED do teclado OSD acende, a retroiluminação liga e o computador externo deteta o ecrã com imagem estável.

### 4. Esvaziar o Chassis do iMac
* **Ação:** Seguindo o guia de desmontagem do iFixit para o teu modelo, remove a *logic board*, fonte de alimentação interna, discos rígidos, leitor ótico, ventoinhas e cablagem interna.
* **Verificação:** O interior da carcaça de alumínio fica totalmente oco e limpo, com acesso livre à abertura da tampa da RAM.

### 5. Ensaio de Encaixe (*Dry-Fit*) e Passagem de Cabos
* **Ação:** Fixa temporariamente a placa controladora na traseira do painel LCD (com fita adesiva dobrada) e liga todos os cabos de extensão e o cabo do teclado OSD. Aproxima o LCD do chassis e passa as pontas fêmea das extensões pela abertura traseira da RAM.
* **Verificação:** Todos os cabos chegam ao exterior sem forçar ou dobrar excessivamente as portas da placa.

### 6. Fixação Definitiva da Placa e Gestão de Cabos
* **Ação:** Retira a fita temporária e encaixa 4 espaçadores adesivos de nylon nos furos da placa controladora, colando-a permanentemente na traseira plana do painel LCD. Organiza e prende os cabos com bases adesivas e abraçadeiras, identificando cada porta.
* **Verificação:** A placa está firmemente elevada sobre o painel LCD, sem qualquer contacto metálico.

### 7. Teste de Entradas Pré-Fecho
* **Ação:** Encaixa provisoriamente o painel LCD no chassis (com alguns parafusos no modelo 2011) com os cabos já passados para fora. Testa todas as portas de extensão (HDMI, DisplayPort, Áudio) com sinal ativo.
* **Verificação:** Todas as entradas funcionam sem falhas antes de fechar definitivamente o equipamento.

### 8. Fecho do Chassis e Montagem do Teclado OSD
* **Ação:** Volta a apertar todos os parafusos Torx do painel LCD e coloca o vidro frontal magnético (ou aplica novas tiras adesivas em modelos 2012+). Cola duas bases de abraçadeiras na traseira exterior do iMac e prende o teclado de controlo (botões de energia/menu) às mesmas, garantindo que a placa do teclado não toca no alumínio.
* **Verificação:** O ecrã fica alinhado e os botões traseiros respondem sem risco de curto-circuito.