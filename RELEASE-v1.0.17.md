## CF Link 1.0.17 — opções de inicialização do QS

No **QS Windows x64 e x86**, a tela principal passa a oferecer:

- **Iniciar com o Windows**, marcado por padrão: na primeira abertura pelo
  pacote portátil original, registra o QS para iniciar ao entrar na conta
  atual do Windows. Desmarcar remove essa inicialização.
- **Iniciar minimizado**, marcado por padrão: o QS abre minimizado na barra
  de tarefas. Desmarcar faz as próximas aberturas mostrarem a janela normal.

As escolhas ficam salvas e são preservadas nas próximas aberturas e atualizações.
Para ver o ID, a senha e as opções após iniciar minimizado, clique no ícone do
QS na barra de tarefas. Fechar o QS continua encerrando o aplicativo.

A inicialização usa o executável portátil original: mantenha-o na mesma pasta.
Se movê-lo, abra-o uma vez no novo local para atualizar o caminho. O recurso
é da conta atual, não instala serviço e não disponibiliza suporte antes do login.
Falhas ao configurar a inicialização são mostradas junto às opções.

| Plataforma | Full | QS |
|---|---|---|
| Windows x64 | 1.0.17, instalador | 1.0.17, portátil com as novas opções |
| Windows x86 | Não disponibilizado | 1.0.17, portátil com as novas opções |
| macOS Apple Silicon ARM64 | 1.0.2, DMG preservado | 1.0.2, DMG preservado |

O Full não recebe essas opções. A biblioteca nativa QS x64 e o QS x86 são
recompilados com o novo módulo; o Full mantém sua biblioteca nativa verificada,
com interface e wrapper recompilados para 1.0.17. macOS não foi recompilado.

Validação: três testes nativos verificaram padrões/opt-out, caminhos com
espaços e ativação/remoção em uma chave de registro isolada, sem modificar a
inicialização real do computador de testes. O HTML real do Sciter x86 passou
por início minimizado, permanência nesse estado, opções marcadas, desmarque
e confirmação de atualização. Análise Dart sem erros novos. Login real do
Windows, sessão remota, instalação/UAC e Windows 7 SP1 continuam para o piloto.

Fontes sanitizados: `CFLink-1.0.17-source.zip`,
`CFLink-1.0.17-qs-x86-source.zip` e `CFLink-1.0.2-source.zip` para os DMGs.
Senha operacional, endereços ID/relay e chave pública são omitidos dos fontes
públicos. Confira os hashes e o manifesto dos arquivos finais.

Base RustDesk 1.5.0, GNU AGPLv3; créditos preservados em **Sobre**.
