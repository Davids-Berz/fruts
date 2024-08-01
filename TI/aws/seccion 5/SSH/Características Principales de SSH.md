- **Autenticación**:
    
    - **Claves Públicas y Privadas**: Los usuarios generan un par de claves (pública y privada). La clave pública se almacena en el servidor, y la clave privada se mantiene segura en el cliente. La autenticación se realiza al comparar la clave pública del servidor con la privada del cliente.
    - **Contraseñas**: SSH también soporta la autenticación basada en contraseñas, aunque es menos segura que el uso de claves.
- **Cifrado**:
    
    - SSH cifra todos los datos transmitidos entre el cliente y el servidor, asegurando que la información no pueda ser interceptada o leída por terceros.
- **Integridad**:
    
    - SSH utiliza algoritmos de hashing (como SHA-2) para asegurar que los datos no se modifiquen durante la transmisión.
- **Redirección de Puertos**:
    
    - Permite redirigir puertos del cliente al servidor y viceversa, lo que puede ser utilizado para crear túneles seguros para aplicaciones.
- **Compresión**:
    
    - SSH puede comprimir los datos antes de cifrarlos, mejorando el rendimiento en conexiones lentas.