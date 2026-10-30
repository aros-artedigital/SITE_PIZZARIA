# Italiana Pizzaria — Base do Design System

**Aplicação:** site de página única, prioridade para telas de celular.
**Objetivo de uso:** levar o visitante ao pedido no menor número de toques possível. Toda decisão visual abaixo serve a isso.

**Direção extraída das referências:** o rústico italiano (madeira, serifa caligráfica, creme) constrói a confiança na comida. O comercial direto (sans pesada, laranja saturado, botão em bloco) constrói a ação. A regra que separa os dois: o rústico ocupa fundos e títulos, o laranja saturado é reservado só para o que se clica.

---

## 1. Cores

### Paleta principal (tricolore italiana)

| Nome | Hex | Uso |
|---|---|---|
| Brasa (vermelho Itália) | `#CC2229` | Botão principal, preços, chapéus de seção, ícones ativos |
| Brasa escura | `#9E1A1F` | Estado de passar o mouse e de clique, links sobre fundo claro |
| Brasa clara | `#F08787` | Texto de destaque sobre fundos escuros |
| Marrom forno (verde Itália) | `#0E3D25` | Fundo das seções imersivas, abertura, rodapé |
| Carvão | `#12180F` | Títulos e texto forte sobre fundo claro |

### Paleta secundária

| Nome | Hex | Uso |
|---|---|---|
| Creme | `#F6F7F2` | Fundo geral das seções claras |
| Massa | `#FBE0E0` | Fundo de blocos suaves, etiquetas, área de imagem vazia |
| Branco | `#FFFFFF` | Fundo de card e de campo de formulário |
| Cinza texto | `#62685E` | Texto de apoio e descrições |
| Borda | `#DCE3D8` | Contorno de card, divisórias, contorno de campo |

### Paleta de suporte (estados e sistema)

| Nome | Hex | Uso |
|---|---|---|
| Verde pedido | `#0F7A3D` | Botão de WhatsApp e botão flutuante |
| Sucesso | `#2E7D4F` | Confirmação de envio de formulário |
| Atenção | `#B57C00` | Aviso de horário fechado, área fora da entrega |
| Erro | `#B3261E` | Mensagem de campo inválido |

### Regras de aplicação

1. **O vermelho é ação, não decoração.** Não use Brasa como fundo de seção inteira nem como cor de bloco grande. Ele perde força e o botão deixa de saltar.
2. **Uma ação principal por seção.** Se houver dois botões, o segundo é de contorno.
3. **Contraste verificado.** Brasa sobre branco é aprovada para texto pequeno. Sobre Marrom forno (verde), use Brasa clara, nunca a Brasa.
4. **Fundo escuro é para atmosfera.** Abertura, faixa de horários e rodapé em Marrom forno (verde Itália). Cardápio e formulários sempre em Creme ou Branco, porque leitura longa em fundo escuro cansa.
5. **Verde do WhatsApp é o mesmo verde da marca**, então o botão de pedido direto se funde naturalmente com a paleta — não precisa de outro tom.

---

## 2. Tipografia

Duas famílias, ambas disponíveis no Google Fonts e com acentuação completa em português.

### Fontes

**Playfair Display** — display serifado. Cobre o papel da serifa caligráfica da primeira referência. Uso restrito: nome da marca, H1 e H2. Nunca em texto corrido.
*Alternativas próximas:* Prata, Yeseva One, Abril Fatface.

**Archivo** — família sans com peso Black. Cobre o papel da sans pesada da segunda referência e também o texto corrido, com uma família só. Uso: H3 em diante, corpo, botões, formulários e preços.
*Alternativas próximas:* Poppins, Barlow, Figtree.

### Hierarquia

| Nível | Fonte e peso | Desktop | Celular | Entrelinha | Observação |
|---|---|---|---|---|---|
| H1 | Playfair Display 700 | 56px | 34px | 1,1 | Só uma vez por página |
| H2 | Playfair Display 700 | 40px | 28px | 1,2 | Título de seção |
| H3 | Archivo 700 | 24px | 20px | 1,35 | Título de card e de bloco |
| H4 | Archivo 600 | 20px | 18px | 1,4 | Nome do sabor |
| Corpo grande | Archivo 400 | 18px | 17px | 1,6 | Texto de abertura de seção |
| Corpo | Archivo 400 | 16px | 16px | 1,65 | Padrão. Nunca abaixo de 16px |
| Apoio | Archivo 400 | 14px | 14px | 1,5 | Descrição de sabor, legenda |
| Chapéu | Archivo 600 | 13px | 12px | 1,4 | Caixa alta, espaçamento 0,16em, cor Brasa |
| Rótulo de campo | Archivo 600 | 14px | 14px | 1,4 | Sempre acima do campo |
| Preço | Archivo 700 | 20px | 18px | 1,2 | Algarismos de largura fixa |
| Botão | Archivo 600 | 16px | 16px | 1 | Frase iniciando por verbo |

