---
title: Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bbc87250ab77f662e0fc5a71f9857e734637dd2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702757"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a>Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro

En este ejemplo se usa el método [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) para obtener información sobre todas las listas de distribución de las que el usuario actual es miembro.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En el ejemplo siguiente, GetCurrentUserMembership llama al método **GetMemberOfList** para obtener una colección [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) de todas las listas de distribución de las que el usuario de Exchange es miembro. Si el usuario no es miembro de ninguna lista de distribución, **GetMemberOfList** devuelve una colección **AddressEntries**con un total de cero. El usuario debe estar en línea para que el método **GetMemberOfList** devuelva una colección **AddressEntries**; en caso contrario, **GetMemberOfList** devuelve una referencia nula. GetCurrentUserMembership usa el método [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), que devuelve el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) actual, para comprobar si el usuario está en línea. Una vez que se obtienen las entradas de direcciones, el ejemplo escribe información sobre cada una de las listas de distribución del usuario en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Usuarios de Exchange](exchange-users.md)

