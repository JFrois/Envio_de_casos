<h1>📊 Automação de Consolidação de Dados ITBI (2019–2025)</h1>

<p>Este projeto automatiza o processo de consolidação, filtragem, padronização e envio de dados de transações imobiliárias (ITBI) do município de São Paulo, referentes aos anos de 2019 a 2025. Os dados são coletados a partir de planilhas Excel, tratados com Python no Google Colab e enviados automaticamente para uma aba de API no Google Sheets, evitando duplicações.</p>

<h2>🚀 Funcionalidades</h2>
<ul>
  <li>Leitura de múltiplas abas de um arquivo Excel consolidado (2019–2025)</li>
  <li>Padronização de colunas e tipos de dados</li>
  <li>Filtro de transações por tipo (ex: apenas <strong>"compra"</strong>)</li>
  <li>Remoção de duplicidades com base em <code>matricula_imovel</code> e <code>data_primeira_visita</code></li>
  <li>Envio automático de até <strong>90 novos registros por vez</strong> para o Google Sheets</li>
  <li>Integração com Google Colab e autenticação via Google Auth</li>
</ul>

<h2>📁 Estrutura do Projeto</h2>
<pre><code>📦itbi-automation
 ┣ 📄 ITBI_Consolidado_2019-2025.xlsx
 ┣ 📄 itbi_automation_colab.ipynb
 ┣ 📄 README.html
</code></pre>

<h2>⚙️ Tecnologias Utilizadas</h2>
<ul>
  <li>Python 3.x</li>
  <li>Pandas</li>
  <li>GSpread</li>
  <li>Google Colab</li>
  <li>Google Sheets API</li>
</ul>

<h2>📌 Pré-requisitos</h2>
<ul>
  <li>Conta Google com acesso à planilha <code>API</code></li>
  <li>Planilha com aba chamada <code>Base</code> (ou altere no código conforme necessidade)</li>
  <li>Arquivo Excel <code>ITBI_Consolidado_2019-2025.xlsx</code> com abas nomeadas por ano (<code>2019</code>, <code>2020</code>, ..., <code>2025</code>)</li>
</ul>

<h2>📦 Instalação e Execução</h2>
<ol>
  <li>Acesse o <a href="https://colab.research.google.com/" target="_blank">Google Colab</a></li>
  <li>Faça upload do notebook e do arquivo <code>.xlsx</code></li>
  <li>Execute o notebook, autenticando sua conta Google quando solicitado</li>
  <li>O script irá consolidar os dados e enviar novos registros para a aba <code>Base</code> da planilha <code>API</code></li>
</ol>

<h2>🔄 Automatização</h2>
<p>Para executar automaticamente a cada 20 minutos, considere:</p>
<ul>
  <li>Google Colab Pro + Autocolab (extensão)</li>
  <li>GitHub Actions com agendamentos</li>
  <li>Integração via Google Apps Script</li>
</ul>

<h2>🛡️ Validação de Dados</h2>
<ul>
  <li>Linhas com <code>matricula_imovel</code> ou <code>data_primeira_visita</code> nulas são descartadas</li>
  <li>Transações não relacionadas à compra são ignoradas</li>
  <li>Apenas registros únicos (não duplicados) são enviados à planilha</li>
</ul>

<h2>🧑‍💻 Autor</h2>
<p><strong>Juan Frois</strong><br>
Estudante de Engenharia de Software | Analista de Dados em transição de carreira<br>
🔗 <a href="https://www.linkedin.com/in/juanfrois" target="_blank">LinkedIn</a><br>
💻 <a href="https://github.com/jfrois" target="_blank">GitHub</a>
</p>

<hr>

<p>📝 Licença: Este projeto está sob a licença MIT. Veja o arquivo <code>LICENSE</code> para mais detalhes.</p>
