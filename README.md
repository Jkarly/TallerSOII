# Proyecto de Automatización de Servidores con Ansible

Este proyecto utiliza **Ansible** para automatizar la configuración y gestión de servidores, permitiendo una administración eficiente y reproducible de la infraestructura.
---
### Requisitos

Para utilizar este proyecto, asegúrate de tener lo siguiente:

* **Ansible** instalado en el nodo de control.
* **Conectividad SSH** configurada con los servidores remotos.
* **Acceso sudo** sin contraseña o con contraseña en los servidores destino.
---
### Uso

Sigue estos pasos para ejecutar los playbooks:

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/Jkarly/TallerSOII.git](https://github.com/Jkarly/TallerSOII.git)
    cd TallerSOII
    ```

2.  **Ejecuta el playbook:**
    Utiliza el siguiente comando para ejecutar el playbook con permisos de superusuario:
    ```bash
    ansible-playbook -i inventory.ini playbook.yml --become --ask-become-pass
    ```
    * `-i inventory.ini`: Especifica el archivo de inventario que contiene la lista de tus servidores.
    * `playbook.yml`: Es el archivo principal del playbook que contiene las tareas a ejecutar.
    * `--become`: Habilita la escalada de privilegios (`sudo`) para ejecutar tareas con permisos de root.
    * `--ask-become-pass`: Solicita la contraseña de sudo, si es necesaria en los servidores remotos.
