Install all depedencies: 
```
npm install
```

Start JS application:
```
node controller.js
```

Install pm2(node service orchestrator) as standalone 
```
sudo npm install -g pm2
```

Start JS application as service using pm2:
```
pm2 start -n "My task name" /path/to/node/script
```

List pm2 services:
```
pm2 list
```

Restart pm2 service:
```
pm2 restart <id of process>
```

Remove pm2 service:
```
pm2 delete <id of process>
```
