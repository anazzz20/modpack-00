# Jeito fácil: o GitHub compila o mod para você (sem instalar nada)

1. Crie uma conta grátis em https://github.com (se ainda não tiver).
2. Clique em "+" (canto superior direito) > "New repository". Nome: ariel-unit. Deixe "Public" e clique em "Create repository".
3. Na página do repositório, clique em "uploading an existing file".
4. Extraia este zip no computador. Arraste TUDO que está dentro da pasta (a pasta src, os arquivos
   build.gradle, gradle.properties, settings.gradle e a pasta .github) para a página. Espere carregar
   e clique em "Commit changes".
   - Se a pasta .github não subir (no Mac ela fica escondida), veja o "Plano B" abaixo.
5. Clique na aba "Actions". O trabalho "Compilar o mod" começa sozinho (leva uns 3 a 6 minutos).
   Se não começar: clique nele > "Run workflow".
6. Quando ficar com um check verde, abra a execução e, no final da página, em "Artifacts", baixe "ariel-unit-mod".
   Dentro do zip está o arquivo .jar (use o que NÃO termina em -sources).
7. Instale o Fabric Loader para 1.20.1 (https://fabricmc.net/use/installer/) e coloque o Fabric API
   (versão 1.20.1) e o .jar do mod na pasta mods do Minecraft. Abra o jogo no perfil Fabric 1.20.1.

## Se ficar vermelho (erro de compilação)
Abra a execução com o X vermelho > clique em "build" > no passo "Compilar" copie as linhas de erro
(as que começam com "error:") e me mande. Eu corrijo e você sobe só o arquivo corrigido.

## Plano B (se a pasta .github não subiu)
Na aba "Actions", clique em "set up a workflow yourself", apague o texto que aparece, cole o conteúdo do arquivo
.github/workflows/build.yml e clique em "Commit changes".
