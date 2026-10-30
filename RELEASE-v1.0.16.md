## CF Link 1.0.16 — versão para validar a atualização

Nova versão para testar o fluxo de atualização a partir da **1.0.15**.
Não há mudança funcional nesta publicação; as correções do QS x86 da 1.0.15
(ícone da janela, altura pelo conteúdo e confirmação interna) permanecem.

| Plataforma | Full | QS |
|---|---|---|
| Windows x64 | 1.0.16, instalador | 1.0.16, portátil |
| Windows x86 | Não disponibilizado | 1.0.16, portátil |
| macOS Apple Silicon ARM64 | 1.0.2, DMG preservado | 1.0.2, DMG preservado |

### Testar a partir da 1.0.15

1. Abra o aplicativo 1.0.15 e use **Verificar atualização** (no x86, **Verificar**).
2. Baixe a 1.0.16 oferecida para o perfil e a arquitetura corretos.
3. No QS x86, clique **Atualizar e reiniciar** e depois **Confirmar e reiniciar**.
   Antes de confirmar, **Cancelar** deve manter o aplicativo aberto na 1.0.15.
4. Após aceitar, confirme que o QS fecha e reabre exibindo **1.0.16**, com o
   mesmo ID e pronto para suporte. O Full instalado pode solicitar UAC.
5. Confira que a versão 1.0.16 não oferece a si mesma como atualização.

O QS x86 1.0.13/1.0.14 com o botão antigo sem responder precisa de substituição
manual por uma versão corrigida antes deste teste. Não use esses clientes
antigos como validação da confirmação implementada na 1.0.15.

Full/QS x64 têm interface e wrappers recompilados, preservando as bibliotecas
nativas verificadas da 1.0.14, sem mudança de código nativo nesses perfis.
O QS x86 foi recompilado com versão/metadados 1.0.16. macOS não foi recompilado.
Windows 7 SP1 e a atualização real entre computadores continuam para o piloto.

Verificações desta publicação: sete testes Python de preparação/privacidade,
identidade Full/QS x64, metadados 1.0.16 e PE32 do QS x86. O helper x86 passou
nos três cenários isolados: troca com backup e reabertura, rejeição de hash
incorreto e rejeição de arquitetura incorreta. A confirmação na interface
1.0.15 com download real da 1.0.16 é o teste solicitado para o piloto.

Os três pacotes Windows são publicados juntos com os fontes sanitizados
`CFLink-1.0.16-source.zip` e `CFLink-1.0.16-qs-x86-source.zip`. Os DMGs usam
`CFLink-1.0.2-source.zip`. Senha operacional, endereços ID/relay e chave pública
são omitidos dos fontes públicos; preencha sua configuração antes de compilar.
Confira tamanho e SHA-256 em `release-manifest.json` e `SHA256SUMS.txt`.

Base RustDesk 1.5.0, GNU AGPLv3; créditos preservados em **Sobre**.
