# 📚 Exemplos de Prompts Excelentes para os Agentes

Este documento contém exemplos de prompts eficazes para usar com o **Product Manager** e o **Frontend Engineer Senior**.

---

## 🎯 Product Manager - Exemplos de Prompts

### 1. Definição de Nova Feature

#### ✅ Prompt Excelente
```
Preciso de uma especificação completa para uma feature de filtros avançados 
na listagem de produtos. Os usuários reclamam que não conseguem encontrar 
produtos específicos facilmente. Queremos filtros por: categoria, preço, 
disponibilidade e avaliação. Prioridade alta pois impacta conversão.
```

**Por que é excelente:**
- Contexto claro do problema
- Lista requisitos específicos
- Menciona motivação (reclamações de usuários)
- Define impacto no negócio
- Indica prioridade

#### ❌ Prompt Ruim
```
Crie filtros para produtos
```

---

### 2. User Story para Nova Funcionalidade

#### ✅ Prompt Excelente
```
Escreva uma user story completa para implementação de autenticação social 
(Google e GitHub). Nosso target são desenvolvedores que preferem login 
rápido. Precisamos considerar:
- Fluxo de primeiro acesso vs retorno
- Vinculação com contas existentes
- Dados que vamos coletar (email, nome, avatar)
- Estados de erro se o OAuth falhar

Inclua acceptance criteria, fluxos detalhados e considerações de segurança.
```

**Por que é excelente:**
- Define escopo claro
- Menciona persona (desenvolvedores)
- Lista considerações técnicas importantes
- Pede componentes específicos da especificação
- Antecipa edge cases

#### ❌ Prompt Ruim
```
Faça user story de login
```

---

### 3. Priorização de Features

#### ✅ Prompt Excelente
```
Tenho 4 features no backlog e preciso priorizar para o próximo sprint:

1. Sistema de notificações em tempo real
2. Export de relatórios em PDF
3. Dashboard de analytics para admins
4. Modo escuro (dark mode)

Contexto:
- Temos 5000 usuários ativos
- 70% usam mobile
- NPS atual é 45
- Recebemos 50+ pedidos de dark mode
- Admins reclamam de falta de visibilidade de métricas

Use framework RICE para priorizar e justifique cada decisão.
```

**Por que é excelente:**
- Lista todas as opções claramente
- Fornece dados quantitativos
- Dá contexto de negócio e usuários
- Solicita framework específico
- Pede justificativas

#### ❌ Prompt Ruim
```
Qual feature fazer primeiro?
```

---

### 4. Análise de Fluxo de Usuário

#### ✅ Prompt Excelente
```
Preciso mapear o fluxo completo de checkout do nosso e-commerce, incluindo:
- Revisão do carrinho
- Endereço de entrega
- Método de pagamento
- Confirmação

Atualmente temos 40% de abandono no checkout. Quero identificar:
- Pontos de fricção em cada etapa
- Estados de erro e como lidar
- Oportunidades de reduzir passos
- Como lidar com usuários não-logados

Inclua tanto fluxo feliz quanto alternativas e erros.
```

**Por que é excelente:**
- Define escopo completo do fluxo
- Apresenta problema (40% abandono)
- Lista objetivos específicos da análise
- Pede consideração de edge cases
- Menciona diferentes tipos de usuário

#### ❌ Prompt Ruim
```
Como deve ser o checkout?
```

---

### 5. Definition of Done

#### ✅ Prompt Excelente
```
Crie uma Definition of Done específica para a feature de chat em tempo real 
que estamos implementando. Considere:

Aspectos técnicos:
- Performance (latência < 200ms)
- Suporte offline e reconexão
- Scroll infinito para histórico

Aspectos de qualidade:
- Acessibilidade (screen readers)
- Responsivo (mobile-first)
- Testes automatizados

Aspectos de negócio:
- Métricas de sucesso definidas
- Documentação para suporte
- Rollout gradual (10% -> 50% -> 100%)
```

**Por que é excelente:**
- Específico para a feature
- Categoriza diferentes aspectos
- Define requisitos mensuráveis
- Considera qualidade e negócio
- Menciona estratégia de deploy

#### ❌ Prompt Ruim
```
O que precisa estar pronto?
```

---

## 💻 Frontend Engineer - Exemplos de Prompts

### 1. Implementação de Componente

