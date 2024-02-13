# FamilyDocBackend
START SPRING BOOT
mvn spring-boot:run

START POSTGRES DB AS CONTAINER
docker run --name ds-lab-pg --rm -e POSTGRES_PASSWORD=pass123 -e POSTGRES_USER=postgres -e POSTGRES_DB=family
doc -d -p 5432:5432 -v ds-lab-vol:/var/lib/postgresql/data postgres
