---
title: Buscar una frase exacta en los archivos adjuntos de los elementos de una carpeta
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3d14da44731810308d57ba0e70f9651f3105aad0
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773718"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="80e43-102">Buscar una frase exacta en los archivos adjuntos de los elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="80e43-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="80e43-103">Este ejemplo busca la cadena de búsqueda exacta "office" en los datos adjuntos de los elementos de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="80e43-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="80e43-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80e43-104">Example</span></span>

<span data-ttu-id="80e43-105">En este ejemplo de código se usa una sintaxis de DAV Searching and Locating (DASL) para especificar una consulta.</span><span class="sxs-lookup"><span data-stu-id="80e43-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="80e43-106">Para crear el filtro, el código de ejemplo comprueba primero si la Búsqueda instantánea está habilitada en el almacén predeterminado para determinar si se utiliza la palabra clave **ci\_phrasematch** para obtener una coincidencia de una frase exacta "office" en los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="80e43-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="80e43-107">El ejemplo luego aplica el filtro del método [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) en la Bandeja de entrada y obtiene los resultados de un objeto [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="80e43-107">The sample then applies the filter to the [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) method on the Inbox and obtains the results in a [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia) object.</span></span> <span data-ttu-id="80e43-108">En el ejemplo de código se muestra el asunto de cada uno de los elementos devueltos en **Table**.</span><span class="sxs-lookup"><span data-stu-id="80e43-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="80e43-109">Especifica el código de ejemplo de la propiedad **Attachments** de un elemento mediante la representación del espacio de nombres, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span><span class="sxs-lookup"><span data-stu-id="80e43-109">The code sample specifies the **Attachments** property of an item using the namespace representation, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="80e43-110">La sintaxis para utilizar la palabra clave **ci\_phrasematch** es:</span><span class="sxs-lookup"><span data-stu-id="80e43-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="80e43-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="80e43-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="80e43-112">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="80e43-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="80e43-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="80e43-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```


```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="80e43-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="80e43-114">See also</span></span>

- <span data-ttu-id="80e43-115">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="80e43-115">[Search and filter](search-and-filter.md)</span></span>

