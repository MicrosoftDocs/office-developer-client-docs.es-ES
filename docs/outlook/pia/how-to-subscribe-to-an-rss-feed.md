---
title: Suscribirse a una fuente RSS
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b92c733c5030ce12eb691bba57afb5ce6b9d1dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335402"
---
# <a name="subscribe-to-an-rss-feed"></a>Suscribirse a una fuente RSS

En este ejemplo se muestra cómo suscribirse a una fuente RSS mediante el método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

El modelo de objetos de Outlook permite proporcionar acceso a datos compartidos, como calendarios de Internet, fuentes RSS y datos de listas y bibliotecas de documentos de Microsoft SharePoint. Permite conectarse a esos orígenes de datos compartidos y configurar los contextos de sincronización para continuar sondeando esos recursos compartidos. El modelo de objetos de Outlook proporciona el método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para descargar y sincronizar con un tipo concreto de carpeta compartida.

En el siguiente ejemplo, AddRssFeed se suscribe a una nueva fuente RSS denominada “Example RSS Feed” mediante una llamada al método **OpenSharedFolder** con una dirección URL que hace referencia a la nueva fuente RSS. Los dos últimos parámetros del método **OpenSharedFolder** se establecen en **true** para indicar que deben descargarse datos adjuntos y Outlook debe usar la relación de la actualización proporcionada en la fuente RSS.


> [!NOTE]
> Debe especificar el controlador de protocolo correcto para la dirección URL de la carpeta en el método **OpenSharedFolder** para suscribirse a una fuente RSS. Por ejemplo, debe usar una dirección URL que comience con `feed://` en lugar de `https://`. Outlook no puede abrir las fuentes RSS que requieren autenticación a menos que esté disponible la autenticación de LAN Manager de Windows NT (NTLM), y no puede cargar las fuentes RSS desde ubicaciones de Capa de sockets seguros (SSL).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddRssFeed()
{
    string feedUrl = "feed://example.org/rssfeed.xml";
    Outlook.Folder subscriptionFolder =
        Application.Session.OpenSharedFolder(feedUrl, "Example RSS Feed", true, true) as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(subscriptionFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a>Vea también

- [Uso compartido de grupos](group-sharing.md)

