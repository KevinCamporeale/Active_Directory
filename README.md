# Active_Directory
Introduzione Active Directory e installazione e configurazione base guidata


# ACTIVE DIRECTORY

## Cosa sono le Active Directory?

[Active Directory Pro](https://activedirectorypro.com/what-is-active-directory/#lesson1) è un servizio Directory la cui funzione principale è autenticare e autorizzare gli utenti a creare risorse di rete.

- **Autenticazione**: verifica credenziali di un utente (nome utente e password)
- **Autorizzazione**: consentire/negare a un utente di fare modifiche/accedere file o applicazioni


<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/9dc10628-0325-432c-b2aa-8bfbf71de313" />


## Esempio 1 - Autenticazione

Kevin è stato assunto come contabile per Active Directory Pro. L'amministratore IT crea un account (che è univoco) per Kevin. A Kevin vengono forniti nome utente e password in modo che possa accedere alla rete dell'azienda.

1. Kevin accede al suo PC con nome e password forniti.
2. La richiesta va al server Active Directory e verifica le credenziali di Kevin.
3. Active Directory cerca l'account di Kevin e lo verifica.
4. Kevin ora è autenticato nel dominio.

<img width="745" height="328" alt="image" src="https://github.com/user-attachments/assets/87da0af6-49fd-46f8-987c-a26be4a69398" />


## Esempio 2 - Autorizzare l'utente

In questo caso, il server Active Directory autorizzerà l'accesso alle risorse di rete.

1. Kevin accede al suo PC usando nome utente e password e vuole accedere alla sua e-mail, a un file di contratto e al server database del contabile.
2. Le risorse della rete controllano con Active Directory se Kevin è autorizzato all'accesso.
3. Kevin è autorizzato all'accesso.
4. Kevin ora può controllare le email, modificare il file di contratto e lavorare sul database.

   
<img width="745" height="351" alt="image" src="https://github.com/user-attachments/assets/aed25810-d05c-4c81-94d0-669c1f9c8f04" />


## Esempio 3 - Autorizzare o Negare l'accesso a un USER

In questo esempio vediamo un altro utente che ha accesso misto (accesso consentito / negato).

1. Gianfranco si registra sulla rete con il suo username e password, prova ad accedere alle stesse risorse di Kevin (email, file contratto, database).
2. Queste risorse di rete controllano con Active Directory se Gianfranco ha i permessi per accedere alle risorse.
3. Active Directory verifica l'account di Gianfranco (Autenticazione) e controlla quali risorse gli sono accessibili (Autorizzazione).
4. Gianfranco può ora accedere alla mail e al file di contratto, ma non ha i permessi per accedere al database.


<img width="744" height="543" alt="image" src="https://github.com/user-attachments/assets/c6420aac-cba5-43fc-9084-6e50001c3bea" />


## Active Directory Domain Service (AD DS)

AD DS è il componente principale di Active Directory e le sue funzioni si possono riassumere in tre principali:

- **Servizio Directory**: un servizio che fornisce metodi di immagazzinamento dati in modo strutturato per rendere l'accesso e l'amministrazione facile.
- **Servizio Autenticazione**: autentica gli utenti in rete.
- **Servizio Autorizzazione**: consente o nega l'accesso degli utenti alle risorse di rete.

<img width="1020" height="817" alt="image" src="https://github.com/user-attachments/assets/601f2c05-e7de-45f2-a358-cfa61bc970a0" />

## Struttura Gerarchica

La struttura di AD organizza le risorse in modo gerarchico:

- **La Foresta (The Forest)** è il contenitore massimo ed è una collezione di domini AD.
  - Qui i domini condividono lo schema e configurazione della directory e un catalogo generale.
  - Quando installiamo AD e creiamo un dominio, stiamo creando una Foresta (Forest).
  
- **AD ROOT** è una struttura logica che contiene:
  - Una struttura gerarchica per utenti, gruppi, PC e altri oggetti.
  - Servizi di sicurezza (autenticazione e autorizzazione).
  - Polizze applicate a utenti e PC.
  - Un nome DNS che identifica il dominio.
    - Quando logghiamo in un PC che fa parte di un dominio, ci stiamo loggando in un nome di dominio DNS (esempio: ad.activedirectorypro.com).
    - Quando installiamo Active Directory dobbiamo scegliere un dominio da usare; è consigliabile usare un sottodominio di activedirectorypro.com (ad esempio: ad.activedirectorypro.com).
  
- **Domini Figli (Child domain)** sono domini che condividono lo stesso spazio di dominio della AD ROOT (esempio: est.ad.activedirectorypro.com, west.ad.activedirectorypro.com).
  
- **Alberi (Trees)** sono una serie di domini collegati tra di loro; quando aggiungiamo un dominio figlio a un dominio padre, creiamo quello che si chiama Domain Tree.
<img width="692" height="652" alt="image" src="https://github.com/user-attachments/assets/6656795d-d0df-492c-9326-eb33700922e6" />

# Installazione | Configurazione | Note

<img width="904" height="660" alt="image" src="https://github.com/user-attachments/assets/18742250-c02a-4641-b184-5a9d2387e0d9" />
<img width="797" height="577" alt="image" src="https://github.com/user-attachments/assets/c2ad5b16-8350-44fb-9928-9c0bf4516fd6" />
<img width="789" height="581" alt="image" src="https://github.com/user-attachments/assets/b2fd4e6d-04e2-4189-be96-1c79039c52e8" />
<img width="828" height="458" alt="image" src="https://github.com/user-attachments/assets/54c1c27f-6253-4352-924c-c72a982452cc" />
<img width="746" height="532" alt="image" src="https://github.com/user-attachments/assets/0c64e6d4-d6aa-43a4-b1ae-5e96af7f071d" />
<img width="790" height="265" alt="image" src="https://github.com/user-attachments/assets/a4324a0d-6d8a-408c-86dd-5aec842717e9" />
<img width="753" height="533" alt="image" src="https://github.com/user-attachments/assets/72ce1794-7e7e-4213-a8b9-0457c8920f66" />
<img width="915" height="681" alt="image" src="https://github.com/user-attachments/assets/0edd3b4b-a8af-4353-9a25-14287d5ec775" />
<img width="550" height="283" alt="image" src="https://github.com/user-attachments/assets/57e0853b-2980-4a11-a72f-9e87bf0703d7" />
<img width="595" height="498" alt="image" src="https://github.com/user-attachments/assets/9b751b0c-9f9e-4328-87ff-d03eea1afc08" />
<img width="645" height="299" alt="image" src="https://github.com/user-attachments/assets/edb9637c-72a8-400f-affb-a7c28d05deff" />
<img width="585" height="403" alt="image" src="https://github.com/user-attachments/assets/c39a4186-ab97-4fd4-acbe-c665844cb1af" />





