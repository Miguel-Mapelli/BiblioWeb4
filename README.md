# BiblioWeb — protótipo acadêmico

Protótipo navegável de biblioteca virtual desenvolvido para a disciplina de **Interação Humano-Computador**. O projeto funciona diretamente no navegador, sem instalação, servidor ou banco de dados remoto.

## Como executar

1. Extraia a pasta `BiblioWeb-main`.
2. Abra o arquivo `index.html` em um navegador atualizado (Chrome, Edge ou Firefox).
3. Escolha o perfil **Estudante** ou **Bibliotecário(a)**.
4. Entre com uma das contas de demonstração abaixo ou informe outro nome/e-mail. A senha pode ser qualquer texto fictício.

### Contas de demonstração

| Perfil | Nome | E-mail |
|---|---|---|
| Estudante | Ana Souza | `ana@biblioweb.local` |
| Estudante | Bruno Lima | `bruno@biblioweb.local` |
| Bibliotecário | Marina Costa | `marina@biblioweb.local` |

Use qualquer senha fictícia. O protótipo não verifica senha; o e-mail e o perfil identificam a conta dentro do navegador. **Não informe senhas reais.**

> Se você já abriu uma versão anterior do BiblioWeb neste navegador, use **Reiniciar demonstração** no rodapé para carregar os dados iniciais desta versão. Essa ação apaga as alterações locais atuais.

## Funcionalidades do estudante

- Página inicial com destaques, atalhos e navegação por categorias.
- Busca por título, autor, editora, ISBN, ano e categoria.
- Filtros combináveis por gênero e ordenação de novidades.
- Detalhes do livro, sinopse, ficha técnica e disponibilidade.
- Empréstimo demonstrativo por 15 dias, com limite de 3 empréstimos ativos por conta.
- Reserva em fila quando o título está emprestado; bloqueio de reservas duplicadas.
- Área Minha Conta com empréstimos ativos, reservas, renovação e histórico de devoluções.
- Renovação de 7 dias, uma vez por empréstimo, quando não há atraso nem fila de reserva.
- Cancelamento de reserva e atualização da fila.

## Funcionalidades do bibliotecário

- Painel com indicadores de acervo, empréstimos ativos, atrasos, reservas e contas demonstrativas.
- Registro de atividades recentes.
- Cadastro, edição, pesquisa e exclusão de títulos, com validação para impedir exclusão de livro com movimentação vinculada.
- Gerenciamento de empréstimos, confirmação de devolução e identificação de atrasos.
- Fila de reservas, prioridade de retirada por 3 dias e confirmação da retirada.
- Área de contas demonstrativas: pesquisa, consulta de perfil e ativação/desativação de contas criadas no navegador.
- Exportação dos dados para arquivo JSON e importação de backup JSON.

## Regras demonstrativas

- Cada título representa **um exemplar físico**. Não há controle de múltiplas cópias do mesmo título.
- O empréstimo padrão dura 15 dias e cada conta pode manter até 3 empréstimos ativos.
- Cada empréstimo pode ser renovado uma vez por mais 7 dias, desde que não esteja atrasado e não exista reserva pendente.
- Quando um exemplar é devolvido e há fila, a primeira pessoa recebe prioridade por 3 dias. O bibliotecário confirma a retirada para iniciar o novo empréstimo.
- Se o prazo de retirada expirar, a reserva é cancelada e a próxima pessoa da fila recebe prioridade por 3 dias. Se não houver outra reserva nem empréstimo ativo, o título volta a ficar disponível.
- Os dados iniciais incluem títulos, contas, empréstimos, uma devolução atrasada e uma reserva para facilitar a apresentação.

## Roteiro rápido para apresentação

1. Entre como estudante com `ana@biblioweb.local` e consulte **Minha Conta** para mostrar empréstimos e atraso.
2. Busque `1984`, abra os detalhes e mostre que o livro está emprestado e pode ser reservado.
3. Saia e entre como estudante com `bruno@biblioweb.local` para mostrar a posição na fila de reserva.
4. Entre como bibliotecário com `marina@biblioweb.local` e abra **Empréstimos**.
5. Confirme a devolução de `1984`; a reserva de Bruno deverá ficar pronta para retirada.
6. Confirme a retirada da reserva para iniciar um novo empréstimo de 15 dias.
7. Em **Gerenciar livros**, cadastre um título de teste, edite-o e depois exclua-o.
8. Em **Usuários**, pesquise as contas e teste ativar/desativar uma conta de demonstração.
9. No **Painel**, exporte os dados para JSON. Para recuperar uma cópia, use Importar backup.

## Experiência e acessibilidade

- Layout responsivo e identidade visual consistente.
- Tema claro/escuro com preferência salva no navegador.
- Estados vazios, mensagens de feedback e confirmações para ações importantes.
- Ajuda contextual e orientação inicial.
- Foco visível, rótulos acessíveis e navegação por botões.
- Design tokens CSS para cores, tipografia, espaçamentos, raios, sombras e movimento.

## Dados, privacidade e limitações

- Acervo, contas e movimentações ficam no `localStorage` do navegador; a sessão usa `sessionStorage`.
- Os dados não são compartilhados entre dispositivos ou navegadores.
- O login é uma simulação local. Não existe validação de senha, criptografia de credenciais, backend ou autorização segura no servidor.
- A desativação de conta e as regras de negócio são demonstrações no lado do cliente, não mecanismos de segurança.
- Capas externas da Open Library dependem de conexão; se não carregarem, o sistema mantém as capas gráficas de fallback.
- O protótipo não substitui um sistema de biblioteca real.

## Estrutura dos arquivos

- `index.html`: estrutura, componentes e templates das telas.
- `style.css`: identidade visual, tokens, componentes e responsividade.
- `script.js`: dados de demonstração, estado, persistência e regras de interação.

## Reiniciar a demonstração

Use **Reiniciar demonstração** no rodapé. A confirmação restaura o acervo e as movimentações iniciais, removendo as alterações salvas neste navegador.