#### ✅ Prompt Excelente
```
Implemente um componente Card reutilizável baseado nesta especificação:

Requisitos:
- Variantes: default, outlined, elevated
- Slots: header, body, footer (todos opcionais)
- Props: onClick, isLoading, isDisabled
- Responsivo: stack no mobile, horizontal no desktop
- Acessível: role="article", foco via teclado

Design:
- Padding interno: 16px mobile, 24px desktop
- Border radius: 12px
- Shadow em elevated: shadow-lg
- Hover: scale(1.02) com transition suave

IMPORTANTE:
- Verifique primeiro se já existe Card em src/components/ui/
- Use Flexbox com gap para layout interno
- TypeScript strict com todas as props tipadas
- Zero comentários a menos que necessário
```

**Por que é excelente:**
- Especificação completa do componente
- Lista props e variantes
- Define comportamento responsivo
- Inclui requisitos de acessibilidade
- Lembra de verificar componentes existentes
- Reforça regras do projeto (Flexbox, gap)
- Define expectativas de qualidade

#### ❌ Prompt Ruim
```
Crie um card
```

---

### 2. Implementação de Página

#### ✅ Prompt Excelente
```
Crie a página de perfil do usuário (/profile) como Server Component:

Layout:
- Header fixo com avatar, nome, botão editar
- Tabs: "Sobre", "Atividades", "Configurações"
- Conteúdo responsivo: mobile stack, desktop 2 colunas

Dados:
- Fetch user data via getUserProfile(userId)
- Mostrar loading skeleton durante fetch
- Error boundary se falhar

Componentes a reutilizar:
- Avatar de src/components/ui/avatar
- Button de src/components/ui/button  
- Tabs de src/components/ui/tabs

Estilização:
- Flexbox com gap-6 entre seções
- Max width de 1200px centralizado
- Padding responsivo: p-4 mobile, p-8 desktop

NÃO comite automaticamente, mostre o código para revisão.
```

**Por que é excelente:**
- Define estrutura completa da página
- Especifica tipo de component (Server)
- Lista componentes a reutilizar
- Define estratégia de loading/error
- Detalha layout e espaçamento
- Reforça regras (Flexbox, gap, não commitar)
- Dá contexto de responsividade

#### ❌ Prompt Ruim
```
Faça uma página de perfil
```

---

### 3. Refatoração de Código

#### ✅ Prompt Excelente
```
Refatore o componente ProductList em src/components/features/product-list.tsx:

Problemas atuais:
- Usando Grid (deveria ser Flexbox)
- Usando space-y-4 (deveria ser gap)
- Lógica de filtro no componente (mover para hook)
- Sem loading state
- Comentários desnecessários

Objetivos:
- Converter para Flexbox com gap-4
- Extrair lógica para useProductFilter hook
- Adicionar skeleton loading
- Remover comentários óbvios
- Manter apenas comentários críticos

Mantenha:
- TypeScript types existentes
- Mesma interface pública (props)
- Testes existentes funcionando

Mostre diff antes de aplicar mudanças.
```

**Por que é excelente:**
- Especifica arquivo exato
- Lista problemas específicos
- Define objetivos claros de refatoração
- Indica o que manter
- Pede review antes de aplicar
- Alinhado com regras do projeto

#### ❌ Prompt Ruim
```
Melhore o ProductList
```

---

### 4. Debugging

#### ✅ Prompt Excelente
```
Bug no formulário de checkout (src/app/checkout/page.tsx):

Comportamento atual:
- Ao preencher CEP, campo de endereço não atualiza
- Console mostra: "Cannot read property 'street' of undefined"
- Acontece só quando usuário cola o CEP (não quando digita)

Contexto:
- Usamos API ViaCEP para buscar endereço
- Component é Client Component
- Estado gerenciado com useState

Investigar:
- Race condition no onChange vs onPaste?
- Validação de CEP antes da API call?
- Handling de erro da API

Após identificar, explique o problema e proponha solução.
NÃO aplique fix sem minha aprovação.
```

**Por que é excelente:**
- Descreve comportamento específico
- Fornece mensagem de erro
- Detalha quando acontece
- Dá contexto técnico
- Sugere possíveis causas
- Define processo (explicar depois aplicar)
- Pede aprovação

#### ❌ Prompt Ruim
```
O checkout não funciona
```

---

### 5. Implementação de Feature Completa

