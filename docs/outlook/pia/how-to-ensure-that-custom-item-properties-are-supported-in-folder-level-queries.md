---
title: Asegurarse de que las propiedades personalizadas del elemento se admiten en consultas a nivel de carpeta
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcba2648988d2de3c208079d2845e2cb4c2f549
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722973"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a>Asegurarse de que las propiedades personalizadas del elemento se admiten en consultas a nivel de carpeta

En este ejemplo se muestra cómo garantizar que al agregar una propiedad personalizada a un tipo de elemento, también se agregará la propiedad a la carpeta, de modo que se pueda consultar esa propiedad personalizada a nivel de carpeta.

## <a name="example"></a>Ejemplo

En este ejemplo de código se muestra cómo usar el objeto [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) y el objeto [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) para asegurarse de que, al agregar una propiedad personalizada a un tipo de elemento, también se agregará la propiedad a la carpeta de modo que pueda consultarse esa propiedad personalizada a nivel de carpeta.

Cuando use el método [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) en la colección [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) para agregar una propiedad personalizada a un elemento, puede especificar el parámetro *AddToFolderFields* como **true** para agregar la propiedad a la carpeta. Pero, puede que la propiedad personalizada no se agregue a la carpeta deseada debido a un error del desarrollador o una acción del usuario, como la eliminación de la propiedad personalizada por el Selector de campos de Outlook o el desplazamiento del elemento a otra carpeta. Por ello, los métodos [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) y [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) del objeto [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) que usan esa propiedad personalizada producirán un error. Usando el objeto **UserDefinedProperties**, puede comprobar si existen en la carpeta sus propiedades personalizadas y agregarlas si no existen o si se han eliminado.

Para conservar una propiedad personalizada representada por un objeto **UserDefinedProperty** en una carpeta, debe guardar la propiedad personalizada con el mismo nombre en el elemento. Almacenar un valor en el objeto **UserDefinedProperty** de la carpeta no tiene efecto. Debe usar el elemento de la colección **UserProperties** para tener acceso al objeto [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) que desea establecer y, luego, establecer el valor en el objeto **UserProperty**. Asegúrese de llamar al método **Save** en el elemento para guardar los cambios.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. Las instrucciones **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de Clase pública. Las líneas de código siguientes muestran cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoUserDefinedProperty()
    Dim folder As Outlook.Folder = _
        CType(Application.ActiveExplorer().CurrentFolder(), _
        Outlook.Folder)
    Dim post As Outlook.PostItem = CType( _
        folder.Items.Add("IPM.Post"), Outlook.PostItem)
    ' Add UserProperty to PostItem
    post.UserProperties.Add("ColorID", _
        Outlook.OlUserPropertyType.olText, False)
    post.UserProperties("ColorID").Value = "Green"
    post.Subject = "UserProperty Example"
    post.Save()
    Dim findPost As Outlook.PostItem
    Try
        ' Items.Find will fail unless custom property
        ' is defined in the folder
        findPost = _
            CType(folder.Items.Find("[ColorID] = 'Green'"), _
            Outlook.PostItem)
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
        ' Add ColorID field to the folder
        folder.UserDefinedProperties.Add("ColorID", _
            Outlook.OlUserPropertyType.olText)
        ' Now the find works ok
        Dim findPostOK As Outlook.PostItem
        Try
            findPostOK = _
                CType(folder.Items.Find("[ColorID] = 'Green'"), _
                Outlook.PostItem)
            If Not (findPostOK Is Nothing) Then
                Debug.WriteLine("Found PostItem")
            End If
            ' Cleanup by deleting PostItem and ColorID
            findPostOK.Delete()
            Dim userProperty As Outlook.UserDefinedProperty = _
                folder.UserDefinedProperties("ColorID")
            userProperty.Delete()
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
End Sub
```


```csharp
private void DemoUserDefinedProperty()
{
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.PostItem post = folder.Items.Add("IPM.Post")
        as Outlook.PostItem;
    // Add UserProperty to PostItem
    post.UserProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        false, Type.Missing);
    post.UserProperties["ColorID"].Value = "Green";
    post.Subject = "UserProperty Example";
    post.Save();
    Outlook.PostItem findPost;
    try
    {
        // Items.Find will fail unless custom property
        // is defined in the folder
        findPost =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
     // Add ColorID field to the folder
    folder.UserDefinedProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        Type.Missing, Type.Missing);
    // Now the find works ok
    Outlook.PostItem findPostOK;
    try
    {
        findPostOK =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
        if (findPostOK != null)
        {
            Debug.WriteLine("Found PostItem");
        }
        // Cleanup by deleting PostItem and ColorID
        findPostOK.Delete();
        Outlook.UserDefinedProperty userProperty =
            folder.UserDefinedProperties["ColorID"];
        userProperty.Delete();
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>Vea también

- [Carpetas](folders.md)

