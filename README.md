# RailsCasts Episode #357: Adding SSL (pro)

http://railscasts.com/episodes/357-adding-ssl

Requires Ruby 1.9.2 or higher.


### Commands used in rails console

```
curl get.pow.cx | sh
cd ~/.pow
ln -s ~/code/todo .
brew install nginx
cd /usr/local/etc/nginx
openssl req -new -nodes -keyout server.key -out server.csr
openssl x509 -req -days 365 -in server.csr -signkey server.key -out server.crt
mate nginx.conf
mate ~/.powconfig
launchctl stop cx.pow.powd
ENABLE_HTTPS=yes rake middleware
touch tmp/restart.txt
cat example.com.crt example.com-intermediate.crt > example.com-chain.crt
chmod 400 *.key *.crt
sudo chown root *.key *.crt
```
