# Bethlehem Presenter — v0.26.0

**Software de apresentação para cultos ao vivo da Assembleia de Deus — Ministério do Belém (AD Belém).**

O Bethlehem Presenter é o sistema de projeção desenvolvido para as igrejas do
Ministério do Belém: monta o culto (louvores, Bíblia, avisos, vídeos, imagens e
apresentações), mostra a Prévia ao operador e leva ao Telão, ao Palco
(monitor de retorno com próximo slide, relógio e cronômetros) e à Transmissão,
cada saída na sua própria tela. Funciona sem internet durante o culto.

O **Editor de Apresentações** permite criar slides com texto, imagens, formas,
fundos e vídeos dentro de caixas (sem som, repetindo), guardá-los na Biblioteca
e usá-los nos cultos; as mudanças feitas num culto podem voltar para a Biblioteca.
Apresentações do PowerPoint, Keynote e LibreOffice (.pptx, .ppsx, .ppt, .pps,
.key e .odp) viram slides editáveis; .ppt, .pps, .key e .odp são convertidos
antes pelo PowerPoint, Keynote ou LibreOffice instalado no computador. Slides
com gráficos ou tabelas ficam como imagem, com os textos disponíveis para edição.

Este repositório publica **somente os instaladores e o feed de atualização
automática**. O código-fonte é mantido em repositório privado do ministério.

## Baixar

