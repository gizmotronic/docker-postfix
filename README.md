# What would I use this for?

A typical intranet environment includes applications and servers that send mail using SMTP. Some use cases, e.g. authentication or restricted senders enforced by a service provider, require specialized and sometimes complex configuration. This image allows you to centralize that configuration.

# Quick start

At minimum you should provide a persistent storage volume to hold your Postfix configuration. In this example, we'll keep it in /srv/postfix/config:

```
docker run --name postfix -d \
    -p 25:25/tcp \
    -v /srv/postfix/config:/etc/postfix \
    gizmotronic/postfix
```

Currently, you are responsible for populating this with the appropriate configuration.
