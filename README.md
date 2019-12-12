# Snipe-IT

Snipe-IT was made for IT asset management, to enable IT departments to track who has which laptop, when it was purchased, which software licenses and accessories are available, and so on.

## Security Caution

docker-compose.yml is for secure network. (etc. in VPN)
Therefore, don't use insecure network like global network.

## Install

1. Replace `<<>>` in docker-compose.yml and env, and run below command.
  Not need to replace `<<APP KEY>>` of env in this time.

    ```
    $ docker-compose up -d
    ```

1. Enter Snipe-IT app container by below command.

    ```
    $ docker exec -i -t snipe-it-app bash
    ```

1. Generate app key by below command in container.

    ```
    # php artisan key:generate
    ```

1. Go out container by below comamnd, and note app key `base64:...=`.

    ```
    # exit
    ```

1. Replace `<<APP KEY>>` of env.

1. Restart Snipe-IT

    ```
    $ docker-compose restart
    ```

## Backup

Save `<<YOUR DIRECTORY PATH>>` of volumes, docker-compose.yml and env.

## Restore

1. Deploy `<<YOUR DIRECTORY PATH>>`.
1. Run `$ docker-compose up -d`.
