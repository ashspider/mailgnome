# Mail Gnome


## Setup

```bash
sudo apt-get update
sudo apt-get install git python-pip build-essential libssl-dev libpopt-dev
```

## Endpoints
```bash
/diag

/check_email/<email_address>
```

Possible JSON responses
```bash
{'code':0, 'message': 'Unknown Exception'} # for simplicity changed to Unknown
{'code':1, 'message': 'Mail server indicates this is a valid email address'} #changed to Valid 
{'code':2, 'message': 'Mail server found for domain, but the server doesn\'t allow e-mail address verification'} #changed to Catch all
{'code':3, 'message': 'Mail server found for domain, but the email address is not valid'} #changed to Invalid
{'code':4, 'message': 'Mail server not found for domain'}  #changed to Unknown
{'code':5, 'message': 'DNS Lookup Timeout'} #changed to Timeout
{'code':6, 'message': 'Unable to connect to Mail Server'} #changed to Unknown
```

## Notes
Python Version: 2.7

We risk spamming smtp servers with these requests which can lead to getting ourselves added to spam lists.  

## Example Emails

mahto.arvin@gmail.com
potatowithhat@ymail.com - hangs/timesout on connecting to mail server
billgates@hotmail.com - server disconnects client
.
.
