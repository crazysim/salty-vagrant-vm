# Salty-Vagrant-VM

This is an extract of the example vagrant VM found in the salty-vagrant repository.

1. `git clone https://github.com/saltstack/salty-vagrant`
2. `git subtree split --prefix=example -b split`
3. `git remote add github <your repo url>`
4. `git push github split:master`

This does contain a few changes I like though.

* Use the Opscode Chef VM as the box and for the URL. They have the
  infrastrucure and money to make a lean and updated Ubuntu box. It has some
  chef crap but it's inert.

* Run the top state ASAP.

* Provide a sanity check top state that just installs cowsay, an essential tool
  and mission-critical resource for day-to-day operations within any organization.

You must install the salty-vagrant gem:

```sh
vagrant gem install vagrant-salt
```

or, for rubygem users

```sh
gem install vagrant-salt
```
