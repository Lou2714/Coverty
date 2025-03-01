## Prueba de evalución mediante testing
### Pasos

1. Tener instalado CMake
2. Crear una carpeta build
3. Si es primera vez que se clona, se debe ejecutar comando `cmake -S . -B build` fuera de la carpeta de build, para que se generen los archivos de contrucción de cmake (Ya comprobé, debe ser este comando `cmake -S . -B build`)
   - Si en un dado caso no se cambia al directorio build, pero este ya está creado, se puede ejecutar el comando `cmake -S . -B build`
4. Luego, cambiar de directorio a la carpeta build y ejecutar el comando `cmake --build .` o `cmake ..`
    - Si en un dado caso no se cambia al directorio build, pero este ya está creado, se puede ejecutar el comando `cmake --build build`
5. Al no haber problemas en la construcción, dentro de la carpeta build se ejecuta el comando `ctest` para correr las pruebas
    - Cada vez que se realice una modifición, se debe de volver a ejecutar el comando de construcción `cmake --build .`
6. Para realizar las *pruebas* se puede ejecutar los comandos: `ctest`, en dado caso se encuentre en la carpeta buidl, y `ctest --test-dir build`, sino se encuentra en ella
