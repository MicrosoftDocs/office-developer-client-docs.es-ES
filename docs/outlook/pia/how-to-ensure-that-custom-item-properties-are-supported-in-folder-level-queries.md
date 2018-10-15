---
title: Asegurarse de que las propiedades personalizadas del elemento se admiten en consultas a nivel de carpeta
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 659919de8eeb17e675ed67f3b777f67b04f13b54
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406942"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a><span data-ttu-id="0e16d-102">Asegurarse de que las propiedades personalizadas del elemento se admiten en consultas a nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="0e16d-102">Ensure that custom item properties are supported in folder-level queries</span></span>

<span data-ttu-id="0e16d-103">En este ejemplo se muestra cómo garantizar que al agregar una propiedad personalizada a un tipo de elemento, también se agregará la propiedad a la carpeta, de modo que se pueda consultar esa propiedad personalizada a nivel de carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e16d-103">This example shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

## <a name="example"></a><span data-ttu-id="0e16d-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e16d-104">Example</span></span>

<span data-ttu-id="0e16d-105">En este ejemplo de código se muestra cómo usar el objeto [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) y el objeto [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) para asegurarse de que, al agregar una propiedad personalizada a un tipo de elemento, también se agregará la propiedad a la carpeta de modo que pueda consultarse esa propiedad personalizada a nivel de carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e16d-105">This code sample shows how to use the [T:Microsoft.Office.Interop.Outlook.UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) object and the [T:Microsoft.Office.Interop.Outlook.UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) object to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

<span data-ttu-id="0e16d-106">Cuando use el método [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) en la colección [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) para agregar una propiedad personalizada a un elemento, puede especificar el parámetro *AddToFolderFields* como **true** para agregar la propiedad a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e16d-106">When you use the [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) method on the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection to add a custom property to an item, you can specify the *AddToFolderFields* parameter as **true** to add the property to the folder.</span></span> <span data-ttu-id="0e16d-107">Pero, puede que la propiedad personalizada no se agregue a la carpeta deseada debido a un error del desarrollador o una acción del usuario, como la eliminación de la propiedad personalizada por el Selector de campos de Outlook o el desplazamiento del elemento a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e16d-107">However, the custom property might not get added to the desired folderbecause of developer error or a user action, such as removing the custom property through the Outlook Field Chooser or moving the item to another folder.</span></span> <span data-ttu-id="0e16d-108">Por ello, los métodos [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) y [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) del objeto [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) que usan esa propiedad personalizada producirán un error.</span><span class="sxs-lookup"><span data-stu-id="0e16d-108">Consequently, the [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) method and the [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) object that uses that custom property will fail.</span></span> <span data-ttu-id="0e16d-109">Usando el objeto **UserDefinedProperties**, puede comprobar si existen en la carpeta sus propiedades personalizadas y agregarlas si no existen o si se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="0e16d-109">By using the **UserDefinedProperties** object, you can test whether your custom properties exist in the folder, and add the custom properties if they do not exist or if they have been removed.</span></span>

<span data-ttu-id="0e16d-110">Para conservar una propiedad personalizada representada por un objeto **UserDefinedProperty** en una carpeta, debe guardar la propiedad personalizada con el mismo nombre en el elemento.</span><span class="sxs-lookup"><span data-stu-id="0e16d-110">To persist a custom property represented by a **UserDefinedProperty** object in a folder, you must save the custom property with the same name in the item.</span></span> <span data-ttu-id="0e16d-111">Almacenar un valor en el objeto **UserDefinedProperty** de la carpeta no tiene efecto.</span><span class="sxs-lookup"><span data-stu-id="0e16d-111">Storing a value in the **UserDefinedProperty** object for the folder has no effect.</span></span> <span data-ttu-id="0e16d-112">Debe usar el elemento de la colección **UserProperties** para tener acceso al objeto [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) que desea establecer y, luego, establecer el valor en el objeto **UserProperty**.</span><span class="sxs-lookup"><span data-stu-id="0e16d-112">You must se the item's **UserProperties** collection to access the [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) object that you want to set, and then set the value on the **UserProperty** object.</span></span> <span data-ttu-id="0e16d-113">Asegúrese de llamar al método **Save** en el elemento para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="0e16d-113">Be sure to call the **Save** method on the item to persist your changes.</span></span>

<span data-ttu-id="0e16d-114">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0e16d-114">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="0e16d-115">Las instrucciones **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de Clase pública.</span><span class="sxs-lookup"><span data-stu-id="0e16d-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0e16d-116">Las líneas de código siguientes muestran cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="0e16d-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0e16d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e16d-117">See also</span></span>

- [<span data-ttu-id="0e16d-118">Carpetas</span><span class="sxs-lookup"><span data-stu-id="0e16d-118">Folders</span></span>](folders.md)

