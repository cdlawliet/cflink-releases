## CF Link 1.0.14 — QS x86 junto dos pacotes x64

O **QS para Windows 32 bits** passa a acompanhar a release principal, mantendo
o Full x64 e o QS x64. Para receber suporte em Windows 32 bits, baixe
`CFLink-Windows-QS-x86.exe`. O QS x86 usa Sciter e apenas recebe conexões.

| Plataforma | Full | QS |
|---|---|---|
| Windows x64 | 1.0.14, instalador | 1.0.14, portátil |
| Windows x86 (32 bits) | Não disponibilizado | 1.0.14, portátil |
| macOS Apple Silicon ARM64 | 1.0.2, DMG preservado | 1.0.2, DMG preservado |

**Windows 7 SP1 de 32 bits ainda precisa de teste real no piloto.** A presença
do pacote na release principal não certifica compatibilidade com esse sistema.
Consulte `docs/VALIDACAO-WINDOWS-X86.md` nos fontes para o roteiro.

Os três pacotes Windows devem acompanhar todas as próximas releases. A
preparação de publicação agora exige Full x64, QS x64, QS x86 e os dois ZIPs
de fontes Windows; a ausência de um deles interrompe a preparação.

Validação: sete testes Python de preparação/privacidade passaram; bibliotecas
Full/QS x64, metadados 1.0.14 e arquitetura PE32 do QS x86 foram conferidos.
O Full abriu a tela de instalação, sem aceitar a instalação. O atualizador
nativo x86 passou em três cenários: substituir/guardar backup/reabrir, rejeitar
hash incorreto e rejeitar arquitetura incorreta. Sessão remota real, instalação
com UAC e execução no Windows 7 permanecem para validação no piloto.

Os guias e o prompt de personalização exigem retirar senha padrão, endereços
ID/relay e chave pública dos fontes, textos e commits públicos. A configuração
necessária à conexão permanece incorporada nos executáveis autorizados.
Mantidos os recursos de conexão e atualização existentes; o macOS não foi
recompilado e continua em 1.0.2.

Fontes Windows: `CFLink-1.0.14-source.zip` e
`CFLink-1.0.14-qs-x86-source.zip`. Fontes dos DMGs:
`CFLink-1.0.2-source.zip`. Informe sua configuração antes de compilar.
Confira os tamanhos e SHA-256 em `release-manifest.json` e `SHA256SUMS.txt`.
Os arquivos automáticos “Source code” do GitHub contêm apenas a documentação
do repositório de downloads; use os ZIPs CFLink correspondentes.

Base RustDesk 1.5.0, GNU AGPLv3; créditos preservados em **Sobre**.
