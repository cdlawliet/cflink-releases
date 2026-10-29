# CF Link — CF Tecnologia

Aplicativo de suporte remoto para receber atendimento ou acessar outros
computadores, baseado no RustDesk e personalizado pela CF Tecnologia.
Os aplicativos já vêm preparados para usar a infraestrutura de atendimento
da empresa, sem necessidade de configurar um servidor.

## Downloads

**Windows: 1.0.13. macOS: 1.0.2.** Escolha seu sistema e o tipo de uso:

| Sistema | Full — realizar e receber acesso | QS — somente receber suporte |
|---|---|---|
| Windows x64 — **1.0.13** | [Baixar Full — instalador](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-Windows-Full-install.exe) | [Baixar QS — portátil](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-Windows-QS.exe) |
| macOS 12.3 ou posterior, Apple Silicon — **1.0.2** | [Baixar Full — DMG ARM64](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-macOS-Full-arm64.dmg) | [Baixar QS — DMG ARM64](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-macOS-QS-arm64.dmg) |

[Ver todos os arquivos e versões](https://github.com/cdlawliet/cflink-releases/releases)

O Windows 1.0.13 restaura **Lembrar senha** e corrige sessões recentes e
favoritos quando a pasta Documentos não está disponível. Registros existentes
são preservados, sem necessidade de trocar o ID.

A versão Windows também tenta registrar automaticamente o serviço
ausente no Full instalado, usando a mesma rotina do botão Iniciar Serviço.
O Windows pode solicitar autorização de administrador e o Full pode reabrir.
As funcionalidades da versão 1.0.3 estão preservadas nos pacotes Windows. Os DMGs permanecem
na versão 1.0.2, sem essas alterações, até a próxima compilação no Mac.
Os pacotes macOS desta publicação são para Apple Silicon. Não há pacote para
Mac Intel, Android ou iOS nesta release.

## Qual versão escolher?

**CF Link Full:** permite iniciar conexões com outros dispositivos e receber
acesso remoto. No Windows, oferece instalação para uso recorrente.

**CF Link QS:** indicado para quem precisa receber atendimento. Não inicia
conexões com outros dispositivos. No Windows, é portátil e não precisa de
instalação; mantenha o aplicativo aberto durante o suporte.

As duas versões têm a identidade CF Link, interface em português e tema escuro
fixo. O servidor de atendimento é predefinido e não pode ser editado na interface.

## Como receber atendimento

1. Baixe e abra o CF Link QS do seu sistema.
2. Informe o ID exibido ao profissional que prestará o suporte.
3. Para autorizar, compartilhe a senha temporária exibida **ou** aprove a
   solicitação de conexão no próprio aplicativo.
4. Ao terminar, desconecte a sessão e feche o QS para encerrar a disponibilidade.

Quem tiver o ID e a senha temporária poderá conectar sem uma aprovação
adicional. Compartilhe esses dados apenas com o profissional que você autorizou.
No Windows 1.0.3, a senha padrão predefinida pelo responsável pelo projeto
também autoriza o acesso, sem aparecer na tela principal. Quem conhecer o ID e
uma das senhas aceitas poderá conectar sem aprovação adicional. Ao iniciar uma
nova conexão pelo Full, digite a senha do cliente. No Windows 1.0.13, você
pode marcar **Lembrar senha** para reutilizá-la nas próximas conexões com
aquele computador. A senha padrão de recebimento não é preenchida automaticamente.

## Instalação e permissões

### Windows

Para uso recorrente, execute o instalador Full e siga as instruções na tela.
O assistente preenche o diretório da instalação existente. Escolha **Aceitar
e instalar** para substituir essa instalação e autorize o Windows quando
solicitado. Para Full portátil, execute o pacote com `--noinstall`.
Para receber suporte pontual, abra o executável QS. Ao atualizar manualmente,
feche a versão anterior antes de instalar ou abrir o novo pacote.

No Full instalado, o rodapé mostra **Serviço ativo** quando o serviço está
funcionando. Se estiver parado, o aplicativo tenta iniciá-lo e poderá solicitar
autorização de administrador. Se estiver ausente, tenta registrar o serviço
automaticamente, preservando o ID/configurações e reabrindo o Full. Em caso
de falha ou caminho incorreto, **Reparar serviço** continua disponível.
O reparo pode interromper conexões. Há proteção contra repetição automática
de uma tentativa recente que falhou.
QS e Full portátil não instalam nem controlam serviços.

### macOS

Abra o DMG, copie o aplicativo para **Aplicativos** e abra-o. Para receber
controle remoto, autorize **Gravação da Tela** e **Acessibilidade** nas
configurações de Privacidade e Segurança do macOS. Reinicie o aplicativo
se o sistema solicitar após conceder as permissões.

Os pacotes desta versão não possuem assinatura comercial Authenticode no
Windows nem notarização Apple no macOS. O sistema pode exibir uma confirmação
de segurança ao abri-los; confira a origem e os hashes disponíveis na release.

## Atualizações

Desde o Windows 1.0.3, o aplicativo pode consultar este repositório e avisar
sobre um novo pacote compatível. Na **1.0.10**, a consulta inicial acontece em
toda abertura da tela principal, mesmo que já tenha verificado no mesmo dia.
Mantendo o aplicativo aberto, as consultas posteriores continuam limitadas a
uma por dia. “Verificar atualização” permite consultar manualmente.

Desde o Windows **1.0.7**, escolha **Atualizar agora** para baixar com progresso
e conferir o arquivo. Você pode cancelar ou adiar. Ao confirmar **Atualizar e
reiniciar**, as conexões são interrompidas, o pacote é aplicado e o aplicativo
reabre. No Full instalado, autorize o Windows quando solicitar administrador.
No QS e Full portátil, feche outras janelas do mesmo aplicativo antes de atualizar.
O portátil guarda o executável anterior com a extensão `.previous`.

Quem usa **1.0.6 ou anterior precisa baixar e instalar/abrir uma versão recente manualmente**
pela tabela acima. Nas versões 1.0.5/1.0.6, o download pode terminar e a aplicação
falhar após confirmar o reinício; a 1.0.7 corrige a inicialização do atualizador.
macOS permanece na versão 1.0.2, sem esse recurso nos DMGs atuais.

Após instalar uma versão recente, **Verificar atualização** consulta as próximas versões.
Ao atualizar, confira a versão na tela principal e após reabrir pelo mesmo
arquivo/atalho.

As atualizações são distribuídas por este repositório. Baixe o pacote mais
recente na tabela acima e substitua a versão anterior. O atualizador do
RustDesk original fica desabilitado nos clientes CF Link.

## Licença, créditos e código-fonte

CF Link é uma versão modificada do **RustDesk 1.5.0**, distribuída sob a
**GNU Affero General Public License v3**. Os créditos, a licença completa e a
identificação da versão podem ser consultados em **Sobre / Licenças** no aplicativo.

- [Código-fonte do CF Link e instruções de compilação](https://github.com/cdlawliet/CFLink)
- [Pacote de fontes macOS 1.0.2](https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.2/CFLink-1.0.2-source.zip)
- [Pacote de fontes Windows 1.0.13](https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.13/CFLink-1.0.13-source.zip)
- [Licença completa](LICENCE)
- [Projeto original RustDesk](https://github.com/rustdesk/rustdesk)
- [Hashes SHA-256 dos arquivos publicados](https://github.com/cdlawliet/cflink-releases/releases/latest/download/SHA256SUMS.txt)

Copyright dos autores originais preservado. Personalização e identidade visual:
**CF Tecnologia**. O software é fornecido nos termos e limites de garantia da licença.
