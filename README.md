# Nervlayer: releases

O Nervlayer é um launcher open source (MIT) para macOS, nativo em Swift, focado em produtividade e IA:
busca de apps e arquivos, calculadora, clipboard, snippets, janelas e chat de IA com chave própria
ou modelos locais, sem telemetria.

Este repositório guarda só os binários de cada versão (DMG e zip) e o feed de atualização do
Sparkle (`appcast.xml`), que o app consulta para se atualizar. Não há código-fonte aqui.

## Baixar

Baixe o DMG da [última release](https://github.com/luizpereiradev/nervlayer-releases/releases/latest).
Requer macOS 26 e Apple Silicon.

1. Confira o arquivo: `shasum -a 256 Nervlayer-<versão>.dmg` deve bater com o `SHA256SUMS` da release.
2. Abra o DMG e arraste o Nervlayer para a pasta Aplicativos.

## Primeira abertura (Gatekeeper)

O app não é notarizado pela Apple, então o macOS bloqueia a primeira abertura:

1. Abra o Nervlayer uma vez. O macOS avisa que não pode verificá-lo: clique em "OK" (não em
   "Mover para o Lixo").
2. Em Ajustes do Sistema → Privacidade e Segurança, role até Segurança e clique em "Abrir Mesmo
   Assim" ao lado do aviso sobre o Nervlayer. Confirme com a sua senha.
3. Na janela seguinte, clique em "Abrir Mesmo Assim" de novo.

Isso só é preciso uma vez. Depois, as atualizações chegam pelo próprio app, verificadas pela
assinatura EdDSA do Sparkle.

Quem tem a 0.1.0 precisa instalar a 0.1.1 à mão, uma vez: a 0.1.0 procura atualizações num endereço
antigo, que não responde mais.
