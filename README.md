pmmc-pte-pai-patchset
=====================

Introdução
----------

Esta é uma coleção de patches (correções) para o PAI 2.12.2, cujo objetivo principal é fazê-lo funcionar corretamente em servidores Linux, resolvendo basicamente dois tipos de problemas:

1. Divergências na caixa (maiúsculas/minúsculas) dos nomes de arquivos referenciados nas páginas HTML.
2. Divergências na codificação de letras acentuadas (ISO-8859-1 ou UTF-8).

Esta coleção adota as seguintes convenções para corrigir as devergências:

1. Todos os arquivos e diretórios serão renomeados para letras **minúsculas**, exceto na parte do código da atividade (exemplo: `0102POR001`).
2. Todas as ocorrências de letras acentuadas e outros símbolos serão convertidas para entidades HTML (exemplo: todas as ocorrências de `á`, `%E1`, `&#225;` ou `&#x00E1;` serão substituídas por `&aacute;`).

Modo de usar
------------

Para utilizar estes recursos, siga o procedimento abaixo:

1. Instale o Git (em distribuições derivadas do Ubuntu, execute `sudo apt-get install git-core`).
2. Copie este repositório com o comando `git clone git://github.com/oiteam/pmmc-pte-pai-patchset.git`. Substitua `git://` por `https://` em caso de dificuldade de acesso.
3. Vá para o diretório recém-copiado: `cd pmmc-pte-pai-patchset`.
4. Execute o script para renomear os arquivos do PAI (exemplo: `sudo ./pai-rename-files.sh /usr/share/PTE-PMMC/pai`). Um novo diretório `pai.fixed` será criado.
5. **[OPCIONAL]** Se desejar recriar os patches, execute o script apropriado (exemplo: `sudo ./pai-generate-patches.sh /usr/share/PTE-PMMC/pai.fixed`).
6. Aplique os patches, executando o script apropriado (exemplo: `sudo ./pai-apply-patches.sh /usr/share/PTE-PMMC/pai.fixed`).
7. Substitua o diretório `pai` pelo `pai.fixed` (exemplo: `cd /usr/share/PTE-PMMC && sudo rm -rf pai && sudo mv pai.fixed pai`).

Sumário da última geração de patches para a versão 2.12.2.1 (09/11/2012)
----------------------------------------------------------------------

* 2015 arquivos lidos.
* 149 patches gerados para corrigir a caixa das letras dos nomes de arquivos.
* 1892 patches gerados para substituir a codificação de acentos UTF-8.
* 1455 patches gerados para substituir a codificação de acentos ISO-8859-1.

Sumário da última geração de patches para a versão 2.12.2 (02/10/2012)
----------------------------------------------------------------------

* 2015 arquivos lidos.
* 149 patches gerados para corrigir a caixa das letras dos nomes de arquivos.
* 1892 patches gerados para substituir a codificação de acentos UTF-8.
* 1456 patches gerados para substituir a codificação de acentos ISO-8859-1.
* **Observação:** o script de geração de patches foi corrigido nesta data para incluir arquivos do tipo `1234ABC56789.html`, que eram indevidamente desconsiderados nas gerações anteriores.

Sumário da última geração de patches para a versão 2.12.1 (22/06/2012)
----------------------------------------------------------------------

* 1996 arquivos lidos.
* 147 patches gerados para corrigir a caixa das letras dos nomes de arquivos.
* 1891 patches gerados para substituir a codificação de acentos UTF-8.
* 1433 patches gerados para substituir a codificação de acentos ISO-8859-1.

Sumário da última geração de patches para a versão 2.11.2 (01/06/2012)
----------------------------------------------------------------------

* 1990 arquivos lidos.
* 151 patches gerados para corrigir a caixa das letras dos nomes de arquivos.
* 1885 patches gerados para substituir a codificação de acentos UTF-8.
* 1430 patches gerados para substituir a codificação de acentos ISO-8859-1.
