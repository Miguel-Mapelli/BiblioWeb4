# BiblioWeb — novo protótipo acadêmico

Protótipo front-end de um sistema acadêmico de biblioteca, desenvolvido do zero com HTML, CSS e JavaScript puro. Inspirado nos fluxos públicos do Pergamum: catálogo online, pesquisa simples e avançada, consulta de exemplares e localização, área do usuário (“Meu BiblioWeb”), empréstimos, renovações, reservas, histórico e área administrativa para catalogação e circulação.

> **Importante:** este projeto é uma simulação acadêmica. Não possui backend, banco de dados remoto, autenticação segura, envio de e-mails nem integração com o Pergamum. Os dados são fictícios e ficam no `localStorage` do navegador.

## Como executar

1. Extraia a pasta `BiblioWeb-Novo`.
2. Abra `index.html` em um navegador atualizado (Chrome, Edge ou Firefox).
3. Não é necessário instalar dependências ou iniciar servidor.
4. Para zerar os dados, use **Restaurar dados de demonstração** no rodapé.

## Contas de demonstração

A senha é apenas ilustrativa: digite qualquer valor. O protótipo valida a matrícula/e-mail e o perfil selecionado, não a senha.

| Perfil | Nome | Matrícula | E-mail |
|---|---|---|---|
| Estudante | Ana Clara Souza | `2024001` | `ana@biblioweb.local` |
| Estudante | Bruno Martins | `2024002` | `bruno@biblioweb.local` |
| Bibliotecária | Marina Oliveira | `BIB001` | `marina@biblioweb.local` |
| Estudante | Lucas Ferreira | `2024003` | `lucas@biblioweb.local` |
| Estudante | Camila Rocha | `2024004` | `camila@biblioweb.local` |

## Funcionalidades incluídas

### Catálogo público
- Pesquisa por todos os campos, título, autor, assunto, editora e ISBN.
- Pesquisa avançada por tipo, assunto, ano e disponibilidade.
- Ordenação por relevância, título ou ano; visualização em grade ou lista.
- Detalhes bibliográficos e lista de exemplares com situação e localização.
- Cesta de materiais e impressão da lista.

### Área do estudante
- Resumo da conta, empréstimos, reservas, histórico e dados cadastrais.
- Renovação de empréstimos conforme as regras locais.
- Solicitação e cancelamento de reservas quando todos os exemplares estão emprestados.
- Fila de espera e aviso visual de material liberado para retirada.

### Área da biblioteca
- Cadastro, edição e exclusão de títulos.
- Inclusão de exemplares físicos por título.
- Registro de empréstimos e devoluções.
- Gestão de fila de reservas e confirmação de retirada.
- Cadastro e ativação/desativação de usuários.
- Indicadores simples e exportação/importação de backup JSON.
- Configuração de prazo, limite de empréstimos e renovações.

## Regras simuladas

- Prazo padrão: 14 dias.
- Limite: 3 empréstimos ativos por estudante.
- Renovação: até 2 vezes, se não houver atraso nem reserva pendente para o título.
- Reserva: somente quando não há exemplar disponível.
- Retirada da reserva liberada: 2 dias corridos; ao expirar, a fila avança para o próximo usuário.
- O mesmo estudante não pode manter dois empréstimos ativos do mesmo título.

As regras são parâmetros fictícios de demonstração e podem ser ajustadas na área administrativa.

## Roteiro rápido para apresentar

1. Abra o catálogo e pesquise “programação”.
2. Abra os detalhes de um livro e mostre a localização e disponibilidade de cada exemplar.
3. Entre como Ana (`2024001`) e mostre empréstimos, renovação e histórico.
4. Saia e entre como Marina (`BIB001`, perfil Bibliotecário).
5. Cadastre um título e acrescente um exemplar; registre um empréstimo para um estudante.
6. Registre uma devolução e mostre a fila de reservas quando aplicável.
7. Abra Relatórios e exporte o backup JSON.

## Estrutura

- `index.html` — estrutura das páginas e componentes.
- `styles.css` — identidade visual, componentes e responsividade.
- `app.js` — dados de demonstração, navegação, regras e persistência local.

## Referência funcional e limites de inspiração

A organização dos fluxos foi inspirada nas funcionalidades publicamente descritas para o Pergamum, sem copiar código, marca ou telas proprietárias. O Pergamum é um produto real de gestão de informação; este BiblioWeb é apenas um protótipo independente e simplificado.
