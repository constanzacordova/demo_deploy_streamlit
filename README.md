# coopagua-frontend
repositorio para los scripts de **frontend** del Proyecto de Coopagua


## planilla
planilla para la recolección de datos digital

proxy
```
location /appDatos/ {
        rewrite ^/appDatos/(.*)$ /$1 break; 
        proxy_pass http://0.0.0.0:8102; 
        proxy_redirect http://0.0.0.0:8102/ $scheme://$host/appDatos/; 
        proxy_http_version 1.1; 
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for; 
        proxy_set_header Host $http_host; 
        proxy_set_header Upgrade $http_upgrade; 
        proxy_set_header Connection "upgrade"; 
}
```

### challenge
- [ ] dev un script que lea el diccionario y construya el schema de manera automágica
- [ ] planificar la fase de test para analisis de UX + UI + beneficio para el negocio
- [ ] estructurar el flujo de datos para la fase de test
- [ ] incluir elementos de cálculo de concentración en la sección de Dosificación