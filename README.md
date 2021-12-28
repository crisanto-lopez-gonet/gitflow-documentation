## Clonar el repositorio

    git clone git@github.com:MYACCOUNT/MYREPO


## Features
  
#### Crear feature branch a partir de develop:
    ```bash
    git checkout -b feature/MYFEATURE develop
    ```

#### Hacer cambios/commits:
    git add <archivos>
    git commit -m "Cambio"

#### Comprobar que el merge funciona bien con develop:
    git checkout develop
    git pull
    git merge feature/MYFEATURE
    
#### Se deshace el merge en develop:
    git reset --hard <commit_id>
    ó
    git reset --merge <commit_id>

#### Si el merge es OK, se sube la feature al repositorio:
    git checkout feature/MYFEATURE
    git push -u origin feature/MYFEATURE

#### ... se crea el PR en Github
#### Y se espera a que un compañero apruebe el PR  

---
#### Si el merge en develop no es OK ... Se deshace el merge:
    git reset --hard <commit_id>
    ó
    git reset --merge <commit_id>
    
    
    git checkout feature/MYFEATURE

#### Se hacen los cambios para arreglar los conflictos o fallas:
    git add .
    git commit -m "Arreglados conflictos con develop"

#### Se suben los cambios:
    git push -u origin feature/MYFEATURE

#### Y se crea el PR después de comprobar que la integración con develop será OK
