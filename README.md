# CF Link — CF Tecnologia

Aplicativo de suporte remoto para receber atendimento ou acessar outros
computadores, baseado no RustDesk e personalizado pela CF Tecnologia.
Os aplicativos já vêm preparados para usar a infraestrutura de atendimento
da empresa, sem necessidade de configurar um servidor.

## Downloads

**Versão atual: 1.0.2.** Escolha seu sistema e o tipo de uso:

| Sistema | Full — realizar e receber acesso | QS — somente receber suporte |
|---|---|---|
| Windows x64 | [Baixar Full — instalador](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-Windows-Full-install.exe) | [Baixar QS — portátil](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-Windows-QS.exe) |
| macOS 12.3 ou posterior, Apple Silicon (M1/M2/M3 e posteriores) | [Baixar Full — DMG ARM64](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-macOS-Full-arm64.dmg) | [Baixar QS — DMG ARM64](https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-macOS-QS-arm64.dmg) |

[Ver todos os arquivos e versões](https://github.com/cdlawliet/cflink-releases/releases)

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
O aplicativo não traz uma senha fixa compartilhada entre os usuários.

## Instalação e permissões

### Windows

Para uso recorrente, execute o instalador Full e siga as instruções na tela.
Para receber suporte pontual, abra o executável QS. Feche a versão anterior
antes de instalar ou abrir uma atualização.

### macOS

Abra o DMG, copie o aplicativo para **Aplicativos** e abra-o. Para receber
controle remoto, autorize **Gravação da Tela** e **Acessibilidade** nas
configurações de Privacidade e Segurança do macOS. Reinicie o aplicativo
se o sistema solicitar após conceder as permissões.

Os pacotes desta versão não possuem assinatura comercial Authenticode no
Windows nem notarização Apple no macOS. O sistema pode exibir uma confirmação
de segurança ao abri-los; confira a origem e os hashes disponíveis na release.

## Atualizações

As atualizações são distribuídas por este repositório. Baixe o pacote mais
recente na tabela acima e substitua a versão anterior. O atualizador do
RustDesk original fica desabilitado nos clientes CF Link.

## Licença, créditos e código-fonte

CF Link é uma versão modificada do **RustDesk 1.5.0**, distribuída sob a
**GNU Affero General Public License v3**. Os créditos, a licença completa e a
identificação da versão podem ser consultados em **Sobre / Licenças** no aplicativo.

- [Código-fonte do CF Link e instruções de compilação](https://github.com/cdlawliet/CFLink)
- [Pacote de fontes da versão 1.0.2](https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.2/CFLink-1.0.2-source.zip)
- [Licença completa](LICENCE)
- [Projeto original RustDesk](https://github.com/rustdesk/rustdesk)
- [Hashes SHA-256 dos arquivos publicados](https://github.com/cdlawliet/cflink-releases/releases/latest/download/SHA256SUMS.txt)

Copyright dos autores originais preservado. Personalização e identidade visual:
**CF Tecnologia**. O software é fornecido nos termos e limites de garantia da licença.
