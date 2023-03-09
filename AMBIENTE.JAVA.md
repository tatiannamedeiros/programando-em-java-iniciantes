## PROGRAMANDO EM JAVA USANDO OPENJDK
#### Primeiros Passos
##### → Linux

*Para começar a sua jornada como programador Java, entenda que o ambiente precisa ser preparado. Veja o Java como um rei que precisa ser devidamente recepcionado…* 👑

*O OpenJDK é um conjunto de ferramentas que possibilitam a criação de programas em java, assim como a execução destes. Mas você pode usar em vez do OpenJDK (código aberto) o Oracle JDK (licenciado). Ambos podem ser usados de forma gratuita, contudo, a última tem a licença da Oracle, o que cria certas regras quanto à utilização e, ainda, permite ter acesso a alguns benefícios como o auxílio da Oracle caso haja problemas relacionados ao JDK. Entenda que não há diferença quanto ao uso, até porque a JDK da Oracle é baseada na OpenJDK, a questão é que para o âmbito empresarial, poder ter a possibilidade de receber assistência da Oracle acarreta em uma maior segurança.*

## CONFIGURANDO O AMBIENTE JAVA
### Preparando o computador para desenvolver programas em java

1. Precisamos descobrir se o java já está instalado em nosso sistema operacional.
<br>Digite no terminal:<br/>

'''java --version'''

*Nesta situação pode aparecer algo do tipo ‘java’ not found (o que significa que você não tem o java instalado aí no seu belo computador) OU pode aparecer a versão instalada na sua máquina (você já tem o java aí bem pertinho de você).*

*Caso a sua versão do java seja mais antiga você pode atualizá-la (eu sugiro que faça isso, mas fica a seu critério). No momento que digito isso a versão mais recente é a 19.*

## ATUALIZAR O OPENJDK (você já tem uma versão mais antiga instalada)
<br>Digite no terminal:<br/>

'sudo apt upgrade openjdk-19-jdk'

*Aqui no exemplo escolhi a versão 19, eu tinha a versão 11.*

## INSTALAR OPENJDK (para quem não tem instalado - nenhuma versão)
<br>Digite no terminal:<br/>

'sudo apt install openjdk-19-jdk'

*O ‘19’ representa a versão que queremos instalar, apenas um exemplo, pode ser outra versão!). Após a instalação ser concluída digite novamente “java --version” para conferir.*

## CONFIGURANDO A VARIÁVEL DE AMBIENTE
<br>São elas as responsáveis pelo bom funcionamento do nosso ambiente de desenvolvimento. Assim como estão diretamente relacionadas a execução de programas em Java.<br/>

*De início precisamos verificar o caminho no qual o JDK foi instalado na máquina.*
<br>Digite no terminal:<br/>

'sudo update-alternatives --config java'

*Agora, vamos editar o arquivo bashrc*
<br>Digite no terminal:<br/>

'sudo gedit ~/.bashrc'

**Importante: caso não tenha os pacotes gedit basta instalar por meio do comando:**

'sudo apt-get install gedit'

*Mais informações sobre pacotes gedit aqui: https://www.thegeekdiary.com/gedit-command-not-found/*

*Um arquivo de texto será aberto de forma automática…*

'JAVA_HOME=usr/lib/jvm/java-19-openjdk-amd64' (verifique se são semelhantes ao caminho mostrado ao digitar '--config java')

'export JAVA_HOME export PATH=$PATH:$JAVA_HOME'

*COLE as estruturas acima na última linha do arquivo que foi aberto, depois clique em SALVAR e FECHE o arquivo de texto. Feche também o terminal após a etapa anterior.*

*Abra o terminal novamente (CTRL+ALT+T). Confirme se as configurações feitas foram salvas digitando no terminal:*

'cat ~/.bashrc'

*O arquivo que foi alterado deve aparecer no terminal, onde as suas últimas linhas devem conter os caminhos que colocamos.*

**Pronto, você já pode se aventurar no mundo dos javeiros** 🙂
______________________________
### Informações extras:

## DESINSTALAR OPENJDK (a título de curiosidade)
<br>Digite no terminal:<br/>

'$sudo apt purge openjdk-19-*'

*Mais informações sobre desinstalar o openjdk aqui:*
https://ciksiti.com/pt/chapters/3354-how-to-uninstall-java-from-ubuntu--linux-hint


## INSTALAÇÃO EM AMBIENTE WINDOWS
<br>No Windows baixe o JDK pelo site da azul.com ➡️ Depois vá em "Editar as variáveis de ambiente do sistema" ➡️ Opção "Avançado" ➡️ Variáveis de Ambiente ➡️ Nova Variável de Sistema ➡️ Nome: JAVA_HOME e Valor da Variável: colar o caminho onde o arquivo jdk está (descompactado) OU ir em Procurar Diretório ➡️ clicar em OK ➡️ configure o Path clicando em Path e depois em Editar ➡️ Novo ➡️ cole de novo o caminho + barra invertida + bin ➡️ Mover para cima (ficar no topo) ➡️ confirme no Prompt de comando se foi instalado ➡️ java --version

Por Tatiana Medeiros
@tatiannamedeiros
