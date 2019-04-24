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
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a>Usar la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto

En este ejemplo se usa la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto y, a continuación, mostrar los elementos en una ventana del explorador.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

La Búsqueda instantánea es una característica de Microsoft Outlook que permite hacer búsquedas mediante la emisión de consultas que devuelven resultados en función del contenido. Después de que se haya procesado la consulta, los resultados se pueden devolver en varios objetos, como el objeto [Tabla](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), la colección [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) y el objeto [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Puede escribir código que usa la Búsqueda instantánea mediante la Sintaxis de consulta avanzada (AQS) que ofrece Microsoft Windows Desktop Search. AQS es uno de los tres lenguajes de consulta que admite Outlook. Es eficaz, pero se limita al método [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) del objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)). No puede usar AQS para imponer una restricción para objetos **Table** o **Item**. Además, los resultados devueltos por una consulta de AQS solo pueden mostrarse en la interfaz de usuario de Outlook. La siguiente tabla enumera los tres lenguajes de consulta que admite Outlook, aunque en este tema solo se muestra el uso de AQS.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Lenguaje de consulta</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AQS</p></td>
<td><p>Windows Desktop Search usa AQS y es el lenguaje de consulta para la característica Búsqueda instantánea en Outlook.</p></td>
</tr>
<tr class="even">
<td><p>DASL</p></td>
<td><p>El lenguaje de consulta búsqueda y ubicación DAV (DASL) se basa en la implementación de este lenguaje por parte de Microsoft Exchange en Outlook. DASL puede utilizarse para devolver resultados en el objeto <b>Table</b>. </p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>El lenguaje de consulta Jet proporciona un lenguaje de consulta simple para Outlook y se basa en el Servicio de expresiones de Microsoft Jet. Jet se usa para crear cadenas de filtro para los métodos <b>Restrict</b> de la colección <b>Items</b> y el objeto <b>Table</b>.</p></td>
</tr>
</tbody>
</table>


En el ejemplo de código siguiente, DemoInstantSearch devuelve todas las carpetas de correo de todos los almacenes en los que está habilitada la indexación mediante la propiedad [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) del objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)). Después usa el método **Search** del objeto **Explorer** para filtrar todos los elementos que contienen la frase exacta "Office 2007" en el asunto y que se han recibido el mes pasado. Por último, los resultados de la búsqueda se muestran en una ventana independiente del explorador.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

