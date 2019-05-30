---
title: Obtener la lista global de direcciones o un conjunto de listas de direcciones para un almacén
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 677325df863e5b5a52856abb01f55bdb8884bbe8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542530"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>Obtener la lista global de direcciones o un conjunto de listas de direcciones para un almacén

Este tema contiene dos códigos de ejemplo que muestran cómo obtener la lista global de direcciones (GAL) asociada a un almacén y cómo obtener todas las listas de direcciones asociadas a un almacén.

## <a name="example"></a>Ejemplo

En una sesión de Outlook donde hay varias cuentas de Exchange definidas en el perfil, puede haber varias listas de direcciones asociadas con un almacén. En cada uno de los siguientes ejemplos de código, el almacén específico de interés es el almacén de la carpeta actual que se muestra en el explorador activo, pero el algoritmo para obtener una lista global de direcciones o un conjunto de objetos [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) de un almacén se aplica a cualquier almacén de Exchange.

El primer ejemplo de código contiene el método DisplayGlobalAddressListForStore y la función GetGlobalAddressList. El método DisplayGlobalAddressListForStore muestra, en el cuadro de diálogo **Seleccionar nombres**, la Lista global de direcciones que está asociada con el almacén actual. DisplayGlobalAddressListForStore obtiene primero el almacén actual. Si el almacén actual es un almacén de Exchange, llama a GetGlobalAddressList para obtener la Lista global de direcciones asociada con el almacén actual. 

GetGlobalAddressList usa el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) y la propiedad MAPI http://schemas.microsoft.com/mapi/proptag/0x3D150102 para obtener la propiedad PR\_EMSMDB\_SECTION\_UID de una lista de direcciones y el almacén actual. GetGlobalAddressList identifica una lista de direcciones como asociada con un almacén si sus propiedades PR\_EMSMDB\_SECTION\_UID coinciden, y la lista de direcciones es la lista global de direcciones si su propiedad [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) es [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)). Si la llamada a GetGlobalAddressList es correcta, DisplayGlobalAddressListForStore usa el objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) para mostrar la lista global de direcciones devuelta en el cuadro de diálogo **Seleccionar nombres**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
void DisplayGlobalAddressListForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    if (currentStore.ExchangeStoreType !=
        Outlook.OlExchangeStoreType.olNotExchange)
    {
        Outlook.SelectNamesDialog snd = 
            Application.Session.GetSelectNamesDialog();
        Outlook.AddressList addrList = 
            GetGlobalAddressList(currentStore);
        if (addrList != null)
        {
            snd.InitialAddressList = addrList;
            snd.Display();
        }
    }
}

public Outlook.AddressList GetGlobalAddressList(Outlook.Store store)
{
    string  PR_EMSMDB_SECTION_UID = 
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList 
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList = 
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID && addrList.AddressListType ==
            Outlook.OlAddressListType.olExchangeGlobalAddressList)
        {
            return addrList;
        }
    }
    return null;
}
```

El segundo ejemplo de código contiene el método EnumerateAddressListsForStore y la función GetAddressLists. El método EnumerateAddressListsForStore muestra el tipo y el orden de resolución de cada lista de direcciones definida para el almacén actual. EnumerateAddressListsForStore primero obtiene el almacén actual y luego llama a GetAddressLists para obtener un objeto [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19) de .NET Framework genérico que contenga objetos AddressList para el almacén actual. 

GetAddressLists enumera cada lista de direcciones definida para la sesión, usa el objeto PropertyAccessor y la propiedad con nombre MAPI http://schemas.microsoft.com/mapi/proptag/0x3D150102 para obtener la propiedad PR\_EMSMDB\_SECTION\_UID de una lista de direcciones y la propiedad PR\_EMSMDB\_SECTION\_UID de un almacén actual. GetGlobalAddressList identifica una lista de direcciones como asociada con un almacén si sus propiedades PR\_EMSMDB\_SECTION\_UID coinciden, y devuelve un conjunto de listas de direcciones para el almacén actual. EnumerateAddressListsForStore luego usa las propiedades [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) y[ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) del objeto **AddressList** para mostrar el tipo y el orden de resolución para cada lista de direcciones devuelta.

```csharp
private void EnumerateAddressListsForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    List<Outlook.AddressList> addrListsForStore = 
        GetAddressLists(currentStore);
    foreach (Outlook.AddressList addrList in addrListsForStore)
    {
        Debug.WriteLine(addrList.Name 
            + " " + addrList.AddressListType.ToString()
            + " Resolution Order: " +
            addrList.ResolutionOrder);
    }
}
public List<Outlook.AddressList> GetAddressLists(Outlook.Store store)
{
    List<Outlook.AddressList> addrLists = 
        new List<Microsoft.Office.Interop.Outlook.AddressList>();
    string PR_EMSMDB_SECTION_UID =
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList =
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID)
        {
            addrLists.Add(addrList);
        }
    }
    return addrLists;
}
```

## <a name="see-also"></a>Vea también

- [Libreta de direcciones](address-book.md)