| Plataforma | Situação | Download |
|---|---|---|
| macOS 11+ (Apple Silicon e Intel) | Disponível (versão de teste) | [Bethlehem-Presenter_universal.dmg](https://github.com/wsgutnik/bethlehem-presenter-releases/releases/latest/download/Bethlehem-Presenter_universal.dmg) |
| Windows 11 (x64) | Instalador de teste (sem atualização automática) | [Releases](https://github.com/wsgutnik/bethlehem-presenter-releases/releases/latest) (arquivo `Bethlehem-Presenter_x64-setup.exe`) |

Versões anteriores ficam em [Releases](https://github.com/wsgutnik/bethlehem-presenter-releases/releases).

Quem já tem o app instalado (v0.4.0 ou mais nova) recebe esta versão sozinho:
aparece o aviso **"Instalar e reiniciar"**, que nunca é mostrado durante um
culto ao vivo.

### Primeira instalação no Mac

1. Abra o `.dmg` e arraste **Bethlehem Presenter** para **Aplicativos**.
2. Abra o app. O macOS vai avisar que ele não é assinado pela Apple; clique em **OK**.
3. Vá em **Ajustes do Sistema → Privacidade e Segurança**, role até o fim e
   clique em **Abrir Mesmo Assim**.

Se o macOS disser que o app "está danificado", rode no Terminal:

```sh
xattr -dr com.apple.quarantine "/Applications/Bethlehem Presenter.app"
```

### Primeira instalação no Windows (versão de teste)

1. Em [Releases](https://github.com/wsgutnik/bethlehem-presenter-releases/releases/latest), baixe
   o `Bethlehem-Presenter_x64-setup.exe` (o instalador do Windows pode
   aparecer na lista só alguns minutos depois do instalador do Mac).
2. O instalador não é assinado: o Windows (SmartScreen) vai avisar. Clique em
   **Mais informações → Executar assim mesmo**.
3. Ainda não há atualização automática no Windows: baixe cada nova versão em
   Releases. As estatísticas de uso funcionam como no Mac (Ajustes →
   Estatísticas de uso).

## Novidades da v0.26.0

v0.26.0
- Estatísticas de uso anônimas: o app envia uma vez por dia a versão, o sistema, a congregação e contagens de uso (cultos, minutos ao vivo, slides por tipo, telas, importações). Nunca envia letras, textos, nomes, arquivos ou endereço IP.
- Para ver exatamente o que é enviado, ou desligar: Ajustes › Estatísticas de uso.
- Agora sabemos quantas vezes cada versão foi baixada: os instaladores ficam na página de Releases do GitHub.
- Windows: instalador de teste disponível na mesma página (ainda sem atualização automática; baixe cada nova versão por lá).
- Importações de PowerPoint e Keynote passam a contar nas estatísticas.

## Sobre este build

Gerado automaticamente pelo GitHub Actions a partir do código-fonte privado. Esta
versão só é publicada aqui depois que a compilação termina sem erro.

| | |
|---|---|
| Versão | 0.26.0 |
| Publicado em | 2026-10-02 19:27 UTC |
| Commit do código-fonte | `7164a7b` |
| Execução | Package macOS #92 (https://github.com/wsgutnik/bethlehem-presenter/actions/runs/37053853118, acesso restrito à equipe) |
| Compilado em | macOS 26.6.2, binário universal (arm64 + x86_64) |
| Tamanho do .dmg | 39.7 MB |
| SHA-256 do .dmg | `da41d223c1743b4b9b6a26df725b6424344058069a146e212350769ec24292ba` |

Para conferir se o arquivo baixado está íntegro, rode no Terminal e compare
com o SHA-256 acima:

```sh
shasum -a 256 ~/Downloads/Bethlehem-Presenter_universal.dmg
```

O pacote de atualização (`.app.tar.gz`) é assinado digitalmente; o app recusa
qualquer atualização que não tenha sido assinada pela chave do projeto.

## Aviso importante

- **Versão de teste.** O Bethlehem Presenter está em desenvolvimento ativo.
  Teste antes de usar no culto e mantenha um plano B (outro computador ou o
  sistema atual) até a sua equipe ter segurança com ele.
- **Sem garantia.** O software é fornecido "no estado em que se encontra", sem
  garantias de qualquer tipo. O uso é de responsabilidade de cada igreja e
  operador.
- **Uso interno do ministério.** Destinado às igrejas e congregações da AD
  Belém. Não é um produto comercial.
- **Não é assinado pela Apple.** Ainda não há assinatura Developer ID nem
  notarização, por isso o aviso de segurança na primeira abertura.
- **Direitos autorais do conteúdo.** Letras de músicas, imagens, vídeos e
  traduções bíblicas pertencem aos seus respectivos detentores. Cada igreja é
  responsável pelas licenças de uso e projeção (por exemplo, CCLI) do conteúdo
  que apresenta.
- **Privacidade.** O app funciona offline durante o culto. Ele envia **estatísticas anônimas de uso** ao servidor do ministério
  (`bp-usage.bp-usage-worker.workers.dev`): versão do app, sistema (macOS/Windows e versão), a
  congregação escolhida em Ajustes e contagens de uso (aberturas, cultos,
  minutos ao vivo, slides por tipo, telas, importações). Nunca envia conteúdo,
  letras, textos, nomes de pessoas, títulos ou arquivos. Para desligar:
  **Ajustes → Estatísticas de uso**. Fora isso, ele só se conecta
  à internet para verificar e baixar atualizações neste repositório,
  sincronizar a Biblioteca na Nuvem do ministério (Google Drive) e, se o
  operador quiser, fazer login com Google para enviar arquivos. O controle
  remoto pelo celular funciona apenas na rede local e vem desligado.
- **Marcas.** Bethlehem Presenter não é afiliado à Apple, à Microsoft, ao
  Google nem à Renewed Vision (ProPresenter). Os nomes citados pertencem aos
  seus donos.

Dúvidas ou problemas: fale com a equipe de mídia ou tecnologia da sua
congregação.

---

_Bethlehem Presenter is the live worship presentation software of Assembleia
de Deus — Ministério do Belém. This repository only hosts installers and the
auto-update feed; the source code is private. Test builds, provided as is,
without warranty. The app sends anonymous usage statistics (no content or
personal data) when a statistics server is configured; turn them off in
Ajustes._
