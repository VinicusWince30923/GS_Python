<h1>Verificação da Qualidade da Água</h1>

<p>Este repositório contém um script Python para verificar a qualidade da água em várias praias, baseado em quatro parâmetros principais: pH, temperatura, oxigênio dissolvido (OD) e turbidez. O script solicita ao usuário a entrada de valores para esses parâmetros, calcula a média dos valores inseridos, e determina se a qualidade da água está dentro dos padrões recomendáveis.</p>

<h2>Integrantes do grupo</h2>

<ul>
        <li>GUSTAVO JUN IRIZAWA IKEDA (RM554718)</li>
        <li>JÚLIO CÉSAR RUIZ ZEQUIN (RM554676)</li>
        <li>VINICIUS DOS SANTOS WINCE (RM557033)</li>
    <br>
</ul>

<h2>Código do projeto</h2>
<pre>
<code>
        # Lista para armazenar médias dos parâmetros de qualidade da água
lista_media = []

def valor_ph():
    '''Essa função pede 5 valores do pH, tira a média dos mesmos e armazena o resultado em uma lista.
    Caso a média esteja dentro dos valores recomendáveis para o pH, a função retornará True, caso contrário False.'''
    
    ph_lista = []
    for i in range(5):
        ph = float(input(f"Insira o valor de pH {i+1}° valor: "))
        ph_lista.append(ph)
        
    media_ph = sum(ph_lista) / 5
    lista_media.append(media_ph)
    
    if 7 <= media_ph <= 8:
        return True
    else:
        return False

def valor_temp():
    '''Essa função pede 5 valores da temperatura, tira a média dos mesmos e armazena o resultado em uma lista.
    Caso a média esteja dentro dos valores recomendáveis para a temperatura, a função retornará True, caso contrário False.'''
    
    temp_lista = []
    for i in range(5):
        temp = float(input(f"Insira o valor de temperatura {i+1}° valor: "))
        temp_lista.append(temp)
        
    media_temp = sum(temp_lista) / 5
    lista_media.append(media_temp)
    
    if media_temp == 25:
        return True
    else:
        return False
        
def valor_od():
    '''Essa função pede 5 valores do oxigênio dissolvido (OD) em mg/L, tira a média dos mesmos e armazena o resultado em uma lista.
    Caso a média esteja dentro dos valores recomendáveis para o OD, a função retornará True, caso contrário False.'''
    
    od_lista = []
    for i in range(5):
        od = float(input(f"Insira o valor de oxigênio dissolvido (OD) {i+1}° valor: "))
        od_lista.append(od)
        
    media_od = sum(od_lista) / 5
    lista_media.append(media_od)
    
    if media_od >= 5:
        return True
    else:
        return False

def valor_turbidez():
    '''Essa função pede 5 valores de turbidez (clareza da água), tira a média dos mesmos e armazena o resultado em uma lista.
    Caso a média esteja dentro dos valores recomendáveis para a turbidez, a função retornará True, caso contrário False.'''
    
    turbidez_lista = []
    for i in range(5):
        turbidez = float(input(f"Insira o valor de turbidez {i+1}° valor: "))
        turbidez_lista.append(turbidez)
        
    media_turbidez = sum(turbidez_lista) / 5
    lista_media.append(media_turbidez)
    
    if media_turbidez > 3:
        return True
    else:
        return False

''' Lista para armazenar os nomes das praias'''
lista_praias = []

def praias():
    '''Essa função pede o nome de duas praias e armazena os nomes em uma lista.'''
    for k in range(10):
        praia = input(f"Insira o nome da {k+1}° praia: ")
        lista_praias.append(praia)

def verificação_da_qualidade_da_agua():
    '''Essa função define se a água está em boas condições e mostra a média dos valores medidos.'''
    
    print("Insira o nome das praias que deseja ver a qualidade da água.")
    praias()
    
    for i in range(10):
        print(f"\nInsira os valores para a praia {lista_praias[i]}:")
        
        '''Limpa a lista de médias para armazenar novos valores'''
        lista_media.clear()
        
        ''' Coleta e verifica os valores de cada parâmetro'''
        lista_booleana = [valor_ph(), valor_temp(), valor_od(), valor_turbidez()]
        
        ''' Unidades de medida para cada parâmetro'''
        medida_od = "mg/L"
        medida_turbidez = "NTU"
        medida_temp = "°C"
        
        ''' Verificação das condições da água'''
        if False in lista_booleana:
            print(f"\nA água da praia {lista_praias[i]} não está em boas condições.")
        else:
            print(f"\nA água da praia {lista_praias[i]} está em boas condições.")
        
        ''' Exibe os valores médios medidos'''
        print(f"Os valores lidos são - pH: {lista_media[0]}; Temperatura: {lista_media[1]} {medida_temp}; "
            f"Oxigênio dissolvido: {lista_media[2]} {medida_od}; Turbidez: {lista_media[3]} {medida_turbidez}.")

''' Executa a função principal'''
verificação_da_qualidade_da_agua()
</code>
</pre> 
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

<h2>Requisitos</h2>

<p>Para rodar o código, você precisa ter o Python e o Visual Studio Code (VSCode) instalados em sua máquina.</p>

<h3>Instalação do Python</h3>
<p>Você pode baixar o Python <a href="https://www.python.org/downloads/">aqui</a>. A versão recomendada é o Python 3.6 ou superior.</p>

<h3>Instalação do Visual Studio Code</h3>
<p>Você pode baixar o Visual Studio Code <a href="https://code.visualstudio.com/">aqui</a>.</p>

<h2>Execução</h2>

<p>Para executar o script utilizando o Visual Studio Code (VSCode), siga os passos abaixo:</p>

<ol>
    <li>Abra o Visual Studio Code.</li>
    <li>Certifique-se de que a extensão do Python está instalada no VSCode. Caso não esteja, você pode instalá-la a partir da aba de extensões.</li>
    <li>Baixe o script Python do repositório e salve-o em um diretório de sua escolha.</li>
    <li>No VSCode, clique em <strong>File</strong> > <strong>Open Folder</strong> e navegue até o diretório onde o script foi salvo. Abra esse diretório.</li>
    <li>Clique duas vezes no arquivo do script para abri-lo no editor.</li>
    <li>Com o arquivo aberto, clique no botão "Run" no canto superior direito (Símbolo de "Play") ou pressione <code>F5</code> para executar o script.</li>
</ol>

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

</body>
</html>
