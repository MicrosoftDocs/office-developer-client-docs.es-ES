---
title: Obtener e iniciar sesión en una instancia de Outlook
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462097(v=office.15)
ms:contentKeyID: 55119926
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6aa4ecb0b6d9a3082759c7a3b0b4a5f677d1556e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406466"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a><span data-ttu-id="1391f-102">Obtener e iniciar sesión en una instancia de Outlook</span><span class="sxs-lookup"><span data-stu-id="1391f-102">Get and sign in to an instance of Outlook</span></span>

<span data-ttu-id="1391f-103">En este tema se muestra cómo obtener un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)), que representa una sesión activa de Microsoft Outlook en caso de que exista en el equipo local, o cómo crear una nueva sesión de Outlook, iniciar sesión con el perfil predeterminado y devolver la sesión de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1391f-103">This topic shows how to obtain an [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that represents an active instance of Outlook, if there is one running on the local computer, or to create a new instance of Outlook, log on to the default profile, and return that instance of Outlook.</span></span>

## <a name="example"></a><span data-ttu-id="1391f-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1391f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1391f-105">Helmut Obertanner proporciona los siguientes ejemplos de código.</span><span class="sxs-lookup"><span data-stu-id="1391f-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="1391f-106">Los conocimientos de Helmut están en Office Developer Tools para Visual Studio y Outlook.</span><span class="sxs-lookup"><span data-stu-id="1391f-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="1391f-107">Los ejemplos de código siguientes contienen el método GetApplicationObject de la clase de muestra, implementado como parte de un proyecto de complemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1391f-107">The following code examples contain the GetApplicationObject method of the Sample class, implemented as part of an Outlook add-in project. Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the N:Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="1391f-108">Cada proyecto agrega una referencia del ensamblado de interoperabilidad primario de Outlook, que se basa en el espacio de nombres [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1391f-108">The following code examples contain the GetApplicationObject method of the Sample class, implemented as part of an Outlook add-in project. Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [N:Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="1391f-109">El método GetApplicationObject usa clases en la biblioteca de clases de .NET Framework para comprobar y obtener cualquier proceso de Outlook que se ejecuta en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="1391f-109">The GetApplicationObject method uses classes in the .NET Framework class library to check and obtain any Outlook process running on the local computer.</span></span> <span data-ttu-id="1391f-110">Primero usa el método [GetProcessesByName](https://msdn.microsoft.com/es-ES/library/wbt7d3cy) de la clase [Process](https://msdn.microsoft.com/es-ES/library/ccf1tfx0) en el espacio de nombres [System.Diagnostics](https://msdn.microsoft.com/es-ES/library/15t15zda) para obtener una matriz de componentes de proceso en el equipo local que compartan el nombre del proceso "OUTLOOK".</span><span class="sxs-lookup"><span data-stu-id="1391f-110">It first uses the [GetProcessesByName](https://msdn.microsoft.com/es-ES/library/wbt7d3cy) method of the [Process](https://msdn.microsoft.com/es-ES/library/ccf1tfx0) class in the [System.Diagnostics](https://msdn.microsoft.com/es-ES/library/15t15zda) namespace to obtain an array of process components on the local computer that share the process name "OUTLOOK".</span></span> <span data-ttu-id="1391f-111">Para comprobar si la matriz contiene al menos un proceso de Outlook, GetApplicationObject usa Microsoft Language Integrated Query (LINQ).</span><span class="sxs-lookup"><span data-stu-id="1391f-111">To check whether the array does contain at least one Outlook process, GetApplicationObject uses Microsoft Language Integrated Query (LINQ).</span></span> <span data-ttu-id="1391f-112">La clase [Enumerable](https://msdn.microsoft.com/es-ES/library/bb345746) del espacio de nombres [System.Linq](https://msdn.microsoft.com/es-ES/library/bb336768) proporciona un conjunto de métodos, incluyendo el método [Count](https://msdn.microsoft.com/es-ES/library/bb357758), que implementan la interfaz genérica [IEnumerable\<T\>](https://msdn.microsoft.com/es-ES/library/9eekhta0).</span><span class="sxs-lookup"><span data-stu-id="1391f-112">The [Enumerable](https://msdn.microsoft.com/es-ES/library/bb345746) class in the [System.Linq](https://msdn.microsoft.com/es-ES/library/bb336768) namespace provides a set of methods, including the [Count](https://msdn.microsoft.com/es-ES/library/bb357758) method, that implement the [IEnumerable\<T\>](https://msdn.microsoft.com/es-ES/library/9eekhta0) generic interface.</span></span> <span data-ttu-id="1391f-113">Como la clase [Array](https://msdn.microsoft.com/es-ES/library/czz5hkty) implementa la interfaz **IEnumerable(T)**, GetApplicationObject puede aplicar el método **Count** a la matriz devuelta por **GetProcessesByName** para ver si hay un proceso de Outlook en ejecución.</span><span class="sxs-lookup"><span data-stu-id="1391f-113">Because the [Array](https://msdn.microsoft.com/es-ES/library/czz5hkty) class implements the **IEnumerable(T)** interface, GetApplicationObject can apply the **Count** method to the array returned by **GetProcessesByName** to see whether there is an Outlook process running.</span></span> <span data-ttu-id="1391f-114">Si lo hay, GetApplicationObject usa el método [GetActiveObject](https://msdn.microsoft.com/es-ES/library/xt620x09) de la clase [Marshal](https://msdn.microsoft.com/es-ES/library/asx0thw2) en el espacio de nombres [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) para obtener esa instancia de Outlook y proyecta ese objeto a un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1391f-114">If there is, GetApplicationObject uses the [GetActiveObject](https://msdn.microsoft.com/es-ES/library/xt620x09) method of the [Marshal](https://msdn.microsoft.com/es-ES/library/asx0thw2) class in the [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) namespace to obtain that instance of Outlook, and casts that object to an Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

<span data-ttu-id="1391f-115">Si Outlook no está en ejecución en el equipo local, GetApplicationObject crea una nueva sesión de Outlook, usa el método [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para iniciar sesión con el perfil predeterminado y devuelve la nueva sesión de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1391f-115">If Outlook is not running on the local computer, GetApplicationObject creates a new instance of Outlook, uses the  Logon  method of the  NameSpace  object to log on to the default profile, and returns that new instance of Outlook.</span></span>

<span data-ttu-id="1391f-116">El siguiente es el ejemplo de código de Visual Basic, seguido por el ejemplo de código de C\#.</span><span class="sxs-lookup"><span data-stu-id="1391f-116">The following is the Visual Basic code example, followed by the C# code example.</span></span>

<span data-ttu-id="1391f-117">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1391f-117">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="1391f-118">La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="1391f-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1391f-119">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="1391f-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1391f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1391f-120">See also</span></span>

- [<span data-ttu-id="1391f-121">Sesiones</span><span class="sxs-lookup"><span data-stu-id="1391f-121">Sessions</span></span>](sessions.md)

