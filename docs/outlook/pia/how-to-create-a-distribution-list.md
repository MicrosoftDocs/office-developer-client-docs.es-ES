---
title: Crear una lista de distribución
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f37338209ea468d0143dfd1063c3c57216bc13ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359657"
---
# <a name="create-a-distribution-list"></a>Crear una lista de distribución

En este ejemplo se muestra cómo crear una lista de distribución y mostrarla al usuario.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


En el ejemplo de código siguiente, CreateDistributionList crea una lista de distribución llamando al método [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) para crear un objeto [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)). A continuación, crea un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) y llama al método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) para buscar todos los contactos de la carpeta de contactos predeterminada para los cuales el valor de la propiedad [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) sea “Top Customer” y el valor de la propiedad [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) no esté vacío. Una vez que se identifiquen todos los contactos, el nombre **Email1Address** se agrega como columna al objeto **Table**. Después, CreateDistributionList crea un objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) mediante el método [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Por último, CreateDistributionList muestra la lista de distribución "Top Customers" al usuario.

> [!NOTE] 
> Debe pasar un objeto **Recipient** resuelto como parámetro del método [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) del objeto [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)). Para resolver un objeto **Recipient**, use el método [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a>Vea también

- [Exchange users](exchange-users.md) (Usuarios de Exchange)

