# Docker
## Docker Volumes
- Data persistence
    - Databases
    - Other Stateful Applications

3 Docker volume types
- docker run -v /home/mount/data:/var/lib/mysql/data (Host Volumes)

- docker run -v /var/lib/mysql/data (Anonymous Volumes Automaticaly created by Docker)

- docker run -v name:/var/lib/mysql/data (Named Volumes)