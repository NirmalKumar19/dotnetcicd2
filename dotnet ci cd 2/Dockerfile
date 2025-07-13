# Stage 1: Build and publish the app
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src

# Copy the project file and restore dependencies
COPY ["dotnet ci cd 2.csproj", "./"]
RUN dotnet restore "dotnet ci cd 2.csproj"

# Copy the rest of the source code
COPY . .

# Publish the application to /out
RUN dotnet publish "dotnet ci cd 2.csproj" -c Release -o /out
