FROM busybox
LABEL mainteiner="sebastian"
# creamos la ruta app y nos movemos a ella
WORKDIR /app
# copiamos el fichero a la carpeta app
COPY text.txt .
# los comandos incluimos en entrypoint no se pueden machacar
# los comandos incluidos en cmd se pueden machacar en función de los param que le pases al comando
ENTRYPOINT [ "cat", "text.txt" ]