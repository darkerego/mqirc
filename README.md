# mqirc
MQTT Shell to IRC Bridge 


This is an irc bridge for mqtt shells. Data is base64 encoded/decoded <br>
so you might want to remove that if you data is not. <br><br>

# Requirements:

- paho-mqtt (pip install paho-mqtt) or pip install -r requirements.txt

# Usage:

- To bridge mqtt traffic on your localhost from topic shell/incoming and to topic shell/outgoing , to an irc server in channel #mqtt:
  python mqirc -s  'shell/outgoing' -t  'shell/incoming' -m localhost -c '#mqtt' -i localhost -I 6667
- To send a message, type "!cmd \<message to send here\>"
- To get usage type "!help'
- To kill the bot, type "!die"

# TODO:

- implement irc tls
- implement mqtt cert auth
- add message encryption support (maybe, might be better to just use mqtt TLS)
- add options to change/specifiy topics while running

<pre>
                                               _..._     
                   .-''-.                    .-'_..._''.  
 __  __   ___     //'` `\|   .--.          .' .'      '.\ 
|  |/  `.'   `.  '/'    '|   |__|         / .'            
|   .-.  .-.   '|'      '|   .--..-,.--. . '              
|  |  |  |  |  |||     /||   |  ||  .-. || |              
|  |  |  |  |  | '. .'/||   |  || |  | || |              
|  |  |  |  |  |  `--'` ||   |  || |  | |. '              
|  |  |  |  |  |        ||   |  || |  '-  \ '.          . 
|__|  |__|  |__|        || />|__|| |       '. `._____.-'/ 
                        ||//     | |         `-.______ /  
                        |'/      |_|                  `   
                        |/
                        
                   ~ MqTT-IRC Bridge ~
                       ShellzRuS 2017

usage: ircmq5.py [-h] [-m MQ_HOST] [-p MQ_PORT] [-u MQ_USER] [-P MQ_PASS]
                 [-s MQ_SUBTOP] [-t MQ_PUBTOP] [-i IRC_HOST] [-I IRC_PORT]
                 [-n IRC_NICK] [-c IRC_CHAN] [-U PRIV_USER] [-d [DEBUG]]
                 [-v [VERBOSE]] [-b [BASE64_ON]]

optional arguments:
  -h, --help            show this help message and exit
  -m MQ_HOST, --mq_host MQ_HOST
                        Mqtt host to connect to
  -p MQ_PORT, --mq_port MQ_PORT
                        Mqtt port to connect to
  -u MQ_USER, --mq_user MQ_USER
                        Mqtt user to auth with
  -P MQ_PASS, --mq_pass MQ_PASS
                        Mqtt password to authenticate with
  -s MQ_SUBTOP, --mq_subtop MQ_SUBTOP
                        Mqtt topic to subscribe to
  -t MQ_PUBTOP, --mq_pubtop MQ_PUBTOP
                        Mqtt topic to publish to
  -i IRC_HOST, --irc_host IRC_HOST
                        Irc host to connect to
  -I IRC_PORT, --irc_port IRC_PORT
                        Irc port to connect to
  -n IRC_NICK, --irc_nick IRC_NICK
                        Nick of irc user
  -c IRC_CHAN, --irc_chan IRC_CHAN
                        Irc channel to join
  -U PRIV_USER, --priv_user PRIV_USER
                        Irc bot owner
  -d [DEBUG], --debug [DEBUG]
                        Print debug messages
  -v [VERBOSE], --verbose [VERBOSE]
                        Verbose mode
  -b [BASE64_ON], --base64_on [BASE64_ON]
                        Base64

</pre>

# License:

Whatever, just credit me.