#### ✅ Prompt Excelente
```
Implemente sistema de busca com autocomplete no header:

Especificação:
- Input de busca com ícone de lupa
- Dropdown com sugestões ao digitar (debounce 300ms)
- Máximo 5 sugestões
- Highlight do termo buscado nas sugestões
- Navegação via teclado (↑↓ Enter Esc)
- Click fora fecha dropdown
- Mobile: full screen overlay

Arquitetura:
- SearchBar: Client Component principal
- useSearch: hook para lógica e debounce
- SearchSuggestions: componente de dropdown
- API: /api/search?q=term

Componentes a usar:
- Input de src/components/ui/input
- ícones de lucide-react

Layout:
- Flexbox para input + icon
- gap-2 entre elementos
- Dropdown com absolute positioning

Performance:
- Lazy load SearchSuggestions
- Cancel requests anteriores
- Cache results em memória

Entregáveis:
1. Estrutura de arquivos proposta
2. Código dos componentes
3. Hook customizado
4. Diff para revisão (NÃO comitar)

Pergunte se algo não estiver claro antes de começar.
```

**Por que é excelente:**
- Especificação completa e detalhada
- Define arquitetura de componentes
- Lista requisitos de UX (keyboard nav)
- Menciona performance e otimizações
- Especifica componentes a reutilizar
- Segue regras de layout (Flexbox, gap)
- Define entregáveis claramente
- Convida perguntas

#### ❌ Prompt Ruim
```
Adiciona busca no site
```

---

## 🔄 Prompts para Colaboração entre Agentes

### 1. PM → Engineer: Esclarecimento Técnico

#### ✅ Prompt Excelente (PM para Engineer)
```
@Frontend-Engineer

Estou especificando feature de upload de múltiplos arquivos.
Preciso entender viabilidade técnica:

Requisitos de produto:
- Usuário pode arrastar múltiplos arquivos (drag & drop)
- Preview de imagens antes do upload
- Progress bar individual por arquivo
- Limite: 10 arquivos, 5MB cada
- Formatos: JPG, PNG, PDF

Perguntas técnicas:
1. Há limitações no Next.js 16 para file upload?
2. Devemos processar no client ou via API route?
3. Qual a melhor lib para drag & drop (ou nativo)?
4. Como lidar com preview de PDFs?
5. Estimativa de esforço (1-3 dias, 3-5, 5+)?

Preciso dessas respostas para priorizar no roadmap.
```

#### ❌ Prompt Ruim
```
Dá pra fazer upload de arquivos?
```

---

### 2. Engineer → PM: Proposta de Melhoria

#### ✅ Prompt Excelente (Engineer para PM)
```
@Product-Manager

Ao implementar o dashboard de analytics, identifiquei oportunidade:

Situação:
- Especificação pede gráficos usando Chart.js
- Renderização acontece no client (Client Component)
- Bundle size aumenta ~50KB
- Performance no mobile cai (FCP +800ms)

Proposta técnica:
- Usar Server Components para processar dados
- Gerar SVGs estáticos no servidor
- Cliente só hidrata interações (tooltips)
- Reduz bundle em 45KB
- FCP melhora ~700ms

Trade-offs:
- PRO: Performance significativa
- PRO: SEO melhor (gráficos no HTML)
- CON: Interatividade levemente reduzida
- CON: +2 dias de desenvolvimento

Preciso de decisão: seguir spec original ou implementar otimização?
Posso criar protótipo se ajudar na decisão.
```

#### ❌ Prompt Ruim
```
Chart.js é pesado, posso mudar?
```

---

## 💡 Dicas Gerais para Prompts Eficazes

### Para o Product Manager

**Sempre inclua:**
1. ✅ Contexto do problema/oportunidade
2. ✅ Objetivos mensuráveis
3. ✅ Usuários impactados (personas)
4. ✅ Dados quantitativos quando disponíveis
5. ✅ Prioridade e urgência
6. ✅ Constraints conhecidas

**Evite:**
1. ❌ Pedir especificações sem contexto
2. ❌ Perguntas muito abertas sem direção
3. ❌ Omitir stakeholders ou impacto
4. ❌ Não definir critérios de sucesso

### Para o Frontend Engineer

**Sempre inclua:**
1. ✅ Arquivo/caminho específico quando aplicável
2. ✅ Requisitos funcionais E não-funcionais
3. ✅ Componentes existentes a reutilizar
4. ✅ Expectativas de layout (Flexbox, gap)
5. ✅ Lembrete para NÃO commitar automaticamente
6. ✅ Requisitos de acessibilidade

