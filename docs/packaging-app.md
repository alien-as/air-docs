<h1>Packaging App.</h1>

* [](#)
* [](#)
* [Self-Signed Certificate](#)

# Self-Signed Certificate

You can generate a limited certiticate for your app like follows:

```sh
$ adt -certificate -cn SelfSign -ou QE -o "Sample" -c US 2048-RSA <file>.p12 <password>
```

See also [Creating a self-signed certificate with ADT](https://help.adobe.com/en_US/air/build/WS5b3ccc516d4fbf351e63e3d118666ade46-7f74.html).