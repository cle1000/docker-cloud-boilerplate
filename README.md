## 0. REQUIREMENTS

A domain ``{your-domain}`` which points to the IP address of ``{your-domain}``.

## 1. Globally replace
``{your-domain}`` with your domain,

``{your-email}`` with your email address,

``{your-username}`` with your ssh login name at ``{your-domain}`,

``{your-mysql-root-password}`` with a password of your choice,

``{your-mysql-password}`` with a password of your choice.


After renaming push everything to your server, with the following `scp` cmd: ``./push``

## 2. Create the following folder structure on ``{your-domain}``:

``/data/nextcloud/files/``
``/data/nextcloud/database/``
``/data/portainer/``
``/data/traefik/``

## 3. Start containers:

Start traefik (Proxy and load loadbalancer) with ``cd traefik`` and ``docker-compose up -d``

Start portainer (Web App for docker) with ``cd portainer`` and ``docker-compose up -d``
Will be online under https://portainer.{your-domain}

Start nextcloud (Proxy and load loadbalancer) with ``cd nextcloud`` and ``docker-compose up -d``
Will be online under https://nextcloud.{your-domain}

Start website (Static website) with ``cd website`` and ``docker-compose up -d``
Will be online under https://{your-domain}
