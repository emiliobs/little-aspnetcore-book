# Hola Mundo en C\#
Antes de profundizar en ASP.NET Core, prueba creando y ejecutando una aplicaci�n de C\# simple.

Puedes hacer todo esto desde la l�nea de comandos. Primero, abre una Terminal \(o PowerShell en Windows\). Navega a la ubicaci�n donde deseas guardar tus proyectos, tal c�mo la carpeta de mis Documentos:

```text
cd Documentos
```

Usa el comando `dotnet` para crear un nuevo proyecto:

```text
dotnet new console -o CsharpHelloWorld
```

El comando `dotnet new` crea un nuevo proyecto de .NET con C\# por omisi�n. El par�metro `console` selecciona una plantilla para una aplicaci�n de consola \( un programa que emite texto en la pantalla\).El par�metro `-o CsharpHelloWorld` instruye a `dotnet new` para crear una carpeta llamada `CsharpHelloWorld` para los archivos del proyecto . Cambiate a esta carpeta asi:

```text
cd CsharpHelloWorld
```

`dotnet new console` crea un programa de C\# b�sico que escribe el texto `Hello World!` en la pantalla. El programa esta compuesto por dos archivos: un archivo de proyecto\(con extensi�n `.csproj`) y un archivo de c�digo de C# (con extensi�n`.cs\`\). Si abres el primer archivo en un editor de texto, veras esto :

**CsharpHelloWorld.csproj**

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.0</TargetFramework>
  </PropertyGroup>

</Project>
```

El archivo de proyecto esta baso en XML y define algunos metadatos sobre el proyecto. Despu�s , Cuando referencias otros paquetes, aquellos ser�n listados aqu� \(de forma similar a un un archivo `package.json` para npm\). No necesitar�s editar est� archivo de forma manual muy seguido.

**Program.cs**

```csharp
using System;

namespace CsharpHelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
}
```

El m�todo `static void Main` es el punto de entrada de un programa de C\#, y por convenci�n esta colocado en una clase \(un tipo de c�digo estructura o modulo\) llamado `Program`. El enunciado `using` al inicio importa las clases incluidas en espacio de nombres `System` desde .NET y las hace disponibles en el c�digo en t� clase.

Dentro de la carpeta del proyecto, usa `dotnet run` para ejecutar el programa. Veras que la salida se escribe en la consola despu�s que el c�digo compila:

```text
dotnet run

!Hola Mundo!
```

!Esto es todo lo necesario para crear y ejecutar un programa en .NET! Enseguida, har�s lo mismo para una aplicaci�n ASP.NET Core.
