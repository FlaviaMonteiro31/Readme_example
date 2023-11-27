---


---

<h1 id="site-de-compras">Site de compras</h1>
<p>O site de compras foi desenvolvido para permitir a compra de produtos por lojas e parceiros. Este site foi desenvolvido para substituir o antigo site em ASP.</p>
<h2 id="🚀-começando">🚀 Começando</h2>
<p>Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste.</p>
<h3 id="📋pré-requisitos">📋Pré-requisitos</h3>
<p>Para iniciar a manutenção ou desenvolvimento de novas funcionalidades é pré-requisito ter as seguintes ferramentas instaladas:</p>
<ol>
<li>Docker</li>
<li>IntelliJ IDEA</li>
<li>Postman ou Insomnia</li>
<li>JDK 17</li>
</ol>
<h3 id="🔧instalação">🔧Instalação</h3>
<p>Segue os detalhes para criar a imagem do oracle database no docker</p>
<ol>
<li>Baixar as imagem do git<br>
<em>git clone <a href="https://github.com/oracle/docker-images">https://github.com/oracle/docker-images</a></em></li>
<li>Baixar o database 19 versão em linux<br>
<em>LINUX.X64_193000_db_home.zip</em></li>
<li>Extrair os códigos do baixados do git no diretório C</li>
<li>Colocar o zip do batabase 19 na pasta:<br>
<em>C:\docker-images-main\OracleDatabase\SingleInstance\dockerfiles\19.3.0</em></li>
<li>Executar o comando para criar a imagem<br>
<em>./buildContainerImage.sh -v 19.3.0 -e</em></li>
<li>Criar o container, renomear, configurar a porta, usuário e senha<br>
<em>docker run --name oracle19c -p 1521:1521 -p 5500:5500 -e ORACLE_PDB=orcl -e ORACLE_PWD=vivoSdc23 -e ORACLE_MEM=2000 -v /opt/oracle/oradata -d oracle/database:19.3.0-ee</em></li>
<li>Verificar os logs<br>
<em>sudo docker logs -f oracle19c</em></li>
<li>Verificar o listener<br>
<em>sudo docker exec -it oracle19c /bin/bash</em><br>
<em>lsnrctl status</em></li>
<li>Caso seja necessário alterar senha<br>
<em>docker exec oracle19c ./setPassword.sh vivosdc</em><br>
<em>docker exec oracle19c ./runUserScripts.sh</em></li>
</ol>
<h3 id="⚙️executando-os-testes">⚙️Executando os testes</h3>
<p>Explicar como executar os testes automatizados para este sistema.</p>
<h4 id="🔩-analise-os-testes-de-ponta-a-ponta">🔩 Analise os testes de ponta a ponta</h4>
<p>Explique que eles verificam esses testes e porquê.</p>
<pre><code>Dar exemplos

</code></pre>
<h4 id="⌨️-e-testes-de-estilo-de-codificação">⌨️ E testes de estilo de codificação</h4>
<p>Explique que eles verificam esses testes e porquê.</p>
<pre><code>Dar exemplos
</code></pre>
<h3 id="🛠️-construído-com">🛠️ Construído com</h3>
<p>O site de compras foi construído em Java, versão 17, contendo os seguintes frameworks.</p>
<ul>
<li><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/">Spring Boot</a>  - O framework de desenvolvimento</li>
<li><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/">Spring Security</a>  - Recursos de segurança, autenticação e autorização</li>
<li><a href="https://maven.apache.org/">Maven</a>  - Gerenciamento de Dependência</li>
<li><a href="https://projectlombok.org/features/">Lombok</a>  - Usada para redução de código boilerplate</li>
<li><a href="https://docs.spring.io/spring-data/jpa/docs/current-SNAPSHOT/reference/html/#reference">JPA</a>  - Usada para gerenciamento de persistência e mapeamento de objeto e funções</li>
</ul>
<h3 id="📌versão">📌Versão</h3>
<p>Todas as versões existentes  <a href="https://gitlab.redecorp.br/b2c-dev-legados/src/sdc-margarida">neste repositório</a>.</p>
<h3 id="✒️autores">✒️Autores</h3>
<p>Os envolvidos no levantamento e desenvolvimento do site de compras</p>
<ul>
<li><strong>Flávia Alves Monteiro</strong>  -  _Desenvolvedor Back-End</li>
<li><strong>Eduardo Chagas Silva</strong>  -  _Desenvolvedor Back-End</li>
</ul>

