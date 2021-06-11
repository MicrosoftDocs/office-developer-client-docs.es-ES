---
title: Agregar o eliminar un almacén
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4346f3bf1b7bba1f26a34e1562997b4d043c8d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359748"
---
# <a name="add-or-remove-a-store"></a><span data-ttu-id="3743e-102">Agregar o eliminar un almacén</span><span class="sxs-lookup"><span data-stu-id="3743e-102">Add or remove a store</span></span>

<span data-ttu-id="3743e-103">En este ejemplo se muestra cómo agregar y eliminar un almacén en un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="3743e-103">This example shows how to add and remove a store in a given profile.</span></span>

## <a name="example"></a><span data-ttu-id="3743e-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3743e-104">Example</span></span>

<span data-ttu-id="3743e-105">En este ejemplo de código se muestra cómo agregar y eliminar un almacén en un perfil especificado mediante una llamada al método [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) y al método [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)), respectivamente, en el objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3743e-105">This code sample shows how to add and remove a store in a specified profile, by calling the [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) method and the [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) method respectively on the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="3743e-106">En Outlook, solo se puede agregar o quitar un almacén de archivos PST mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3743e-106">In Outlook, you can add or remove a PST store only programmatically.</span></span> <span data-ttu-id="3743e-107">En el siguiente ejemplo de código se agrega un almacén Unicode y se coloca el archivo .pst en la ubicación predeterminada para los archivos .pst de usuario: Documents and Settings\\\<UserName\>\\Configuración local\\Datos de programa \\Microsoft\\Outlook.</span><span class="sxs-lookup"><span data-stu-id="3743e-107">The following code sample adds a Unicode store and places the .pst file in the default location for user .pst files: Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook.</span></span> <span data-ttu-id="3743e-108">En el código de ejemplo se usa Environment.SpecialFolder.LocalApplicationData para recuperar la ruta de acceso a la carpeta Datos de aplicación en la carpeta Configuración Local.</span><span class="sxs-lookup"><span data-stu-id="3743e-108">The code sample uses Environment.SpecialFolder.LocalApplicationData to retrieve the path to the Application Data folder under the Local Settings folder.</span></span> <span data-ttu-id="3743e-109">Una vez que se ha agregado el almacén, el código de ejemplo elimina el almacén.</span><span class="sxs-lookup"><span data-stu-id="3743e-109">Once the store has been added, the code sample removes the store.</span></span> <span data-ttu-id="3743e-110">Como el método **RemoveStore** requiere un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) para eliminar el objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), enumera la colección [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para encontrar el objeto **Store** que se acaba de agregar basándose en la propiedad [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) del objeto **Store**.</span><span class="sxs-lookup"><span data-stu-id="3743e-110">Because the **RemoveStore** method requires a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to remove the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, it enumerates the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to find the **Store** object that has just been added based on the [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) property of the **Store** object.</span></span>

<span data-ttu-id="3743e-p102">**RemoveStore** solo elimina el almacén del perfil actual. No elimina el archivo .pst del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="3743e-p102">**RemoveStore** only removes the store from the current profile. It does not delete the .pst file from the file system.</span></span>

<span data-ttu-id="3743e-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3743e-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3743e-114">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="3743e-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3743e-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="3743e-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3743e-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3743e-116">See also</span></span>

- [<span data-ttu-id="3743e-117">Almacenes</span><span class="sxs-lookup"><span data-stu-id="3743e-117">Stores</span></span>](stores.md)

