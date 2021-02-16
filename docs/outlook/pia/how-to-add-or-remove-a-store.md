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
# <a name="add-or-remove-a-store"></a>Agregar o eliminar un almacén

En este ejemplo se muestra cómo agregar y eliminar un almacén en un perfil determinado.

## <a name="example"></a>Ejemplo

En este ejemplo de código se muestra cómo agregar y eliminar un almacén en un perfil especificado mediante una llamada al método [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) y al método [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)), respectivamente, en el objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).

En Outlook, solo se puede agregar o quitar un almacén de archivos PST mediante programación. En el siguiente ejemplo de código se agrega un almacén Unicode y se coloca el archivo .pst en la ubicación predeterminada para los archivos .pst de usuario: Documents and Settings\\\<UserName\>\\Configuración local\\Datos de programa \\Microsoft\\Outlook. En el código de ejemplo se usa Environment.SpecialFolder.LocalApplicationData para recuperar la ruta de acceso a la carpeta Datos de aplicación en la carpeta Configuración Local. Una vez que se ha agregado el almacén, el código de ejemplo elimina el almacén. Como el método **RemoveStore** requiere un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) para eliminar el objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), enumera la colección [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para encontrar el objeto **Store** que se acaba de agregar basándose en la propiedad [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) del objeto **Store**.

**RemoveStore** solo elimina el almacén del perfil actual. No elimina el archivo .pst del sistema de archivos.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

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

## <a name="see-also"></a>Vea también

- [Almacenes](stores.md)

