# Estágio 1: Build (Usa o SDK completo para compilar o código)
FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /app

# Copia os arquivos de projeto e restaura dependências
COPY *.sln .
COPY src/Vocabulary.Api/*.csproj ./src/Vocabulary.Api/
# (Nota: Copie também os csproj das outras camadas aqui)
RUN dotnet restore ./src/Vocabulary.Api/Vocabulary.Api.csproj

# Copia o resto do código e compila a versão final (Release)
COPY src/ ./src/
WORKDIR /app/src/Vocabulary.Api
RUN dotnet publish -c Release -o /out

# Estágio 2: Runtime (Usa uma imagem muito mais leve só para rodar a API)
FROM mcr.microsoft.com/dotnet/aspnet:9.0 AS runtime
WORKDIR /app
COPY --from=build /out .

# Expõe a porta que a API vai ouvir
EXPOSE 8080
ENTRYPOINT ["dotnet", "Vocabulary.Api.dll"]