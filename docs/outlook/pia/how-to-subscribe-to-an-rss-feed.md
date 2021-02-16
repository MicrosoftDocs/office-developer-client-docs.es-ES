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
# <a name="subscribe-to-an-rss-feed"></a><span data-ttu-id="6d065-102">Suscribirse a una fuente RSS</span><span class="sxs-lookup"><span data-stu-id="6d065-102">Subscribe to an RSS feed</span></span>

<span data-ttu-id="6d065-103">En este ejemplo se muestra cómo suscribirse a una fuente RSS mediante el método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6d065-103">This example shows how to subscribe to an RSS feed by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="6d065-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d065-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6d065-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="6d065-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6d065-106">El modelo de objetos de Outlook permite proporcionar acceso a datos compartidos, como calendarios de Internet, fuentes RSS y datos de listas y bibliotecas de documentos de Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6d065-106">The Outlook object model supports providing access to shared data, such as Internet calendars, RSS feeds, and data from Microsoft SharePoint lists and document libraries.</span></span> <span data-ttu-id="6d065-107">Permite conectarse a esos orígenes de datos compartidos y configurar los contextos de sincronización para continuar sondeando esos recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="6d065-107">It enables connecting to these shared sources of data and setting up the synchronization contexts to continue to poll those shared resources.</span></span> <span data-ttu-id="6d065-108">El modelo de objetos de Outlook proporciona el método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para descargar y sincronizar con un tipo concreto de carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="6d065-108">The Outlook object model provides the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to download and synchronize with a particular type of shared folder.</span></span>

<span data-ttu-id="6d065-p102">En el siguiente ejemplo, AddRssFeed se suscribe a una nueva fuente RSS denominada “Example RSS Feed” mediante una llamada al método **OpenSharedFolder** con una dirección URL que hace referencia a la nueva fuente RSS. Los dos últimos parámetros del método **OpenSharedFolder** se establecen en **true** para indicar que deben descargarse datos adjuntos y Outlook debe usar la relación de la actualización proporcionada en la fuente RSS.</span><span class="sxs-lookup"><span data-stu-id="6d065-p102">In the following example, AddRssFeed subscribes to a new RSS feed named “Example RSS Feed” by calling the **OpenSharedFolder** method with a URL that refers to the new RSS feed. The last two parameters of **OpenSharedFolder** method are set to **true** to indicate that attachments should be downloaded, and Outlook should use the refresh ratio provided in the RSS feed.</span></span>


> [!NOTE]
> <span data-ttu-id="6d065-111">Debe especificar el controlador de protocolo correcto para la dirección URL de la carpeta en el método **OpenSharedFolder** para suscribirse a una fuente RSS.</span><span class="sxs-lookup"><span data-stu-id="6d065-111">You must specify the correct protocol handler for the folder URL in the **OpenSharedFolder** method to subscribe to an RSS feed.</span></span> <span data-ttu-id="6d065-112">Por ejemplo, debe usar una dirección URL que comience con `feed://` en lugar de `https://`.</span><span class="sxs-lookup"><span data-stu-id="6d065-112">For example, you must use a URL that begins with `feed://` instead of `https://`.</span></span> <span data-ttu-id="6d065-113">Outlook no puede abrir las fuentes RSS que requieren autenticación a menos que esté disponible la autenticación de LAN Manager de Windows NT (NTLM), y no puede cargar las fuentes RSS desde ubicaciones de Capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="6d065-113">Outlook cannot open RSS feeds that require authentication unless Windows NT LAN Manager (NTLM) authentication is available, and it cannot load RSS feeds from Secure Sockets Layer (SSL) locations.</span></span>

<span data-ttu-id="6d065-114">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6d065-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6d065-115">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="6d065-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6d065-116">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="6d065-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6d065-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d065-117">See also</span></span>

- [<span data-ttu-id="6d065-118">Uso compartido de grupos</span><span class="sxs-lookup"><span data-stu-id="6d065-118">Group sharing</span></span>](group-sharing.md)

