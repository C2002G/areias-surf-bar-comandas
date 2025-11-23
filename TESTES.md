# 🧪 Guia de Testes - Sistema de Comandas PWA

Este guia ajuda a validar todas as funcionalidades do app de forma sistemática.

## ✅ Lista de Testes

### 1. Teste de Instalação e PWA

#### Teste 1.1: Carregamento Inicial

- [ ] App carrega sem erros no console
- [ ] Interface aparece corretamente
- [ ] Service Worker registra sem erros
- [ ] Manifest.json é válido

#### Teste 1.2: Instalação PWA

- [ ] Navegador sugere "Adicionar à tela inicial"
- [ ] App instala como PWA nativo
- [ ] Ícone aparece na tela inicial
- [ ] App abre em fullscreen quando instalado

### 2. Teste de Funcionalidades Básicas

#### Teste 2.1: Criar Nova Comanda

- [ ] Botão "Nova Comanda" funciona
- [ ] Campo nome do cliente é obrigatório
- [ ] Campo mesa é opcional
- [ ] Pode adicionar itens com Enter ou botão
- [ ] Itens aparecem na lista corretamente
- [ ] Pode editar itens clicando neles
- [ ] Pode remover itens
- [ ] Salvar comanda funciona
- [ ] Volta para lista após salvar

#### Teste 2.2: Listar Comandas

- [ ] Comandas aparecem na lista principal
- [ ] Ordenação por data (mais recente primeiro)
- [ ] Mostra nome do cliente
- [ ] Mostra número da mesa (se houver)
- [ ] Mostra quantidade de itens
- [ ] Mostra horário formatado
- [ ] Estado vazio aparece quando não há comandas

#### Teste 2.3: Buscar Comandas

- [ ] Campo de busca funciona em tempo real
- [ ] Busca por nome do cliente
- [ ] Busca por número da mesa
- [ ] Busca por itens do pedido
- [ ] Limpar busca mostra todas as comandas

#### Teste 2.4: Visualizar Comanda

- [ ] Toque na comanda abre detalhes
- [ ] Mostra nome do cliente
- [ ] Mostra mesa (se houver)
- [ ] Mostra horário de criação
- [ ] Lista todos os itens
- [ ] Botões de ação funcionam

#### Teste 2.5: Editar Comanda

- [ ] Botão editar funciona
- [ ] Carrega dados atuais no formulário
- [ ] Pode alterar nome e mesa
- [ ] Pode adicionar/remover/editar itens
- [ ] Salvar atualiza a comanda
- [ ] Volta para visualização após salvar

#### Teste 2.6: Excluir Comanda

- [ ] Botão excluir funciona
- [ ] Modal de confirmação aparece
- [ ] Cancelar não exclui
- [ ] Confirmar exclui a comanda
- [ ] Volta para lista após excluir
- [ ] Toast de sucesso aparece

### 3. Teste de Integração WhatsApp

#### Teste 3.1: Copiar Pedido

- [ ] Botão "Copiar para WhatsApp" funciona
- [ ] Texto é copiado para área de transferência
- [ ] Toast de confirmação aparece
- [ ] Formato está correto:
  ```
  Cliente: Nome
  Mesa: Número (se houver)
  Pedido:
  - Item 1
  - Item 2
  Horário: Data/hora
  ```

#### Teste 3.2: Integração Manual

- [ ] Texto copiado cola corretamente no WhatsApp
- [ ] Formatação se mantém no WhatsApp
- [ ] Caracteres especiais funcionam

### 4. Teste de Configurações

#### Teste 4.1: Estatísticas

- [ ] Botão configurações funciona
- [ ] Mostra total de comandas corretamente
- [ ] Mostra comandas de hoje corretamente
- [ ] Números se atualizam quando comandas mudam

#### Teste 4.2: Apagar Todas

- [ ] Botão "Apagar todas" funciona
- [ ] Modal de confirmação aparece
- [ ] Cancelar não apaga
- [ ] Confirmar apaga todas as comandas
- [ ] Lista fica vazia
- [ ] Estado vazio aparece

### 5. Teste de Responsividade

#### Teste 5.1: Mobile (320px - 768px)

- [ ] Layout se adapta corretamente
- [ ] Botões são tocáveis (44px mínimo)
- [ ] Texto é legível
- [ ] Formulários funcionam bem
- [ ] Navegação é fluida

#### Teste 5.2: Tablet (768px - 1024px)

