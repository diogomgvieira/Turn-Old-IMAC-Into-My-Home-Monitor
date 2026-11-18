# Guia de Montagem: Conversão de iMac em Monitor (Abordagem "Studio Display Mod" — Jozef Cipa)

> **Resumo e Contexto:** Ao contrário dos dois guias anteriores (onde os cabos saem soltos pela traseira), este projeto foca-se num acabamento limpo e integrado: reutiliza o **cabo de alimentação original**, o **botão de ligar/desligar original**, as **colunas internas do iMac** e substitui a tampa da RAM por uma **peça impressa em 3D** com portas embutidas (*panel-mount*).

## 🛠️ Lista de Componentes (Estimativa ~128€ excluindo o iMac)

* **Placa Controladora (*Controller Board*) + Fonte 12V:** Compatível com o painel LCD específico (~76€ no AliExpress).

* **Placa *Crossover* para Colunas:** Permite ligar as colunas originais do iMac diretamente à saída de áudio da placa controladora (~10€ no AliExpress).

* **Suporte de Portas Impresso em 3D (*iMac Studio Display Mod*):** Substitui a tampa traseira da RAM para fixar as portas e botões sem cabos soltos (~24€). Ficheiros STL usados: `iMac_RAM_Cover_Rear.stl` e `iMac_RAM_Cover_Buttons_and_DP_USB_C.stl`.

* **Cabos Curtos de Montagem em Painel (*Panel-Mount*):** 1x HDMI (~6€) e 1x DisplayPort (~12€) para aparafusar na peça 3D.

* **Tiras Adesivas + Kit de Ferramentas:** Apenas necessário para modelos 2012+ (~2.5€). *(Nota: No teu **iMac 27" de 2011**, o vidro é magnético e o painel usa parafusos Torx, dispensando estas tiras).*

## 📋 Passo a Passo de Montagem

### 1. Abertura do iMac

* **Ação:** Corta cuidadosamente a fita adesiva do ecrã seguindo o guia do iFixit (nos modelos 2012+). No teu **iMac 2011**, basta remover o vidro frontal magnético com ventosas e desaparafusar os parafusos Torx do painel LCD.

* **Verificação:** Painel LCD desconectado e removido em segurança sem danos nos cabos *ribbon*.

### 2. Remoção dos Componentes Internos

* **Ação:** Retira a *logic board*, a fonte de alimentação original, ventoinhas e discos, deixando o chassis de alumínio oco (mantendo as colunas originais e o botão de energia no sítio).

* **Verificação:** Interior livre para alojar a nova eletrónica e passagem de cabos.

### 3. Cablagem Avançada (Fonte Interna, Botão Original e Portas 3D)

* **Fonte de Alimentação Interna:** Retira a caixa plástica do transformador de 12V que vem com a placa controladora (para melhorar a dissipação térmica e poupar espaço), fixa-o dentro do chassis e solda/liga-o diretamente à tomada AC original do iMac.

* **Botão de Energia Original:** Dessolda/remove o botão *power* da placa de controlo (OSD) da controladora e faz a ligação direta (*splice*) dos fios aos pinos do botão físico original do iMac.

* **Portas Traseiras em 3D:** Instala a tampa impressa em 3D no espaço da tampa da RAM, aparafusa os cabos *panel-mount* (HDMI e DisplayPort) e encaixa os restantes botões do menu OSD na peça 3D.

* **Verificação:** Nenhuma fonte externa nem cabos soltos saem da traseira; o iMac mantém o aspeto original por fora.

### 4. Instalação da Placa Controladora e Áudio

* **Ação:** Fixa a placa controladora no interior do chassis, liga o cabo de vídeo ao painel LCD, liga os cabos HDMI/DisplayPort vindos da tampa 3D e conecta as colunas originais do iMac através da placa *crossover*.

* **Verificação:** Todas as ligações internas (vídeo, alimentação, botão *power*, OSD e som) estão devidamente isoladas e firmes.

### 5. Teste Final e Fecho do Chassis

* **Ação:** Liga o cabo de energia original do iMac à tomada e testa a imagem, os botões e o som antes de fechar. Depois de validado, limpa as bordas do chassis, aplica as novas tiras adesivas (ou reaperta os parafusos Torx e coloca o vidro magnético no modelo 2011) para selar o monitor.

* **Verificação:** O ecrã liga através do botão traseiro original, reproduz som pelas colunas internas e apresenta imagem estável.

## 💡 Notas Técnicas do Autor (Pós-Montagem)

* **Resolução via MacBook:** Embora o painel do autor seja 5K, o MacBook dele limitou a saída externa a 4K (`3840x2160`), mantendo ainda assim excelente nitidez. *(No teu iMac 2011, o painel é 2K nativo `2560x1440`, pelo que funcionará na resolução máxima nativa sem limitações).*

* **Efeito "Pinkish Edge":** Painéis antigos da Apple podem apresentar uma ligeira tonalidade rosada nas extremidades em fundos muito brancos devido ao desgaste natural do painel LCD.