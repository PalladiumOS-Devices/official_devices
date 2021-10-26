# Configuring gerrit for Palladium-OS

## Generating SSH Key

```bash
$ cd ~/
$ ssh-keygen
```

After that it will ask for the key location, for default press enter
Then it will ask to add passphrase, for blank pass press enter
[Note: if you want to any pass you can do it, so while pushing commits everytime you need to enter your pass]

## Setting up gerrit account

Open `https://gerrit.palladiumos.com` and Sign-up with your github. After successfull sign-up go to `https://gerrit.palladiumos.com/#/settings/contact` and register your email, and then go to `https://gerrit.palladiumos.com/#/settings`, make sure there every info should be filled up there.

```
1. Username       xxxxxx
2. Full Name      xxxxxx
3. Email Address  xxxxxx@xxxx.com
4. Registered     xxxxx xx:xx
5. Account ID     100xxxx
```

## Adding SSH Key to gerrit

Open your terminal and type: 

```bash
cat .ssh/id_rsa.pub
```

Copy the SSH key and paste it on `https://gerrit.palladiumos.com/#/settings/ssh-keys` and **save it**.


## Checking everything

To check everything is fine, do a connection Test by typing -> `ssh -p 29418 <YourGerritUserName>@mail.palladiumos.com` [Type yes if they ask for it]

```
               Welcome to Gerrit Code Review

Hi <YourGerritUserName>, you have successfully connected over SSH.

Unfortunately, interactive shells are disabled.
To clone a hosted Git repository, use:

git clone ssh://<YourGerritUserName>@mail.palladiumos.com:29418/REPOSITORY_NAME.git

Connection to mail.palladiumos.com closed.
```

[If you get the above output message, your gerrit is configured]
