yourlabs.drone
==============

Full one-command documented here, but `traefik_*` variables are not necessary
if you have already executed yourlabs.traefik:

    bigsudo yourlabs.drone github_id="<GhAppId>" github_secret="<GhAppSecret>" url=https://ci.example.com @ci.example.com --become -v traefik_domain=traefik.ci.example.com traefik_acme=prod traefik_email=you@example.com
