# Introduction

**GPG COMMAND**
Generate a GPG key pair. Since there are multiple versions of GPG, you many need to consult the relevant man page to find the appropriate key generation command. Your GPG key must use RSA with a key size of 4096 bits.

```
gpg --full-generate-key
```

Use the gpg --list-secret-keys --keyid-format LONG command to list GPG keys for which you have both a public and private key. A private key is required for signing commits or tags.

```
gpg --list-secret-keys --keyid-format LONG
```

From the list of GPG keys, copy the GPG key ID you'd like to use. In this example, the GPG key ID is D569493B606C70EB:

```
Output :
/home/bayudwiyansatria/.gnupg/pubring.kbx
sec   rsa4096/D569493B606C70EB 2019-05-26 [SC]
      D1E8DD7D569493B606C70EB
uid                 [ultimate] Bayu Dwiyan Satria (Bayu Dwiyan Satria) <bayudwiyansatria@gmail.com>
ssb   rsa4096/D1E8DD7 2019-05-26 [E]
```

To set your GPG signing key in Git, paste the text below, substituting in the GPG key ID you'd like to use. In this example, the GPG key ID is D569493B606C70EB:

```
git config --global user.signingkey D569493B606C70EB
```

Export, the GPG key ID is D569493B606C70EB:

```
gpg --armor --export 3AA5C34371567BD2 > ~/gpg.asc
```