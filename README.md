# RaidenApp-PoC
1st Vivido Raiden App - 

RaidenApp è un'applicazione il cui scopo è quello di testare il funzionamento (al momento su Ropsten) di [Raiden Network](https://github.com/raiden-network/raiden)

 

# Use Case 1

INVIO DEI TOKEN
L'indirizzo 0xbAe2661E1357aB9f22440AdD9BA0a3A9d6f520C0 che nella fase di test dell'infrastruttura Raiden Network ha generato i token VVDO e VVDO1 (entrambi registrati sul network di Raiden Network) invierà 10.000 token (VVDO o VVDO1 da definire) agli Ethereum address associati ai due smartphone che hanno scaricato la RaidenApp-Poc.

FUNZIONALITA' 
Le funzionalità della RaidenApp-Poc sono:

1) Creazione nuovo account Ethereum. Chiave privata salvata sul dispositivo. in questa prima versione non inseriremo nessun controllo di sicurezza, come seed e/o password.

2) Open Channel on Raiden Network.
   Per fare questa operazione l'idea è quella che dall'interno dell'app i due corrispndenti si scambino un messaggio (via Telegram/Whatsapp?? quindi devono conoscere l'indirizzo dell'istant messenger del corrispondente) che riporta il proprio indirizzo Ethereum.
   All'interno di questa funzione Open Channel copiamo l'indirizzo che abbiamo ricevuto dal nostro corrispondente. 
   Saranno presenti due bottoni:
    OPEN
    CLOSE
   LA prima volta OPEN sarà abilitatoe CLOSE disabilitato.
   Il canale può essere aperto da entrambi.
   Una volta aperto il bottone OPEN sarà disabilitato per entrambi, mentre CLOSE risulterà abilitato per entrambi.
   
 3) DEPOSIT: questa funzione provvedere a prelevare un certo numero dei token presenti nell'Ethereum address ed a depositarli nel canale.
 Questa operazione genera una transazione sulla blockchain Ethereum in OUT per il numero di token depositati.
 Gestire l'errore "Prelievo maggiore dei fondi"
 
 4) PAYMENT: invio di token al corrispondente.
  Gestire l'errore "Pagamento maggiore dei token in deposito"
  
 
 5) VISUALIZZAZIONE INFORMAZIONI:
   Devono essere visualizzate :
   a) Importo del Deposito originario
   b) Saldo al momento
   c) Lista dei pagamenti
 
 
# Risorse

1) [VividoRaidenToken.sol](https://github.com/vividosrl/RaidenApp-PoC/blob/master/VividoRaidenToken.sol) 
Smart Contract con il quale è stato creato il token VVDO (VIVIDO) : qty 100.000.000 ; decimals: 18 

2) [UTC...](https://github.com/vividosrl/RaidenApp-PoC/blob/master/UTC--2018-08-16T08-07-48.536Z--bae2661e1357ab9f22440add9ba0a3a9d6f520c0) 
chiave privata per fare i test

3) [MetaMask Secret Backup Phrase.txt](https://github.com/vividosrl/RaidenApp-PoC/blob/master/MetaMask%20Secret%20Backup%20Phrase.txt)
passphrase per account MetaMask di test --- in verità non so se serve, pechè poi ho creato il tken con il JSON e MyEtherWallet , quindi si potrebbe anche cancellare ---

4) [Smart Contract Address](https://ropsten.etherscan.io/token/0x81f762a313da2eac32f64ac71ecae477c76168c3?a=0xbae2661e1357ab9f22440add9ba0a3a9d6f520c0 )



