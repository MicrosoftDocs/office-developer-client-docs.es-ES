---
title: Usar la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335374"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a><span data-ttu-id="ca2fd-102">Usar la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto</span><span class="sxs-lookup"><span data-stu-id="ca2fd-102">Use instant search to search all folders and all stores for a phrase in the subject</span></span>

<span data-ttu-id="ca2fd-103">En este ejemplo se usa la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto y, a continuación, mostrar los elementos en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-103">This example uses Instant Search to search all folders and all stores for a phrase in the subject, and then displays the items in an explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="ca2fd-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca2fd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ca2fd-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="ca2fd-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ca2fd-106">La Búsqueda instantánea es una característica de Microsoft Outlook que permite hacer búsquedas mediante la emisión de consultas que devuelven resultados en función del contenido.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-106">Instant Search is a feature of Microsoft Outlook that enables you to search by issuing queries that return results based on the content.</span></span> <span data-ttu-id="ca2fd-107">Después de que se haya procesado la consulta, los resultados se pueden devolver en varios objetos, como el objeto [Tabla](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), la colección [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) y el objeto [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ca2fd-107">Once your query has been processed, the results can be returned in a variety of objects, including the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection, and the [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="ca2fd-108">Puede escribir código que usa la Búsqueda instantánea mediante la Sintaxis de consulta avanzada (AQS) que ofrece Microsoft Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-108">You can write code that uses Instant Search by using the Advanced Query Syntax (AQS) that is offered by Microsoft Windows Desktop Search.</span></span> <span data-ttu-id="ca2fd-109">AQS es uno de los tres lenguajes de consulta que admite Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-109">AQS is one of three query languages that Outlook supports.</span></span> <span data-ttu-id="ca2fd-110">Es eficaz, pero se limita al método [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) del objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ca2fd-110">It is powerful, but limited to the [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="ca2fd-111">No puede usar AQS para imponer una restricción para objetos **Table** o **Item**.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-111">You cannot use AQS to provide a restriction for **Table** or **Item** objects.</span></span> <span data-ttu-id="ca2fd-112">Además, los resultados devueltos por una consulta de AQS solo pueden mostrarse en la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-112">In addition, the results returned by an AQS query can be displayed only in the Outlook user interface.</span></span> <span data-ttu-id="ca2fd-113">La siguiente tabla enumera los tres lenguajes de consulta que admite Outlook, aunque en este tema solo se muestra el uso de AQS.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-113">The following table lists the three query languages that Outlook supports; however, this topic will illustrate the use of only AQS.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca2fd-114">Lenguaje de consulta</span><span class="sxs-lookup"><span data-stu-id="ca2fd-114">Query language</span></span></p></th>
<th><p><span data-ttu-id="ca2fd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca2fd-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca2fd-116">AQS</span><span class="sxs-lookup"><span data-stu-id="ca2fd-116">AQS</span></span></p></td>
<td><p><span data-ttu-id="ca2fd-117">Windows Desktop Search usa AQS y es el lenguaje de consulta para la característica Búsqueda instantánea en Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-117">AQS is used by Windows Desktop Search and is the query language for the Instant Search feature in Outlook.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca2fd-118">DASL</span><span class="sxs-lookup"><span data-stu-id="ca2fd-118">DASL</span></span></p></td>
<td><p><span data-ttu-id="ca2fd-p102">El lenguaje de consulta búsqueda y ubicación DAV (DASL) se basa en la implementación de este lenguaje por parte de Microsoft Exchange en Outlook. DASL puede utilizarse para devolver resultados en el objeto <b>Table</b>. </span><span class="sxs-lookup"><span data-stu-id="ca2fd-p102">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook. DASL can be used to return results in the <b>Table</b> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca2fd-121">Jet</span><span class="sxs-lookup"><span data-stu-id="ca2fd-121">Jet</span></span></p></td>
<td><p><span data-ttu-id="ca2fd-p103">El lenguaje de consulta Jet proporciona un lenguaje de consulta simple para Outlook y se basa en el Servicio de expresiones de Microsoft Jet. Jet se usa para crear cadenas de filtro para los métodos <b>Restrict</b> de la colección <b>Items</b> y el objeto <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-p103">Jet query language provides a simple query language for Outlook, and is based on the Microsoft Jet Expression Service. Jet is used to create filter strings for the <b>Restrict</b> methods of the <b>Items</b> collection and the <b>Table</b> object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca2fd-124">En el ejemplo de código siguiente, DemoInstantSearch devuelve todas las carpetas de correo de todos los almacenes en los que está habilitada la indexación mediante la propiedad [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) del objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ca2fd-124">In the following code example, DemoInstantSearch gets all mail folders in all stores where indexing is enabled by using the [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) property of the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="ca2fd-125">Después usa el método **Search** del objeto **Explorer** para filtrar todos los elementos que contienen la frase exacta "Office 2007" en el asunto y que se han recibido el mes pasado.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-125">It then uses the **Search** method of the **Explorer** object to filter for all items that contain the exact phrase “Office 2007” in the subject and that have been received in the last month.</span></span> <span data-ttu-id="ca2fd-126">Por último, los resultados de la búsqueda se muestran en una ventana independiente del explorador.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-126">The results of the search are finally displayed in a separate explorer window.</span></span>

<span data-ttu-id="ca2fd-127">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ca2fd-128">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ca2fd-129">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="ca2fd-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="ca2fd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca2fd-130">See also</span></span>

- <span data-ttu-id="ca2fd-131">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="ca2fd-131">[Search and filter](search-and-filter.md)</span></span>

