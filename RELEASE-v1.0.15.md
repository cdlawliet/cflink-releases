## CF Link 1.0.15 — correções da interface do QS x86

- O ícone da barra de título/janela do QS 32 bits passa a usar a marca CF Link.
- A janela calcula a altura mínima pelo conteúdo, incluindo os avisos e a
  confirmação de atualização, evitando a rolagem inicial. Se a área útil da
  tela for menor que o conteúdo, mantém rolagem para não esconder os controles.
- **Atualizar e reiniciar** abre a confirmação dentro do QS. **Cancelar** não
  inicia a troca; **Confirmar e reiniciar** prepara o helper e fecha o QS após
  a confirmação de que ele está pronto. Falhas nativas aparecem no aviso do app.

**Quem está no QS x86 1.0.13/1.0.14 com o botão sem responder deve baixar e
abrir o novo portátil manualmente uma vez.** A correção da interface não é
aplicada retroativamente ao executável antigo. Depois, use o fluxo interno
nas próximas versões compatíveis.

| Plataforma | Full | QS |
|---|---|---|
| Windows x64 | 1.0.15, instalador | 1.0.15, portátil |
| Windows x86 | Não disponibilizado | 1.0.15, portátil |
| macOS Apple Silicon ARM64 | 1.0.2, DMG preservado | 1.0.2, DMG preservado |

Os três pacotes Windows acompanham a release principal. O QS x86 foi
recompilado. Nos perfis x64, interface e wrappers foram recompilados com os
metadados 1.0.15, preservando suas bibliotecas nativas verificadas da 1.0.14:
as correções desta versão são específicas do Sciter x86.

Validação: sete testes Python de publicação/privacidade; teste offline do
HTML real no Sciter x86 (altura, confirmação, cancelamento e uma chamada do
aplicador); verificação do ícone da janela nativa; arquitetura e identidade
dos pacotes; três cenários do helper x86 (troca/backup/reabertura e rejeições
por hash/arquitetura). O caminho de preparação `apply()` também foi exercitado
com fixture nativa: plano, handshake ready/go, substituição e reabertura.
Sessão remota real, instalação com UAC e Windows 7 SP1 continuam para o piloto.

Fontes: `CFLink-1.0.15-source.zip`, `CFLink-1.0.15-qs-x86-source.zip` e
`CFLink-1.0.2-source.zip` para os DMGs preservados. Senha operacional, servidores
ID/relay e chave pública são omitidos dos fontes públicos. Configure seus dados
antes de compilar. Confira manifesto e SHA-256 dos arquivos finais.

Base RustDesk 1.5.0, GNU AGPLv3; créditos preservados em **Sobre**.
