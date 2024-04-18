# Custom kubernetes opening

To extend the functionality of k9s on your MacBook to handle custom commands, you can 
create a shell script that interprets the arguments and launches k9s with the appropriate 
Kubernetes context and namespace. This approach allows you to customize your command to 
fit different configurations based on the arguments passed.

* **-c, --context string:** Set the context to be used
* **-n, --namespace string:** Set the namespace to be used

```sh
touch k9s-custom
chmod +x k9s-custom

mv k9s-custom /usr/local/bin
```

Or to make it controlled
```sh
nano ~/.zshrc
export PATH="$PATH:/path/to/script"
source ~/.zshrc
echo $PATH
```