### Regras

- Largura máxima de leitura: 65 caracteres. Acima disso o olho perde a linha.
- Playfair Display não vai para caixa alta. A serifa fina quebra visualmente.
- Caixa alta apenas em chapéus e etiquetas, sempre com espaçamento entre letras.
- Preço com algarismos tabulares para alinhar coluna de valores no cardápio.

---

## 3. Componentes

### Botões

| Variação | Fundo | Texto | Borda | Uso |
|---|---|---|---|---|
| Principal | `#CC2229` | Branco | nenhuma | Fazer pedido |
| WhatsApp | `#0F7A3D` | Branco | nenhuma | Pedido direto por mensagem |
| Contorno claro | transparente | `#9E1A1F` | 2px `#CC2229` | Ação secundária em fundo claro |
| Contorno escuro | transparente | Branco | 2px branco | Ação secundária em fundo escuro |
| Texto | transparente | `#9E1A1F` | linha inferior 1,5px | Ver cardápio completo, ver rota |

**Medidas:** altura mínima 52px, espaçamento interno 16px em cima e embaixo, 32px nas laterais, arredondamento 6px.
**Passar o mouse:** fundo escurece para `#9E1A1F`, sem mudança de tamanho.
**Clique:** escala 0,98 em 120 milissegundos.
**Foco pelo teclado:** contorno de 3px em `rgba(204,34,41,0.35)`, afastado 2px. Nunca remover.
**Escrita:** verbo primeiro, sem ponto final, letra maiúscula só na primeira palavra. "Fazer meu pedido", não "Pedidos".

**Botão flutuante:** círculo de 60px, fundo Verde pedido, ícone branco, canto inferior direito, afastado 20px das bordas. Em telas de até 768px, substituir por barra fixa de largura total no rodapé, altura 64px.

### Campos de formulário

- Altura 52px, arredondamento 6px, fundo branco, borda 1,5px `#E6DAD0`.
- Espaçamento interno lateral 16px.
- Rótulo acima do campo, Archivo 600, 14px, cor Carvão. Nunca usar apenas texto dentro do campo como rótulo.
- Texto de exemplo dentro do campo: cinza `#9C8F86`, com um exemplo real ("71 99999-0000"), não a repetição do rótulo.
- **Foco:** borda `#CC2229` mais halo `0 0 0 3px rgba(204,34,41,0.15)`.
- **Erro:** borda `#B3261E`, mensagem abaixo em 13px na mesma cor, dizendo o que corrigir. "Informe um telefone com DDD", não "Campo inválido".
- Campo de área de texto: altura mínima 120px, sem redimensionamento livre.

### Cards

**Card de sabor** — fundo branco, borda 1px `#E6DAD0`, arredondamento 12px, imagem no topo em proporção 4:3, espaçamento interno 20px. Ordem do conteúdo: etiqueta de categoria, nome do sabor, descrição, preço. O preço fecha o card porque é a última informação da decisão.
Ao passar o mouse: sobe 2px e ganha a sombra nível 2.

**Card de depoimento** — fundo Creme, sem borda, arredondamento 12px, espaçamento interno 24px. Texto em Archivo 400 16px, assinatura em 14px cinza.

**Card sobre fundo escuro** — fundo `rgba(255,255,255,0.06)`, borda 1px `rgba(255,255,255,0.14)`, texto branco, chapéu em Brasa clara.

**Etiqueta** — altura 26px, arredondamento total, fundo Massa, texto `#9E1A1F` em 12px caixa alta.

### Navegação

- Barra fixa no topo, altura 76px, fundo branco com sombra nível 1 após a rolagem.
- Itens em Archivo 500, 16px, cor Carvão. Item ativo com linha de 2px em Brasa embaixo.
- Botão principal sempre visível na barra, mesmo no celular.
- Menu de celular: sanduíche à direita, painel em tela cheia com fundo Marrom forno e itens em 24px.

---

## 4. Estética

### Arredondamento

