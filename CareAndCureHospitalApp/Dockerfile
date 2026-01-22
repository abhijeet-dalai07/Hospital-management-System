FROM eclipse-temurin:17-jdk

WORKDIR /app

COPY . .

RUN chmod +x mvnw

RUN ./mvnw clean package

# 🔍 DEBUG: list target directory
RUN ls -l target

RUN mv target/*.jar app.jar

# 🔍 DEBUG: confirm rename
RUN ls -l

EXPOSE 8080

CMD ["java","-jar","app.jar"]