**Evite:**
1. ❌ Pedidos vagos sem especificação
2. ❌ Omitir se deve usar componentes existentes
3. ❌ Não mencionar responsividade
4. ❌ Esquecer de pedir revisão antes de commit
5. ❌ Pedir Grid quando Flexbox seria adequado

---

## 🎯 Template Rápido: Prompt Completo para Nova Feature

```markdown
## Para o Product Manager

Contexto: [Descreva o problema ou oportunidade]

Objetivo: [O que queremos alcançar]

Usuários: [Quem será impactado]

Dados: [Métricas atuais relevantes]

Requisitos:
- [Requisito funcional 1]
- [Requisito funcional 2]
- [Requisito não-funcional]

Prioridade: [Alta/Média/Baixa] porque [justificativa]

Entregáveis necessários:
- [ ] User story completa
- [ ] Fluxos detalhados
- [ ] Acceptance criteria
- [ ] Definition of Done

---

## Para o Frontend Engineer (após ter spec do PM)

Implementar: [Nome da feature com base na spec do PM]

Arquivos:
- [Listar arquivos a criar/modificar]

Componentes reutilizáveis:
- [Checar em src/components/ui/]

Layout:
- Flexbox com gap-[X]
- Responsivo: [especificar breakpoints]
- [Outros requisitos de layout]

Requisitos técnicos:
- [Server ou Client Component]
- [APIs a consumir]
- [Estados: loading, error, success]
- [Acessibilidade: roles, aria-labels]

Performance:
- [Requisitos de performance]

Importante:
- NÃO commitar sem aprovação
- Reutilizar componentes existentes
- Zero uso de Grid/space-*/margin-top-bottom
- Código autoexplicativo

Entregáveis:
1. Estrutura proposta
2. Código implementado
3. Diff para revisão
```

---

## 📖 Exemplos de Conversas Multi-Agente

### Exemplo 1: Feature do Zero

```
[Usuário → PM]
Precisamos de uma feature de favoritos. Usuários querem salvar produtos
para ver depois. Vejo isso em 30% dos tickets de suporte.

[PM → Usuário]
Entendido. Vou criar especificação completa...
[PM gera user story, fluxos, acceptance criteria]

[Usuário → Engineer]
@Frontend-Engineer implementar esta spec: [link para spec do PM]

[Engineer → Usuário]
Analisando spec... Tenho dúvida: onde mostrar lista de favoritos?
Header dropdown ou página dedicada?

[Usuário → PM]
@Product-Manager qual a melhor abordagem?

[PM → Usuário]
Recomendo dropdown no header (acesso rápido) + página full para gestão.
Vou atualizar spec...

[Usuário → Engineer]
@Frontend-Engineer pode prosseguir com abordagem do PM

[Engineer → Usuário]
Implementado! Aqui está o diff:
[mostra mudanças]
Reutilizei: Button, Card, Dropdown do UI
Layout: Flexbox com gap-4
Pronto para você revisar antes de commitar.
```

### Exemplo 2: Bug + Melhoria

```
[Usuário → Engineer]
Bug: filtros não funcionam no mobile. Dropdown fica cortado.

[Engineer → Usuário]
Investigando...
Encontrei: dropdown usa position:absolute mas parent não tem relative.
Também notei: estamos usando Grid aqui (deveria ser Flex).

Proposta:
1. Fix do bug (position relative)
2. Refactor Grid → Flexbox (alinha com padrão)

Posso fazer ambos ou só o fix urgente?

[Usuário → PM]
@Product-Manager vale refatorar agora ou depois?

[PM → Usuário]
Prioridade no fix do bug (afeta mobile = 70% usuários).
Refactor: adicionar ao backlog técnico.

[Usuário → Engineer]
@Frontend-Engineer só o fix por agora

[Engineer → Usuário]
Fix aplicado. Testei em iOS e Android.
Diff pronto para revisão. NÃO comitei.
```

---

## ✨ Conclusão

**Prompts eficazes têm:**
- 🎯 Contexto claro
- 📋 Requisitos específicos
- 📊 Dados quando disponíveis
- 🔍 Nível de detalhe apropriado
- ⚡ Ação esperada clara
- 🚦 Prioridade definida

**Use este guia como referência**, mas adapte ao seu contexto e necessidades específicas!