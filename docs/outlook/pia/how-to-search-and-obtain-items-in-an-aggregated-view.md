---
title: Buscar y obtener elementos en una vista agregada
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92f99069dae2976a00ac075f605754fe8704ae60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342766"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a><span data-ttu-id="84bf5-102">Buscar y obtener elementos en una vista agregada</span><span class="sxs-lookup"><span data-stu-id="84bf5-102">Search and obtain items in an aggregated view</span></span>

<span data-ttu-id="84bf5-103">En este ejemplo se muestra cómo buscar elementos en varias carpetas y almacenes para devolver los elementos en una vista agregada de tabla.</span><span class="sxs-lookup"><span data-stu-id="84bf5-103">This example shows how to search for items in multiple folders and stores and to return those items in an aggregated table view.</span></span>

## <a name="example"></a><span data-ttu-id="84bf5-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84bf5-104">Example</span></span>

<span data-ttu-id="84bf5-105">El método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) del objeto[TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) puede devolver, en una vista agregada, un objeto[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) que contiene elementos de una o más carpetas del mismo almacén o de varios almacenes.</span><span class="sxs-lookup"><span data-stu-id="84bf5-105">The [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method of the [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) object can return, in an aggregated view, a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains items from one or more folders in the same store or spanning over multiple stores.</span></span> <span data-ttu-id="84bf5-106">Esto es muy útil cuando se quiere tener acceso a elementos devueltos de una búsqueda (por ejemplo, una búsqueda de todos los elementos de un almacén).</span><span class="sxs-lookup"><span data-stu-id="84bf5-106">This is particularly useful when you want to access items returned from a search (for example, a search on all mail items in a store).</span></span> <span data-ttu-id="84bf5-107">Este tema muestra un ejemplo de cómo usar la **Búsqueda instantánea** para buscar todos los elementos recibidos del administrador del usuario actual que están marcados como importantes, y luego mostrar el asunto de cada resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84bf5-107">This topic shows an example of how to use **Instant Search** to search for all items received from the manager of the current user that are marked important, and then display the subject of each search result.</span></span>

<span data-ttu-id="84bf5-108">En el ejemplo siguiente, el método **GetItemsInView** comprueba si la cuenta primaria del almacén de entrega del usuario actual es una cuenta de Exchange, si el usuario actual tiene un administrador y si la **Búsqueda instantánea** está operativa en el almacén predeterminado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="84bf5-108">In the following code example, the **GetItemsInView** method checks whether the current user’s primary delivery store account is an Exchange account, whether the current user has a manager, and whether **Instant Search** is operational in the default store of the session.</span></span> <span data-ttu-id="84bf5-109">Como la búsqueda se basa en el método [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) del objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)), y el resultado de la búsqueda se obtiene mediante el método **GetTable**, **GetItemsInView** crea un objeto **Explorer**, muestra la Bandeja de entrada en este objeto, y lo usa para configurar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84bf5-109">Because the search relies on the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object, and the search result is obtained by using the **GetTable** method, **GetItemsInView** creates an **Explorer** object, displays the Inbox in this object, and uses it to set up the search.</span></span> 

<span data-ttu-id="84bf5-110">**GetItemsInView** busca en todas las carpetas del tipo [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) los elementos del administrador del usuario actual que están marcados como importantes.</span><span class="sxs-lookup"><span data-stu-id="84bf5-110">**GetItemsInView** searches all folders of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) type for items from the current user's manager that are marked as important.</span></span> <span data-ttu-id="84bf5-111">Una vez que **GetItemsInView** llama al método [Explorer.Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), los resultados de la búsqueda se muestran en el Explorador, incluso los elementos de otras carpetas y almacenes que cumplan los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84bf5-111">After **GetItemsInView** calls the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method, any search results are displayed in the Explorer, including items from other folders and stores that meet the search criteria.</span></span> <span data-ttu-id="84bf5-112">**GetItemsInView** obtiene un objeto **TableView** que contiene esta vista del explorador de los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84bf5-112">**GetItemsInView** gets a **TableView** object that contains this explorer view of the search results.</span></span> <span data-ttu-id="84bf5-113">Mediante el método **GetTable** de este objeto **TableView**, **GetItemsInView** obtiene después un objeto **Table** que contiene los elementos agregados devueltos de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84bf5-113">By using the **GetTable** method of this **TableView** object, **GetItemsInView** then gets a **Table** object that contains the aggregated items returned from the search.</span></span> <span data-ttu-id="84bf5-114">Por último, **GetItemsInView** muestra la columna de asunto de cada fila del objeto **Table** que representa un elemento en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84bf5-114">Finally **GetItemsInView** displays the subject column of each row of the **Table** object that represents an item in the search results.</span></span>

<span data-ttu-id="84bf5-115">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="84bf5-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="84bf5-116">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="84bf5-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="84bf5-117">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="84bf5-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetItemsInView()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;

    // Check whether the current user uses the Exchange Server.
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();

        // Check whether the current user has a manager.
        if (manager != null)
        {
            string managerName = manager.Name;

            // Check whether Instant Search is enabled and 
            // operational in the default store.
            if (Application.Session.DefaultStore.IsInstantSearchEnabled)
            {
                Outlook.Folder inbox =
                    Application.Session.GetDefaultFolder(
                    Outlook.OlDefaultFolders.olFolderInbox);

                // Create a new explorer to display the Inbox as
                // the current folder.
                Outlook.Explorer explorer =
                    Application.Explorers.Add(inbox,
                    Outlook.OlFolderDisplayMode.olFolderDisplayNormal);

                // Make the new explorer visible.
                explorer.Display;

                // Search for items from the manager marked important, 
                // from all folders of the same item type as the current folder, 
                // which is the MailItem item type.
                string searchFor =
                    "from:" + "\"" + managerName 
                    + "\"" + " importance:high";
                explorer.Search(searchFor,
                    Outlook.OlSearchScope.olSearchScopeAllFolders);

                // Any search results are displayed in that new explorer
                // in an aggregated table view.
                Outlook.TableView tableView = 
                    explorer.CurrentView as Outlook.TableView;

                // Use GetTable of that table view to obtain items in that
                // aggregated view in a Table object.
                Outlook.Table table = tableView.GetTable();
                while (!table.EndOfTable)
                {
                    // Then display each row in the Table object
                    // that represents an item in the search results.
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="84bf5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="84bf5-118">See also</span></span>

- <span data-ttu-id="84bf5-119">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="84bf5-119">[Search and filter](search-and-filter.md)</span></span>

