---
title: Obtener e iniciar sesión en una instancia de Outlook
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462097(v=office.15)
ms:contentKeyID: 55119926
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4445d0665ea5a3d36a5ff7c92b5a46cfe4fffaa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320275"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Obtener e iniciar sesión en una instancia de Outlook

En este tema se muestra cómo obtener un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)), que representa una sesión activa de Microsoft Outlook en caso de que exista en el equipo local, o cómo crear una nueva sesión de Outlook, iniciar sesión con el perfil predeterminado y devolver la sesión de Outlook.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> Helmut Obertanner proporciona los siguientes ejemplos de código. Los conocimientos de Helmut están en Office Developer Tools para Visual Studio y Outlook. 

Los ejemplos de código siguientes contienen el método GetApplicationObject de la clase de muestra, implementado como parte de un proyecto de complemento de Outlook. Cada proyecto agrega una referencia del ensamblado de interoperabilidad primario de Outlook, que se basa en el espacio de nombres [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).

El método GetApplicationObject usa clases en la biblioteca de clases de .NET Framework para comprobar y obtener cualquier proceso de Outlook que se ejecuta en el equipo local. Primero usa el método [GetProcessesByName](https://msdn.microsoft.com/es-ES/library/wbt7d3cy) de la clase [Process](https://msdn.microsoft.com/es-ES/library/ccf1tfx0) en el espacio de nombres [System.Diagnostics](https://msdn.microsoft.com/es-ES/library/15t15zda) para obtener una matriz de componentes de proceso en el equipo local que compartan el nombre del proceso "OUTLOOK". Para comprobar si la matriz contiene al menos un proceso de Outlook, GetApplicationObject usa Microsoft Language Integrated Query (LINQ). La clase [Enumerable](https://msdn.microsoft.com/es-ES/library/bb345746) del espacio de nombres [System.Linq](https://msdn.microsoft.com/es-ES/library/bb336768) proporciona un conjunto de métodos, incluyendo el método [Count](https://msdn.microsoft.com/es-ES/library/bb357758), que implementan la interfaz genérica [IEnumerable\<T\>](https://msdn.microsoft.com/es-ES/library/9eekhta0). Como la clase [Array](https://msdn.microsoft.com/es-ES/library/czz5hkty) implementa la interfaz **IEnumerable(T)**, GetApplicationObject puede aplicar el método **Count** a la matriz devuelta por **GetProcessesByName** para ver si hay un proceso de Outlook en ejecución. Si lo hay, GetApplicationObject usa el método [GetActiveObject](https://msdn.microsoft.com/es-ES/library/xt620x09) de la clase [Marshal](https://msdn.microsoft.com/es-ES/library/asx0thw2) en el espacio de nombres [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) para obtener esa instancia de Outlook y proyecta ese objeto a un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) de Outlook.

Si Outlook no está en ejecución en el equipo local, GetApplicationObject crea una nueva sesión de Outlook, usa el método [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para iniciar sesión con el perfil predeterminado y devuelve la nueva sesión de Outlook.

El siguiente es el ejemplo de código de Visual Basic, seguido por el ejemplo de código de C\#.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>Vea también

- [Sesiones](sessions.md)

