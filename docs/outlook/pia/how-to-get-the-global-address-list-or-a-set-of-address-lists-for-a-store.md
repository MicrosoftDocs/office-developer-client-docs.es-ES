---
title: Obtener la lista global de direcciones o un conjunto de listas de direcciones para un almacén
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 582b0e836edc361d1d8717f94a5d7490c57cd530
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320121"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a><span data-ttu-id="f398a-102">Obtener la lista global de direcciones o un conjunto de listas de direcciones para un almacén</span><span class="sxs-lookup"><span data-stu-id="f398a-102">Get the Global Address List or a set of address lists for a store</span></span>

<span data-ttu-id="f398a-103">Este tema contiene dos códigos de ejemplo que muestran cómo obtener la lista global de direcciones (GAL) asociada a un almacén y cómo obtener todas las listas de direcciones asociadas a un almacén.</span><span class="sxs-lookup"><span data-stu-id="f398a-103">This topic contains two code examples that show how to get the Global Address List (GAL) that is associated with a store, and how to get all of the address lists that are associated with a store.</span></span>

## <a name="example"></a><span data-ttu-id="f398a-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f398a-104">Example</span></span>

<span data-ttu-id="f398a-105">En una sesión de Outlook donde hay varias cuentas de Exchange definidas en el perfil, puede haber varias listas de direcciones asociadas con un almacén.</span><span class="sxs-lookup"><span data-stu-id="f398a-105">In an Outlook session where multiple Exchange accounts are defined in the profile, there can be multiple address lists associated with a store.</span></span> <span data-ttu-id="f398a-106">En cada uno de los siguientes ejemplos de código, el almacén específico de interés es el almacén de la carpeta actual que se muestra en el explorador activo, pero el algoritmo para obtener una lista global de direcciones o un conjunto de objetos [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) de un almacén se aplica a cualquier almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f398a-106">In each of the following code examples, the specific store of interest is the store for the current folder displayed in the active explorer, but the algorithm to get a Global Address List or a set of [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) objects for a store applies to any Exchange store.</span></span>

<span data-ttu-id="f398a-107">El primer ejemplo de código contiene el método DisplayGlobalAddressListForStore y la función GetGlobalAddressList.</span><span class="sxs-lookup"><span data-stu-id="f398a-107">The first code example contains the DisplayGlobalAddressListForStore method and the GetGlobalAddressList function.</span></span> <span data-ttu-id="f398a-108">El método DisplayGlobalAddressListForStore muestra, en el cuadro de diálogo **Seleccionar nombres**, la Lista global de direcciones que está asociada con el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-108">The DisplayGlobalAddressListForStore method displays, in the **Select Names** dialog box, the Global Address List that is associated with the current store.</span></span> <span data-ttu-id="f398a-109">DisplayGlobalAddressListForStore obtiene primero el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-109">DisplayGlobalAddressListForStore first obtains the current store.</span></span> <span data-ttu-id="f398a-110">Si el almacén actual es un almacén de Exchange, llama a GetGlobalAddressList para obtener la Lista global de direcciones asociada con el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-110">If the current store is an Exchange store, GetGlobalAddressList is called to obtain the Global Address List associated with the current store.</span></span> 

<span data-ttu-id="f398a-111">GetGlobalAddressList usa el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) y la propiedad MAPI https://schemas.microsoft.com/mapi/proptag/0x3D150102 para obtener la propiedad PR\_EMSMDB\_SECTION\_UID de una lista de direcciones y el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-111">GetGlobalAddressList uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the MAPI property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list and the current store.</span></span> <span data-ttu-id="f398a-112">GetGlobalAddressList identifica una lista de direcciones como asociada con un almacén si sus propiedades PR\_EMSMDB\_SECTION\_UID coinciden, y la lista de direcciones es la lista global de direcciones si su propiedad [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) es [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f398a-112">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and the address list is the Global Address List if its [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) property is [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span></span> <span data-ttu-id="f398a-113">Si la llamada a GetGlobalAddressList es correcta, DisplayGlobalAddressListForStore usa el objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) para mostrar la lista global de direcciones devuelta en el cuadro de diálogo **Seleccionar nombres**.</span><span class="sxs-lookup"><span data-stu-id="f398a-113">If the call to GetGlobalAddressList succeeds, DisplayGlobalAddressListForStore uses the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the returned Global Address List in the **Select Names** dialog box.</span></span>

<span data-ttu-id="f398a-114">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f398a-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f398a-115">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="f398a-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f398a-116">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="f398a-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

<span data-ttu-id="f398a-117">El segundo ejemplo de código contiene el método EnumerateAddressListsForStore y la función GetAddressLists.</span><span class="sxs-lookup"><span data-stu-id="f398a-117">The second code example contains the EnumerateAddressListsForStore method and GetAddressLists function.</span></span> <span data-ttu-id="f398a-118">El método EnumerateAddressListsForStore muestra el tipo y el orden de resolución de cada lista de direcciones definida para el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-118">The EnumerateAddressListsForStore method displays the type and resolution order of each address list defined for the current store.</span></span> <span data-ttu-id="f398a-119">EnumerateAddressListsForStore primero obtiene el almacén actual y luego llama a GetAddressLists para obtener un objeto [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19) de .NET Framework genérico que contenga objetos AddressList para el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-119">EnumerateAddressListsForStore first obtains the current store, and then calls GetAddressLists to obtain a .NET Framework generic [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19) object that contains AddressList objects for the current store.</span></span> 

<span data-ttu-id="f398a-120">GetAddressLists enumera cada lista de direcciones definida para la sesión, usa el objeto PropertyAccessor y la propiedad con nombre MAPI https://schemas.microsoft.com/mapi/proptag/0x3D150102 para obtener la propiedad PR\_EMSMDB\_SECTION\_UID de una lista de direcciones y la propiedad PR\_EMSMDB\_SECTION\_UID de un almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-120">GetAddressLists enumerates each address list defined for the session, uses the PropertyAccessor object and the MAPI named property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list, and the PR\_EMSMDB\_SECTION\_UID property of a current store.</span></span> <span data-ttu-id="f398a-121">GetGlobalAddressList identifica una lista de direcciones como asociada con un almacén si sus propiedades PR\_EMSMDB\_SECTION\_UID coinciden, y devuelve un conjunto de listas de direcciones para el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="f398a-121">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and returns a set of address lists for the current store.</span></span> <span data-ttu-id="f398a-122">EnumerateAddressListsForStore luego usa las propiedades [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) y[ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) del objeto **AddressList** para mostrar el tipo y el orden de resolución para cada lista de direcciones devuelta.</span><span class="sxs-lookup"><span data-stu-id="f398a-122">EnumerateAddressListsForStore then uses the [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) and [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) properties of the **AddressList** object to display the type and resolution order for each returned address list.</span></span>

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
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

## <a name="see-also"></a><span data-ttu-id="f398a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f398a-123">See also</span></span>

- [<span data-ttu-id="f398a-124">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="f398a-124">Address book</span></span>](address-book.md)

