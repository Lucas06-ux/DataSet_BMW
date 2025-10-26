# DataSet_BMW
Repositório que contém o código completo no colab contendo informações de dados dos carros da BMW.
Os dados foram retirados do kaggle, plataforma que contém diversos DataSets. Foi escolhido especificamente sobre BMW por ser um assunto de gosto pessoal, além de conter boas informações para análise de dados.
O arquivo foi inserido no colab através do: 

    !pip install kagglehub -q 
    
que instala as dependencias do kaggle. Logo em seguida, foi feito o import dele atraves do: 

    import kagglehub
# Download latest version of the dataset
    path = kagglehub.dataset_download("ayeshaimran123/bmw-car-data-analysis")

    print("Path to dataset files:", path)


Esse caminho está disponível no proprio DataSet do site: https://www.kaggle.com/datasets/ayeshaimran123/bmw-car-data-analysis/code


Por fim, para carregar o DataSet:


    import os

    if 'path' in locals() and os.path.isdir(path):

    csv_file_path = os.path.join(path, 'bmw.csv')
    
     Verifica se o arquivo CSV existe no caminho esperado
    
    if os.path.exists(csv_file_path):
    
        df_bmw = pd.read_csv(csv_file_path)
        
        print(f"Dataset carregado de: {csv_file_path}")
        
    else:
    
        print(f"Erro: O arquivo 'bmw.csv' não foi encontrado em {path}")
        
        print("Conteúdo do diretório baixado:", os.listdir(path))
        
    else:

    print("Erro: O caminho do dataset baixado não foi encontrado ou não é um diretório.")
    
    print("Certifique-se de que a célula de download do KaggleHub foi executada corretamente.")
    

Feito isso, todo o DataSet está disponível para uso, sendo possivel iniciar as análises e as preparações dos dados!
