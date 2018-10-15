---
title: Crear una lista de distribución
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 19b282a3b3e756814aa2add07cda4be7609206ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407138"
---
# <a name="create-a-distribution-list"></a><span data-ttu-id="b9589-102">Crear una lista de distribución</span><span class="sxs-lookup"><span data-stu-id="b9589-102">Create a distribution list</span></span>

<span data-ttu-id="b9589-103">En este ejemplo se muestra cómo crear una lista de distribución y mostrarla al usuario.</span><span class="sxs-lookup"><span data-stu-id="b9589-103">This example shows how to create a distribution list and display it to the user.</span></span>

## <a name="example"></a><span data-ttu-id="b9589-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9589-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b9589-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="b9589-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="b9589-106">En el ejemplo de código siguiente, CreateDistributionList crea una lista de distribución llamando al método [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) para crear un objeto [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b9589-106">In the following code example, CreateDistributionList creates a distribution list by calling the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method to create a [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="b9589-107">A continuación, crea un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) y llama al método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) para buscar todos los contactos de la carpeta de contactos predeterminada para los cuales el valor de la propiedad [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) sea “Top Customer” y el valor de la propiedad [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) no esté vacío.</span><span class="sxs-lookup"><span data-stu-id="b9589-107">Next it creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and calls the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) method to find all contacts in the default Contacts folder for which the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property value is “Top Customer” and the [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) property value is not empty.</span></span> <span data-ttu-id="b9589-108">Una vez que se identifiquen todos los contactos, el nombre **Email1Address** se agrega como columna al objeto **Table**.</span><span class="sxs-lookup"><span data-stu-id="b9589-108">Once all contacts are identified, the **Email1Address** name is added as a column to the **Table**.</span></span> <span data-ttu-id="b9589-109">Después, CreateDistributionList crea un objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) mediante el método [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b9589-109">CreateDistributionList then creates a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method from the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="b9589-110">Por último, CreateDistributionList muestra la lista de distribución "Top Customers" al usuario.</span><span class="sxs-lookup"><span data-stu-id="b9589-110">CreateDistributionList finally displays the “Top Customers” distribution list to the user.</span></span>

> [!NOTE] 
> <span data-ttu-id="b9589-111">Debe pasar un objeto **Recipient** resuelto como parámetro del método [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) del objeto [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b9589-111">You must pass a resolved **Recipient** object as a parameter to the [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) method of the [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="b9589-112">Para resolver un objeto **Recipient**, use el método [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="b9589-112">To resolve a **Recipient** object, use the [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) method.</span></span>

<span data-ttu-id="b9589-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b9589-113">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="b9589-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="b9589-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b9589-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="b9589-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b9589-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9589-116">See also</span></span>

- [<span data-ttu-id="b9589-117">Usuarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="b9589-117">exchange users</span></span>](exchange-users.md)

