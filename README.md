# Namecheap DDNS Client

Small and uncomplicated snap to use Namecheap dynamic DNS services.
You just need to configure three attributes:
    $ snap set ncddns password=${PASSWORD}
    $ snap set ncddns domain=${FQDN}
    $ snap set ncddns host=${HOST}

You can also do this in one step as shown in the example below:

    $ snap set ncddns domain=example.com host=@ password=mypassword

If everything is setup correctly, you can see that every five minutes,
the IP address is updated. In case of any complications, just checkout the logs:

    $ sudo journalctl -fu snap.ncddns.ncddns

*Note*: This project initially forked [`duckdns-kyrofa`](https://github.com/kyrofa/duckdns).
