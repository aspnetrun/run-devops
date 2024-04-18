#See https://aka.ms/customizecontainer to learn how to customize your debug container and how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
ARG BUILD_CONFIGURATION=Release
WORKDIR /src
COPY ["Shopping.Client/Shopping.Client.csproj", "Shopping.Client/"]
RUN dotnet restore "./Shopping.Client/Shopping.Client.csproj"
COPY . .
WORKDIR "/src/Shopping.Client"
RUN dotnet build "./Shopping.Client.csproj" -c $BUILD_CONFIGURATION -o /app/build

FROM build AS publish
ARG BUILD_CONFIGURATION=Release
RUN dotnet publish "./Shopping.Client.csproj" -c $BUILD_CONFIGURATION -o /app/publish
#RUN dotnet publish "./Shopping.Client.csproj" -c $BUILD_CONFIGURATION -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Shopping.Client.dll"]