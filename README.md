# Configurar o git em uma nova máquina

![alt](https://i.imgur.com/KZWuBHE.jpeg)

### Configurações da conta


```bash
git config --global user.name "name"
git config --global user.email "email@email.com"
```

### Criar chave SSH

```bash
ssh-keygen -t rsa -b 4096 -C "email@email.com"
```

Verificar a dita cuja foi criada
```bash
ls -al ~/.ssh`
```

Adicionar a chave ao *agent*
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

Copiar a saída do seguinte comando
```bash
cat ~/.ssh/id_rsa.pub
```
- Adicionar no **Github** via `Settings > SSH and GPG keys > New SSH key`.


Ver se sua conta esta autenticando corretamente
```bash
ssh -T git@github.com
```







