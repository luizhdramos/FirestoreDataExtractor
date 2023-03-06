# Firestore Data Extractor

## Português

### Descrição da função FirestoreConnector:

Essa função se chama FirestoreConnector e recebe um parâmetro SDK_Path, que é uma string que representa o caminho para o arquivo do SDK da Firebase.

A função começa importando as bibliotecas necessárias: firebase_admin e credentials.

Em seguida, a função cria um objeto cred que é uma instância da classe Certificate da biblioteca credentials. Esse objeto é inicializado com o caminho do arquivo SDK fornecido como argumento.

Depois disso, a função inicializa o aplicativo Firebase usando o objeto cred com o método initialize_app da biblioteca firebase_admin. O objeto do aplicativo resultante é armazenado em uma variável chamada app.

Finalmente, a função retorna o objeto app, que pode ser usado posteriormente para se conectar a um banco de dados Firestore.

Portanto, essa função cria uma conexão com o Firebase Firestore usando as credenciais fornecidas pelo arquivo SDK e retorna um objeto do aplicativo que pode ser usado para acessar o banco de dados Firestore.


### Descrição da função FirestoreExtractor:

Esta é uma função em Python que extrai dados de uma coleção do Firestore, um banco de dados NoSQL da Google, e os transforma em um DataFrame do Pandas. A função possui três argumentos de entrada, sendo eles:

1. collection_name: nome da coleção que deseja extrair dados.
2. app: instância da aplicação Firebase criada com a autenticação válida para acessar o Firestore.
3. batch_size (opcional, padrão = 4000): número de documentos a serem retornados por iteração.
4. cursor (opcional, padrão = nulo): ponto de partida para a próxima iteração de documentos a serem retornados.

A função começa importando as bibliotecas necessárias, como o Pandas, o firebase_admin e o json. Em seguida, é criada uma conexão com o Firestore usando a biblioteca firebase_admin. Em seguida, uma função auxiliar "iterate" é definida para iterar sobre a coleção e retornar documentos em um tamanho especificado. A função iterate usa um argumento adicional "cursor", que permite iniciar a iteração a partir de um ponto específico.

Em seguida, a função principal FirestoreExtractor cria uma lista de dicionários, onde cada dicionário representa um documento da coleção e contém todos os campos e seus valores. Em seguida, essa lista é convertida em um DataFrame do Pandas e a coluna "id" é definida como índice do DataFrame. Por fim, o DataFrame é retornado como resultado da função.


## English

### Description of the FirestoreConnector function:

This function is called FirestoreConnector and takes a parameter SDK_Path, which is a string representing the path to the Firebase SDK file.

The function starts by importing the necessary libraries: firebase_admin and credentials.

Next, the function creates a cred object, which is an instance of the Certificate class from the credentials library. This object is initialized with the SDK file path provided as an argument.

After that, the function initializes the Firebase app using the cred object with the initialize_app method from the firebase_admin library. The resulting app object is stored in a variable called app.

Finally, the function returns the app object, which can be used later to connect to a Firestore database.

Therefore, this function creates a connection to the Firebase Firestore using the credentials provided by the SDK file and returns an app object that can be used to access the Firestore database.

### Description of the FirestoreExtractor function:

This is a Python function that extracts data from a collection in Firestore, a Google NoSQL database, and transforms it into a Pandas DataFrame. The function has three input arguments, which are:

collection_name: name of the collection to extract data from.
app: instance of the Firebase app created with valid authentication to access Firestore.
batch_size (optional, default = 4000): number of documents to be returned per iteration.
cursor (optional, default = null): starting point for the next iteration of documents to be returned.
The function starts by importing the necessary libraries, such as Pandas, firebase_admin, and json. Next, a connection to Firestore is created using the firebase_admin library. Then, an auxiliary function "iterate" is defined to iterate over the collection and return documents in a specified size. The iterate function uses an additional argument "cursor," which allows starting the iteration from a specific point.

Next, the main function FirestoreExtractor creates a list of dictionaries, where each dictionary represents a document from the collection and contains all fields and their values. Then, this list is converted into a Pandas DataFrame, and the "id" column is set as the index of the DataFrame. Finally, the DataFrame is returned as the result of the function.
