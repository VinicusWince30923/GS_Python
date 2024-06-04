<h1>Verificação da Qualidade da Água</h1>

<p>Este repositório contém um script Python para verificar a qualidade da água em várias praias, baseado em quatro parâmetros principais: pH, temperatura, oxigênio dissolvido (OD) e turbidez. O script solicita ao usuário a entrada de valores para esses parâmetros, calcula a média dos valores inseridos, e determina se a qualidade da água está dentro dos padrões recomendáveis.</p>

<h2>Integrantes do grupo</h2>

<ul>
        <li>GUSTAVO JUN IRIZAWA IKEDA (RM554718)</li>
        <li>JÚLIO CÉSAR RUIZ ZEQUIN (RM554676)</li>
        <li>VINICIUS DOS SANTOS WINCE (RM557033)</li>
    <br>
</ul>

<h2>Estrutura do Código</h2>

<p>O código está organizado em funções que lidam com cada parâmetro de qualidade da água e uma função principal que coordena a verificação para múltiplas praias.</p>

<h3>Lista de Funções</h3>

<ul>
    <li><strong>valor_ph()</strong>
        <ul>
            <li>Pede 5 valores de pH ao usuário.</li>
            <li>Calcula a média dos valores.</li>
            <li>Armazena a média na lista <code>lista_media</code>.</li>
            <li>Retorna <code>True</code> se a média estiver entre 7 e 8, caso contrário, retorna <code>False</code>.</li>
        </ul>
    </li>
    <li><strong>valor_temp()</strong>
        <ul>
            <li>Pede 5 valores de temperatura ao usuário.</li>
            <li>Calcula a média dos valores.</li>
            <li>Armazena a média na lista <code>lista_media</code>.</li>
            <li>Retorna <code>True</code> se a média for igual a 25°C, caso contrário, retorna <code>False</code>.</li>
        </ul>
    </li>
    <li><strong>valor_od()</strong>
        <ul>
            <li>Pede 5 valores de oxigênio dissolvido (OD) ao usuário.</li>
            <li>Calcula a média dos valores.</li>
            <li>Armazena a média na lista <code>lista_media</code>.</li>
            <li>Retorna <code>True</code> se a média for maior ou igual a 5 mg/L, caso contrário, retorna <code>False</code>.</li>
        </ul>
    </li>
    <li><strong>valor_turbidez()</strong>
        <ul>
            <li>Pede 5 valores de turbidez ao usuário.</li>
            <li>Calcula a média dos valores.</li>
            <li>Armazena a média na lista <code>lista_media</code>.</li>
            <li>Retorna <code>True</code> se a média for maior que 3 NTU, caso contrário, retorna <code>False</code>.</li>
        </ul>
    </li>
    <li><strong>praias()</strong>
        <ul>
            <li>Pede o nome de 10 praias ao usuário.</li>
            <li>Armazena os nomes na lista <code>lista_praias</code>.</li>
        </ul>
    </li>
    <li><strong>verificação_da_qualidade_da_agua()</strong>
        <ul>
            <li>Pede ao usuário os nomes das praias.</li>
            <li>Para cada praia, solicita os valores de pH, temperatura, OD e turbidez.</li>
            <li>Calcula as médias e verifica se os valores estão dentro dos limites recomendados.</li>
            <li>Imprime o status da qualidade da água e as médias dos parâmetros para cada praia.</li>
        </ul>
    </li>
</ul>

<h2>Requisitos</h2>

<p>Para rodar o código, você precisa ter o Python instalado em sua máquina. Você pode baixar o Python <a href="https://www.python.org/downloads/">aqui</a>.</p>

<h3>Passos para executar o código:</h3>

<ol>
    <li>Certifique-se de ter o Python instalado. A versão recomendada é o Python 3.6 ou superior.</li>
    <li>Baixe o script Python do repositório.</li>
    <li>Abra um terminal (ou prompt de comando) e navegue até o diretório onde o script foi salvo.</li>
    <li>Execute o script com o comando:
        <pre><code>python nome_do_script.py</code></pre>
    </li>
</ol>

<h2>Execução</h2>

<p>Para executar o script, basta rodar a função principal <code>verificação_da_qualidade_da_agua()</code> que coordenará toda a coleta de dados e verificação da qualidade da água.</p>

<h3>Exemplo de Uso</h3>

<ol>
    <li>O usuário será solicitado a inserir o nome de 10 praias.</li>
    <li>Para cada praia, o usuário deve fornecer 5 valores para pH, temperatura, oxigênio dissolvido e turbidez.</li>
    <li>O script calculará a média dos valores fornecidos para cada parâmetro.</li>
    <li>Será verificado se a média de cada parâmetro está dentro dos limites recomendados.</li>
    <li>O script exibirá se a água da praia está em boas condições ou não, junto com os valores médios dos parâmetros medidos.</li>
</ol>

<h3>Limitações</h3>

<ul>
    <li>O script não possui validações de entrada robustas e assume que o usuário fornecerá entradas numéricas válidas.</li>
    <li>Os limites recomendáveis para cada parâmetro são fixos no código e podem precisar de ajustes conforme as normas locais de qualidade da água.</li>
</ul>

<h2>Contribuições</h2>

<p>Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias no código, validações de entrada, ou ajustes nos limites dos parâmetros.</p>

<p>Esperamos que este script seja útil para a verificação da qualidade da água em praias e contribua para a conscientização sobre a importância da preservação da qualidade da água.</p>



</body>
</html>