| Valor | Onde |
|---|---|
| 0 | Faixas de largura total, imagens de fundo, seções |
| 6px | Botões, campos, seletores |
| 12px | Cards, blocos de conteúdo, imagens dentro de card |
| 20px | Blocos grandes, janelas de confirmação |
| Total | Etiquetas, botão flutuante, indicadores |

Regra: nunca misturar mais de dois valores dentro de um mesmo bloco.

### Sombras

Todas com base marrom, nunca cinza neutro. Sombra cinza sobre fundo creme deixa a interface suja.

| Nível | Valor | Onde |
|---|---|---|
| 1 | `0 1px 2px rgba(14,61,37,0.06)` | Barra do topo após rolagem |
| 2 | `0 4px 12px rgba(14,61,37,0.08)` | Card ao passar o mouse |
| 3 | `0 12px 32px rgba(14,61,37,0.12)` | Botão flutuante, janelas |
| Foco | `0 0 0 3px rgba(204,34,41,0.15)` | Campo em foco |

Botões não recebem sombra em repouso. Se o botão precisa de sombra para ser visto, o problema é a cor de fundo da seção.

### Espaçamento

Escala de base 8: **4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96 · 128**. Nenhum valor fora dessa lista.

| Medida | Desktop | Celular |
|---|---|---|
| Espaço vertical entre seções | 96px | 56px |
| Largura do contêiner | 1200px | 100% |
| Margem lateral | 24px | 16px |
| Espaço entre cards | 24px | 16px |
| Espaço entre título e texto de apoio | 16px | 12px |
| Espaço entre texto e botão | 32px | 24px |

Grade de 12 colunas no desktop. Cardápio em 3 colunas no desktop, 2 no tablet, 1 no celular.

---

## 5. Regras de usabilidade voltadas ao pedido

1. **Alvo de toque mínimo de 48 por 48 pixels**, com 8px de folga entre alvos. A maioria dos pedidos sai do celular, muitas vezes com uma mão só.
2. **A ação de pedir nunca sai da tela.** Barra fixa no rodapé do celular, botão na barra do topo no desktop.
3. **Preço sempre junto do sabor.** Cardápio sem preço aumenta o abandono e joga a dúvida para o WhatsApp.
4. **Foto real do produto.** Imagem de banco de imagens em pizzaria destrói a confiança mais rápido do que qualquer erro de layout.
5. **Horário e área de entrega acima da dobra.** São as duas primeiras perguntas de quem chega com fome.
6. **Formulário de reserva com no máximo 5 campos:** nome, telefone, data, horário, número de pessoas.
7. **Estados vazios convidam.** Fora do horário: "Estamos fechados agora. Abrimos terça às 18h. Deixe seu pedido agendado."
8. **Respeitar redução de movimento.** Toda animação dentro de `prefers-reduced-motion` deve ser desligada.
9. **Foco visível em tudo.** Nunca remover o contorno do teclado sem substituir por outro indicador.

---

## 6. Variáveis para desenvolvimento

```css
:root {
  --cor-brasa: #CC2229;
  --cor-brasa-escura: #9E1A1F;
  --cor-brasa-clara: #F08787;
  --cor-marrom: #0E3D25;
  --cor-carvao: #12180F;
  --cor-creme: #F6F7F2;
  --cor-massa: #FBE0E0;
  --cor-branco: #FFFFFF;
  --cor-texto-apoio: #62685E;
  --cor-borda: #DCE3D8;
  --cor-whatsapp: #0F7A3D;
  --cor-sucesso: #2E7D4F;
  --cor-atencao: #B57C00;
  --cor-erro: #B3261E;

  --fonte-display: "Playfair Display", Georgia, serif;
  --fonte-texto: "Archivo", "Helvetica Neue", Arial, sans-serif;

  --raio-controle: 6px;
  --raio-card: 12px;
  --raio-bloco: 20px;

  --sombra-1: 0 1px 2px rgba(14,61,37,0.06);
  --sombra-2: 0 4px 12px rgba(14,61,37,0.08);
  --sombra-3: 0 12px 32px rgba(14,61,37,0.12);
  --sombra-foco: 0 0 0 3px rgba(204,34,41,0.15);

  --esp-1: 4px;  --esp-2: 8px;  --esp-3: 12px;
  --esp-4: 16px; --esp-5: 24px; --esp-6: 32px;
  --esp-7: 48px; --esp-8: 64px; --esp-9: 96px; --esp-10: 128px;

  --container: 1200px;
  --altura-controle: 52px;
}
```