- [ ] Layout usa espaço disponível
- [ ] Cards podem aparecer em grid
- [ ] Interface não fica esticada
- [ ] Botões mantêm tamanho adequado

#### Teste 5.3: Desktop (1024px+)

- [ ] Largura máxima respeitada
- [ ] Layout centralizado
- [ ] Funcionalidades mantidas
- [ ] Performance é boa

### 6. Teste de Performance

#### Teste 6.1: Carregamento

- [ ] App carrega em menos de 2 segundos
- [ ] Não há travamentos na interface
- [ ] Transições são suaves
- [ ] Sem memory leaks detectados

#### Teste 6.2: Operações

- [ ] Criar comanda é instantâneo
- [ ] Busca responde em tempo real
- [ ] Navegação é fluida
- [ ] Sem atrasos perceptíveis

### 7. Teste Offline

#### Teste 7.1: Funcionamento Offline

- [ ] App funciona sem internet
- [ ] Dados salvos persistem offline
- [ ] Todas as funcionalidades mantidas
- [ ] Sem erros no console offline

#### Teste 7.2: Cache

- [ ] Resources são cacheados
- [ ] App carrega offline
- [ ] Service Worker intercepta requests
- [ ] Fallback offline funciona

#### Teste 7.3: Persistência

- [ ] Fechar e reabrir mantém dados
- [ ] Reiniciar navegador mantém dados
- [ ] Dados não se perdem
- [ ] IndexedDB funciona corretamente

### 8. Teste de Compatibilidade

#### Teste 8.1: Navegadores

- [ ] Chrome/Edge: Todas as funcionalidades
- [ ] Firefox: Todas as funcionalidades
- [ ] Safari: Funcionalidades essenciais
- [ ] Mobile browsers: Responsivo

#### Teste 8.2: Dispositivos

- [ ] Android: PWA instala e funciona
- [ ] iOS: Funciona no Safari
- [ ] Windows: PWA instala
- [ ] Diferentes resoluções

### 9. Teste de Usabilidade

#### Teste 9.1: Fluxo do Usuário

- [ ] Fluxo criar → visualizar → editar é intuitivo
- [ ] Navegação é clara
- [ ] Botões são auto-explicativos
- [ ] Feedback visual adequado

#### Teste 9.2: Acessibilidade

- [ ] Contraste adequado
- [ ] Texto legível
- [ ] Botões grandes o suficiente
- [ ] Funciona com teclado

### 10. Teste de Estresse

#### Teste 10.1: Volume de Dados

- [ ] Funciona com 50 comandas
- [ ] Funciona com 100 comandas
- [ ] Busca permanece rápida
- [ ] Performance mantida

#### Teste 10.2: Dados Extremos

- [ ] Nomes muito longos
- [ ] Muitos itens por comanda
- [ ] Caracteres especiais
- [ ] Emojis nos textos

## 🚀 Como Executar os Testes

### Setup de Teste

1. Inicie o servidor local: `python -m http.server 8080`
2. Abra `http://localhost:8080` no navegador
3. Abra as DevTools (F12) para monitorar erros
4. Execute cada teste marcando ✅ ou ❌

### Teste Offline

1. Na aba Network das DevTools, marque "Offline"
2. Recarregue a página
3. Execute testes de funcionalidade
4. Desmarque "Offline" quando terminar

### Teste em Mobile

1. Use DevTools > Toggle device toolbar (Ctrl+Shift+M)
2. Teste diferentes resoluções
3. Ou acesse pelo celular na mesma rede: `http://IP_DO_PC:8080`

## 🐛 Relatório de Bugs

Se encontrar problemas durante os testes:

1. **Anotar**:

   - Navegador e versão
   - Resolução de tela
   - Passos para reproduzir
   - Erro no console (se houver)

2. **Prioridades**:

   - 🔴 Crítico: App não funciona
   - 🟡 Alto: Funcionalidade importante quebrada
   - 🟢 Baixo: Problema cosmético

3. **Reportar**:
   - Abrir issue no GitHub
   - Incluir screenshots se necessário
   - Marcar com labels apropriadas

## ✅ Checklist Final

Antes de considerar o app pronto para produção:

- [ ] Todos os testes passaram
- [ ] Sem erros no console
- [ ] PWA instala corretamente
- [ ] Funciona offline
- [ ] Performance adequada
- [ ] Responsivo em todos os tamanhos
- [ ] Compatível com navegadores principais
- [ ] Usabilidade validada
- [ ] Documentação completa

---

**🎯 Meta: 100% dos testes passando para garantir a melhor experiência do usuário!**
