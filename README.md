# FirestoreDataExtractor



English:

Function FirestoreConnector: Use this function to connect to Firestore

-(Variables)-

SDK_Path: The Path of the SDK file used to connect to Firestore


Português:

Função FirestoreConnector: Use essa função para se conectar no Firestore

-(Variáveis)-

SDK_Path: O caminho do arquivo SDK usado para se conectar no Firestore





English:

Function FirestoreExtractor: Use this function to extract data from Firestore to a Pandas Dataframe

-(Variables)-

collection_name: The Collection you want to extract 
app: Firestore Connector (Use FirestoreConnector to get this variable)
batch_size: Batch of date you'll load per time from your connection
cursor: The "document number" from query

Português:

Função FirestoreExtractor: Use essa função para extrair dados do Firestore para um Dataframe Pandas

-(Variáveis)-

collection_name: A Collection que você quer extrair
app: Conector do Firestore (Use a função FirestoreConnector para conseguir esta variável)
batch_size: Lote de dados que você vai carregar por vez de sua conexão
cursor: O "número documento atual" da query.
