#Programando em Java - primeiros passos
###Linux - Ubuntu

1. CONFIGURANDO O AMBIENTE JAVA
_Precisamos saber se já temos o Java instalado na máquina pelo terminal:_
java --version

_Se aparecer 'java' not found, então baixar OpenJDK. Basta digitar a seguinte estrutura no terminal:_
sudo apt install openjdk-17-jdk

_Confirme se o download foi feito digitando a seguinte estrutura no terminal:_
java --version (ou basta ir clicando no símbolo da seta para cima até aparecer 'java --version') e pressione "enter"

Deve aparecer a versão instalada, assim como a data de instalação.

2. CONFIGURANDO A VARIÁVEL DE AMBIENTE
_Verificando o caminho no qual o JDK foi instalado na máquina:_
sudo update-alternatives --config java

_Editando o arquivo bashrc:_
sudo gedit ~/.bashrc

_Um arquivo de texto será aberto de forma automática, copie a seguinte estrutura:_
JAVA_HOME=usr/lib/jvm/java-17-openjdk-amd64 (essa primeira parte deve combinar com o caminho que apareceu para você ao digitar '--config java')
export JAVA_HOME
export PATH=$PATH:$JAVA_HOME

_COLE a estrutura acima na última linha do arquivo que foi aberto, depois clique em SALVAR e FECHE o arquivo de texto. Feche também o terminal após a etapa anterior._

_Abra o terminal novamente (CTRL+ALT+T). Confirme se as configurações feitas foram salvas digitando no terminal:_
cat ~/.bashrc

_O arquivo que foi alterado deve aparecer no terminal, onde as suas últimas linhas devem conter os caminhos que colocamos._

_Caso queira, pode confirmar novamente se o Java foi devidamente instalado digitando:_
java --version
