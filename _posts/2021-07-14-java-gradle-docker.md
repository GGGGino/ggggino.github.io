Come impostazione base uso docker per evitare di sporcare il computer con dipendenze che non mi servono

Scaricare l'immagine di gradle

Inizializzare il progetto con:

docker run --rm -it -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle gradle init

Il *-it* è importante perchè permette di poter avere una bas interattiva, senza questo non ti fa scegliere opzioni e quindi non inizializza niente.


Per runnare il progetto usare :
docker run --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle gradle run
invece di 
docker run --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle ./gradlew run
Altrimenti scarica tutti i pacchetti e ci vuole tanto

