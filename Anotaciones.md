-dp 127.0.0.1:3000:3000Igual que antes. Ejecutar en modo independiente (en segundo plano) y crear una asignación de puertos.
-w /app- establece el "directorio de trabajo" o el directorio actual desde el que se ejecutará el comando
--mount type=bind,src=.,target=/app- enlazar montar el directorio actual desde el host al /appdirectorio en el contenedor
node:24-alpineLa imagen que se usará. Tenga en cuenta que esta es la imagen base de su aplicación, según el Dockerfile.
sh -c "npm install && npm run dev"El comando. Estás iniciando un shell usando sh(alpine no tiene bash) y ejecutando npm installpara instalar paquetes y luego ejecutando npm run devpara iniciar el servidor de desarrollo. Si revisas el package.json, verás que el devscript inicia nodemon.
