# Correction bug Symphony sur Nginx

> Après le root sur la config Nginx.
> Corrige le bug Symphony sur Nginx de page qui redirige vers le front à partir du back.

```nginx
location /adminXXXX/ {
    if (!-e $request_filename) {
        rewrite ^/.*$ /adminXXXX/index.php last;
    }
}
```
