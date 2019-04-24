---
title: Buscar una frase en el cuerpo de los elementos de una carpeta
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc8e0fb2b82ae9660e292a6ec1dea70e82fe36ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316033"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a>Buscar una frase en el cuerpo de los elementos de una carpeta

En este ejemplo se busca la cadena "office" en la sección Cuerpo de todos los elementos de la Bandeja de entrada.

## <a name="example"></a>Ejemplo

En este ejemplo de código se usa una sintaxis de DASL (DAV Searching and Locating) para especificar una consulta. Para crear el filtro, el código de ejemplo comprueba primero si la Búsqueda instantánea está habilitada en el almacén predeterminado, para determinar si se usa la palabra clave **ci\_phrasematch** para una coincidencia de la frase exacta "office" en el cuerpo del elemento, o la palabra clave **like** para cualquier coincidencia de "office" como una cadena exacta o una subcadena en el cuerpo del elemento. El ejemplo luego aplica el filtro del método [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) en la Bandeja de entrada y obtiene los resultados de un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). En el ejemplo de código se muestra el asunto de cada uno de los elementos devueltos en **Table**.

En el código de ejemplo se especifica la propiedad **Body** usando la representación del espacio de nombres urn:schemas:httpmail:textdescription.

La sintaxis para utilizar la palabra clave **ci\_phrasematch** es:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

La sintaxis para utilizar la palabra clave **like** para la coincidencia de prefijo es:

`<PropertySchemaName> like <Token>%`

La sintaxis para utilizar la palabra clave **like** para la coincidencia de subcadena es:

`<PropertySchemaName> like %<Token>%`

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

