FROM mcr.microsoft.com/dotnet/sdk:5.0.103-alpine3.12 AS build-env
WORKDIR /app
COPY Review.Web/*.csproj ./
RUN dotnet restore 
COPY . ./
RUN dotnet publish ./Review.sln -c Release -o out

FROM mcr.microsoft.com/dotnet/aspnet:5.0-alpine3.12
WORKDIR /app
COPY --from=build-env /app/out .
EXPOSE 8282
ENTRYPOINT [ "dotnet", "Review.Web.dll" ]