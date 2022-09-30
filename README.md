# ec2-node-d

npm i

node app.js


### Simple script for deploy in EC2

```
#!/bin/bash
apt-get update
apt-get install -y nodejs npm
git clone git@github.com:ctiry01/ec2-node-d.git
"$HOME/application"
cd "$HOME/application" || exit 0
git checkout 99c6efa
npm install

cat <<EOT > /etc/rc.local
#!/bin/bash
cd "$HOME/application"
nodejs app.js &
exit 0
EOT

nodejs app.js &
```

