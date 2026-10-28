# Km e Despesas — projeto Android

Este projeto empacota o aplicativo de Km e Despesas (versão offline) em um APK.
Os dados ficam salvos no próprio aparelho, e o botão "Baixar em Excel" grava a
planilha, no modelo original da Semear, na pasta Downloads do celular.

Requisito do celular: Android 10 ou mais novo.

## Gerar o APK pelo GitHub (sem instalar nada)

1. Crie uma conta gratuita em github.com e clique em **New repository**. Dê um nome
   (por exemplo `km-despesas`) e crie o repositório.
2. No repositório, clique em **Add file > Upload files** e arraste **todo o conteúdo
   desta pasta** (incluindo a pasta oculta `.github`). Clique em **Commit changes**.
   - Se a pasta `.github` não subir, use **Add file > Create new file**, digite o nome
     `.github/workflows/build-apk.yml` e cole o conteúdo do arquivo de mesmo nome.
3. Abra a aba **Actions**. Um fluxo chamado **Gerar APK** começa sozinho e leva uns
   5 minutos. (Se não começar, abra o fluxo e clique em **Run workflow**.)
4. Quando ficar verde, abra a execução e, no final da página, em **Artifacts**,
   baixe **KmDespesas-apk**. Dentro do zip está o `app-debug.apk`.
5. Envie o APK para o celular, abra o arquivo e permita a instalação de fontes
   desconhecidas quando o Android pedir.

## Gerar o APK no Android Studio

Abra esta pasta no Android Studio, aguarde a sincronização e use
**Build > Build APK(s)**. O arquivo sai em `app/build/outputs/apk/debug/`.

## Atualizar o aplicativo depois

O app fica em `app/src/main/assets/index.html`. Para trocar por uma nova versão,
substitua esse arquivo e gere o APK de novo.
