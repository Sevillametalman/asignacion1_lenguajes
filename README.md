## Instrucciones de Ejecución

Siguiendo las instrucciones mencionadas en el PDF, adicionalmente se agregó lo siguiente a los tokens por comodidad:

```
llaveizquierda { "{" }
llavederecha { "}" }
corcheteizquierdo { "[" }
corchetederecho { "]" }
dospuntos { ":" }
coma { "," }
```

Y en `package.json` la instrucción:

```json
"build": "lezer-generator src/json.grammar -o dist/index.js"
```

en la sección de scripts.

### Ejecución:
0.  CREAR LA CARPETA dist EN LA RAIZ DEL PROYECTO (accidentalmente la borré y no hay más tiempo jej)
1.  Ejecutar en la terminal la instrucción `npm install`.
    * **NOTA**: Es probable que automáticamente genere los `.js` y `.cjs` de la prueba en la carpeta `dist`. De ser así, podría obviar el paso 2.
2.  Asegurarse que el JSON a evaluar (`example.json` **DEBE TENER ESE NOMBRE**) y el archivo `.grammar` a utilizar (`json.grammar` **DEBE TENER ESE NOMBRE**) se encuentren en la carpeta `src`.
3.  Ejecutar la instrucción en la terminal `npm run build` para generar los archivos necesarios en la carpeta `dist`.
4.  Ejecutar en la terminal `node dist/index.js`.
5.  Evaluar la salida.
