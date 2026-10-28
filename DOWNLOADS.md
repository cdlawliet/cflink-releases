# Links de download para o site

Estes links apontam para os arquivos da release marcada como mais recente:

| Pacote | Link estável |
|---|---|
| Windows Full x64 — instalador | https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-Windows-Full-install.exe |
| Windows QS x64 — portátil | https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-Windows-QS.exe |
| macOS Full — Apple Silicon ARM64 | https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-macOS-Full-arm64.dmg |
| macOS QS — Apple Silicon ARM64 | https://github.com/cdlawliet/cflink-releases/releases/latest/download/CFLink-macOS-QS-arm64.dmg |
| SHA-256 | https://github.com/cdlawliet/cflink-releases/releases/latest/download/SHA256SUMS.txt |
| Manifesto da release | https://github.com/cdlawliet/cflink-releases/releases/latest/download/release-manifest.json |

Para acompanhar atualizações sem alterar o site, mantenha os mesmos nomes de
assets nas próximas releases e marque a versão nova como a mais recente.
Publique todos os quatro instaladores antes de disponibilizar a release.
O sufixo `-install.exe` do Full Windows deve ser preservado.

Para fixar especificamente a versão 1.0.2, substitua `/releases/latest/download/`
por `/releases/download/v1.0.2/` nos links acima.

Release 1.0.2: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.2

Fontes da versão: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.2/CFLink-1.0.2-source.zip

O ZIP de fontes é o código modificado do CF Link. Os arquivos automáticos
“Source code” do GitHub neste repositório contêm apenas a documentação de
downloads e não substituem o pacote de fontes do aplicativo.

## Release v1.0.3

Windows Full e QS estão na versão 1.0.3. Os mesmos links estáveis de macOS
continuam entregando os DMGs 1.0.2. A release informa as versões separadamente.

Windows — fontes: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.3/CFLink-1.0.3-source.zip

Cada asset tem um label terminado em `vX.Y.Z`, com sua versão real, por exemplo
`CFLink-macOS-QS-arm64.dmg - v1.0.2`. Preserve essa convenção ao publicar: o
aplicativo usa a versão do asset para não oferecer um download antigo como novo
em releases que misturam versões de plataformas diferentes.

## Release v1.0.4

Windows Full e QS estão na versão 1.0.4, com a versão visível na tela principal.
Os downloads macOS permanecem em 1.0.2. Os links estáveis acima não mudaram.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.4

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.4/CFLink-1.0.4-source.zip

## Release v1.0.5

Windows Full e QS têm atualização interna com download, verificação SHA-256 e
confirmação para aplicar e reiniciar. A instalação inicial da 1.0.5 é manual
para quem usa versões anteriores. Os DMGs macOS permanecem na versão 1.0.2.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.5

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.5/CFLink-1.0.5-source.zip

Para a atualização interna, a API do asset precisa informar `size` e `digest`
SHA-256. Preserve os nomes estáveis e os labels com a versão real por plataforma.

## Release v1.0.6

Windows Full e QS passam à 1.0.6 para testar a atualização interna a partir da
1.0.5, mantendo as funcionalidades. macOS continua na 1.0.2. Os links estáveis
permanecem iguais.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.6

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.6/CFLink-1.0.6-source.zip

## Release v1.0.7

Windows Full e QS corrigem a inicialização do atualizador e reorganizam o
rodapé. Usuários da 1.0.5/1.0.6 precisam instalar a 1.0.7 manualmente uma vez,
pois a chamada defeituosa fica no aplicativo antigo. macOS continua na 1.0.2.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.7

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.7/CFLink-1.0.7-source.zip

## Release v1.0.8

O Full abre o instalador mesmo com nomes `install (1).exe`/`install (2).exe`,
sem depender do nome atribuído pelo navegador. QS continua portátil. O
assistente reutiliza o diretório da instalação já registrada. macOS permanece
na 1.0.2; os links estáveis não mudaram.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.8

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.8/CFLink-1.0.8-source.zip

## Release v1.0.9

Versão Windows Full/QS para testar a atualização a partir da 1.0.8, mantendo
suas funcionalidades. macOS permanece na 1.0.2; links estáveis preservados.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.9

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.9/CFLink-1.0.9-source.zip

## Release v1.0.10

Windows Full/QS verificam atualizações em toda abertura da tela principal.
Download e instalação continuam dependendo da escolha do usuário. As
consultas periódicas, com o app aberto, mantêm o intervalo diário.
macOS permanece nos DMGs 1.0.2; os links estáveis foram preservados.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.10

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.10/CFLink-1.0.10-source.zip

## Release v1.0.11

O Full instalado verifica/inicia seu serviço ao abrir, com UAC quando
necessário, e oferece reparo pela rotina original se o serviço não existir
ou apontar para outro executável. QS e Full portátil não controlam serviços.
macOS permanece na 1.0.2; os links estáveis foram preservados.

Release: https://github.com/cdlawliet/cflink-releases/releases/tag/v1.0.11

Fontes Windows: https://github.com/cdlawliet/cflink-releases/releases/download/v1.0.11/CFLink-1.0.11-source.zip
