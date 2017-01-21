# Build the image:
# docker build -t helloaspnet:nanoserver .

# Create and run a container:
# docker run -d -p 80:5000 --name helloaspnet tonysneed/helloaspnet:1.1.0-sdk-projectjson

# Get image IP address (Windows container)
# docker inspect -f "{{ .NetworkSettings.Networks.nat.IPAddress }}" helloaspnet

# Browse to app
# http://172.27.236.169

# Alternate between Windows and Linux images
# FROM microsoft/dotnet:1.1.0-sdk-projectjson
FROM microsoft/dotnet:1.1.0-sdk-projectjson-nanoserver

COPY . /app

WORKDIR /app

RUN ["dotnet", "restore"]

EXPOSE 5000

ENTRYPOINT ["dotnet", "run", "--server.urls", "http://*:5000"]
