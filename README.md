# Bethlehem Presenter — v0.28.1

**Software de apresentação para cultos ao vivo da Assembleia de Deus — Ministério do Belém (AD Belém).**

O Bethlehem Presenter é o sistema de projeção desenvolvido para as igrejas do
Ministério do Belém: monta o culto (louvores, Bíblia, avisos, vídeos, imagens e
apresentações), mostra a Prévia ao operador e leva ao Telão, ao Palco
(monitor de retorno com próximo slide, relógio e cronômetros) e à Transmissão,
cada saída na sua própria tela. Funciona sem internet durante o culto.
Se uma saída cair por engano na tela do operador, um X (ao passar o mouse) a
leva para um monitor externo livre (se não houver, pergunta antes de desligá-la), e
⌘⌥⇧W (Ctrl+Alt+Shift+W no Windows) traz a tela de trabalho para a frente sem
fechar nenhuma saída.
Os painéis do Ao Vivo podem ser guardados como layouts com nome e ficam
travados durante o culto (opção em Ajustes); há também um modo "dock"
experimental, desligado por padrão, para arrastar e empilhar painéis no Ao
Vivo, no Construtor de culto e no Editor de slides (macOS e Windows; ainda sem
teste em computadores Windows): se algo estranho acontecer,
volte ao modo clássico em **Ajustes → Área de trabalho** e conte para a equipe,
com o diagnóstico que aparece ali.
O Roteiro e os monitores de Prévia e Programa também abrem numa janela
separada, só leitura (para um segundo monitor; nunca por cima de uma saída):
**Janela → Destacar**; fechar a janela devolve o painel ao Ao Vivo.

O **Editor de Apresentações** permite criar slides com texto, imagens, formas,
fundos e vídeos dentro de caixas (sem som, repetindo), guardá-los na Biblioteca
e usá-los nos cultos; as mudanças feitas num culto podem voltar para a Biblioteca.
Apresentações do PowerPoint, Keynote e LibreOffice (.pptx, .ppsx, .ppt, .pps,
.key e .odp) viram slides editáveis; .ppt, .pps, .key e .odp são convertidos
antes pelo PowerPoint, Keynote ou LibreOffice instalado no computador. Slides
com gráficos ou tabelas ficam como imagem, com os textos disponíveis para edição.

A troca de slides no Telão faz dissolve suave (ou corte seco, se preferir); o
operador escolhe a duração, de 150 ms a 1 s, em Live › Saídas. O Palco nunca anima.

A Bíblia inclui 18 edições em 12 idiomas: português, inglês, espanhol,
italiano (Nuova Riveduta 1994 e 2006), dinamarquês, crioulo haitiano, francês,
alemão, neerlandês, sueco, bengali e tcheco. Os textos funcionam offline,
com atribuições e numeração próprias de cada edição.

Este repositório publica **somente os instaladores e o feed de atualização
automática**. O código-fonte é mantido em repositório privado do ministério.

## Baixar

| Plataforma | Situação | Download |
|---|---|---|
| macOS 11+ (Apple Silicon e Intel) | Disponível (versão de teste) | [Bethlehem-Presenter_universal.dmg](https://github.com/wsgutnik/bethlehem-presenter-releases/releases/latest/download/Bethlehem-Presenter_universal.dmg) |
| Windows 11 (x64) | Instalador de teste (atualização automática a partir da 0.27.1) | [Releases](https://github.com/wsgutnik/bethlehem-presenter-releases/releases/latest) (arquivo `Bethlehem-Presenter_x64-setup.exe`) |

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
3. A partir da 0.27.1 o app também se atualiza sozinho no Windows (aviso
   “Install & restart”, nunca durante um culto ao vivo); a primeira
   atualização ainda está em validação, então confira em Releases se
   precisar. As estatísticas de uso funcionam como no Mac (Ajustes →
   Estatísticas de uso).

## Novidades da v0.28.1

Desempenho no Diagnóstico: mostra a memória do Mac, travadas do programa, engasgos de vídeo e quais vídeos são pesados demais (acima de 1080p ou 30 Mbps). O monitor Programa fica mais leve em Macs com pouca memória ou com vídeos acima de 1080p: mostra uma imagem do vídeo e a saída continua tocando normalmente. Miniaturas de vídeo da biblioteca só carregam quando aparecem na tela. Esta versão substitui a 0.27.7 (numeração corrigida) e contém tudo da 0.28.0.

## Sobre este build

Gerado automaticamente pelo GitHub Actions a partir do código-fonte privado. Esta
versão só é publicada aqui depois que a compilação termina sem erro.

| | |
|---|---|
| Versão | 0.28.1 |
| Publicado em | 2026-10-12 02:29 UTC |
| Commit do código-fonte | `e91ec81` |
| Execução | Package macOS #104 (https://github.com/wsgutnik/bethlehem-presenter/actions/runs/38195773568, acesso restrito à equipe) |
| Compilado em | macOS 26.6.2, binário universal (arm64 + x86_64) |
| Tamanho do .dmg | 77.3 MB |
| SHA-256 do .dmg | `be2929e955d5b3b93c46047bf5f74fdbae17b49a5efe579aff840b8bc314d7fa` |

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
  O Companion dos participantes também vem desligado: compartilha com
  celulares na rede da igreja o que está no telão (letras do louvor,
  versículos e slides de texto). Versículos aparecem na Bíblia instalada no
  idioma do celular, sem IA; sem Bíblia nesse idioma, viram tradução
  automática marcada. Se configurado, envia essas letras e textos ao Ollama
  no próprio computador para tradução. A captura
  opcional do púlpito envia áudio a um Whisper local e traduz o texto com
  Ollama; exige modelos instalados e validação da configuração no culto.
  Só trechos com fala são enviados: silêncio, ruído e o louvor no ar
  (as letras já vêm dos slides) ficam de fora.
  Por padrão tudo isso fica no próprio computador. Somente se o operador
  ligar e informar a própria chave, o áudio do púlpito pode ser enviado ao
  OpenRouter (transcrição; tradução de fala, letras e textos, se ligada) e o
  texto traduzido à ElevenLabs (voz); a chave
  fica no cofre do sistema e nunca vai no QR ou no link. No celular, ouvir a
  tradução é opcional, começa desligado e usa fones. O operador pode mostrar
  e tirar do telão um QR do Companion (botão em Live › Saídas); ele só
  aparece com o Companion ativo na rede e some com a tela preta. Na aba Telão
  do celular, o versículo no ar aparece na Bíblia do idioma da pessoa.
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
