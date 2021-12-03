# Class Cookie

<p>Cria um cookie, uma pequena quantidade de informação enviada por um servlet a um navegador da Web, salva pelo navegador e posteriormente enviada de volta ao servidor. 
O valor de um cookie pode identificar exclusivamente um cliente, portanto, os cookies são comumente usados para gerenciamento de sessão.</p>
<p>Um cookie possui um nome, um único valor e atributos opcionais, como um comentário, caminho e qualificadores de domínio, uma idade máxima e um número de versão. 
Alguns navegadores da Web apresentam erros em como manipulam os atributos opcionais, portanto, use-os com moderação para melhorar a interoperabilidade de seus servlets.</p>

<p>O servlet envia cookies para o navegador usando o HttpServletResponse.addCookie(javax.servlet.http.Cookie)método, que adiciona campos aos cabeçalhos de resposta HTTP para
enviar cookies para o navegador, um por vez. Espera-se que o navegador suporte 20 cookies para cada servidor Web, 300 cookies no total, e pode limitar o tamanho dos cookies
a 4 KB cada.</p>

<p>O navegador retorna cookies para o servlet adicionando campos aos cabeçalhos de solicitação HTTP. Os cookies podem ser recuperados de uma solicitação usando o 
HttpServletRequest.getCookies()método. Vários cookies podem ter o mesmo nome, mas atributos de caminho diferentes.</p>

<p>Os cookies afetam o armazenamento em cache das páginas da Web que os utilizam. O HTTP 1.0 não armazena em cache as páginas que usam cookies criados com esta classe.
Esta classe não oferece suporte ao controle de cache definido com HTTP 1.1.</p>

<p>Esta classe suporta as especificações de cookies da Versão 0 (por Netscape) e Versão 1 (por RFC 2109). Por padrão, os cookies são criados usando a versão 0 
para garantir a melhor interoperabilidade.</p>


<table class="memberSummary" border="0" cellpadding="3" cellspacing="0" summary="Method Summary table, listing methods, and an explanation">
<caption><span id="t0" class="activeTableTab"><span><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"></font></font></span><span class="tabEnd">&nbsp;</span></span><span id="t2" class="tableTab"><span><a href="javascript:show(2);"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"></a></span><span class="tabEnd">&nbsp;</span></span><span id="t4" class="tableTab"><span><a href="javascript:show(8);"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"></font></font></a></span><span class="tabEnd">&nbsp;</span></span></caption>
<tbody><tr>
<th class="colFirst" scope="col"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Modificador e tipo</font></font></th>
<th class="colLast" scope="col"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Método e Descrição</font></font></th>
</tr>
<tr id="i0" class="altColor">
<td class="colFirst"><code><a href="http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html?is-external=true" title="class or interface in java.lang">Object</a></code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#clone--">clone</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Substitui o </font></font><code>java.lang.Object.clone</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> 
 método </font><font style="vertical-align: inherit;">padrão </font><font style="vertical-align: inherit;">para retornar uma cópia deste Cookie.</font></font></div>
</td>
</tr>
<tr id="i1" class="rowColor">
<td class="colFirst"><code><a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a></code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getComment--">getComment</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Retorna o comentário que descreve a finalidade deste cookie, ou
  </font></font><code>null</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">se o cookie não tiver comentários.</font></font></div>
</td>
</tr>
<tr id="i2" class="altColor">
<td class="colFirst"><code><a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a></code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getDomain--">getDomain</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Obtém o nome de domínio deste Cookie.</font></font></div>
</td>
</tr>
<tr id="i3" class="rowColor">
<td class="colFirst"><code>int</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getMaxAge--">getMaxAge</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Obtém a idade máxima em segundos deste Cookie.</font></font></div>
</td>
</tr>
<tr id="i4" class="altColor">
<td class="colFirst"><code><a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a></code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getName--">getName</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Retorna o nome do cookie.</font></font></div>
</td>
</tr>
<tr id="i5" class="rowColor">
<td class="colFirst"><code><a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a></code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getPath--">getPath</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Retorna o caminho no servidor para o qual o navegador retorna este cookie.</font></font></div>
</td>
</tr>
<tr id="i6" class="altColor">
<td class="colFirst"><code>boolean</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getSecure--">getSecure</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Retorna </font></font><code>true</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">se o navegador está enviando cookies apenas por um protocolo seguro ou </font></font><code>false</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">se o navegador pode enviar cookies usando qualquer protocolo.</font></font></div>
</td>
</tr>
<tr id="i7" class="rowColor">
<td class="colFirst"><code><a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a></code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getValue--">getValue</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Obtém o valor atual deste Cookie.</font></font></div>
</td>
</tr>
<tr id="i8" class="altColor">
<td class="colFirst"><code>int</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#getVersion--">getVersion</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Retorna a versão do protocolo com o qual este cookie está em conformidade.</font></font></div>
</td>
</tr>
<tr id="i9" class="rowColor">
<td class="colFirst"><code>boolean</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#isHttpOnly--">isHttpOnly</a></span>()</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Verifica se este Cookie foi marcado como </font></font><i><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">HttpOnly</font></font></i><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> .</font></font></div>
</td>
</tr>
<tr id="i10" class="altColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setComment-java.lang.String-">setComment</a></span>(<a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a>&nbsp;purpose)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Especifica um comentário que descreve a finalidade de um cookie.</font></font></div>
</td>
</tr>
<tr id="i11" class="rowColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setDomain-java.lang.String-">setDomain</a></span>(<a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a>&nbsp;domain)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Especifica o domínio no qual este cookie deve ser apresentado.</font></font></div>
</td>
</tr>
<tr id="i12" class="altColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setHttpOnly-boolean-">setHttpOnly</a></span>(boolean&nbsp;isHttpOnly)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Marca ou desmarca este Cookie como </font></font><i><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">HttpOnly</font></font></i><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> .</font></font></div>
</td>
</tr>
<tr id="i13" class="rowColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setMaxAge-int-">setMaxAge</a></span>(int&nbsp;expiry)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Define a idade máxima em segundos para este Cookie.</font></font></div>
</td>
</tr>
<tr id="i14" class="altColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setPath-java.lang.String-">setPath</a></span>(<a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a>&nbsp;uri)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Especifica um caminho para o cookie ao qual o cliente deve retornar o cookie.</font></font></div>
</td>
</tr>
<tr id="i15" class="rowColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setSecure-boolean-">setSecure</a></span>(boolean&nbsp;flag)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Indica ao navegador se o cookie deve ser enviado apenas por meio de um protocolo seguro, como HTTPS ou SSL.</font></font></div>
</td>
</tr>
<tr id="i16" class="altColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setValue-java.lang.String-">setValue</a></span>(<a href="http://docs.oracle.com/javase/7/docs/api/java/lang/String.html?is-external=true" title="class or interface in java.lang">String</a>&nbsp;newValue)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Atribui um novo valor a este Cookie.</font></font></div>
</td>
</tr>
<tr id="i17" class="rowColor">
<td class="colFirst"><code>void</code></td>
<td class="colLast"><code><span class="memberNameLink"><a href="../../../javax/servlet/http/Cookie.html#setVersion-int-">setVersion</a></span>(int&nbsp;v)</code>
<div class="block"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Define a versão do protocolo de cookie com o qual este Cookie está em conformidade.</font></font></div>
</td>
</tr>
</tbody></table>
