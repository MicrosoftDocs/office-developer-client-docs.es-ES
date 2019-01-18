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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704402"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a>Buscar y obtener elementos en una vista agregada

En este ejemplo se muestra cómo buscar elementos en varias carpetas y almacenes para devolver los elementos en una vista agregada de tabla.

## <a name="example"></a>Ejemplo

El método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) del objeto[TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) puede devolver, en una vista agregada, un objeto[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) que contiene elementos de una o más carpetas del mismo almacén o de varios almacenes. Esto es muy útil cuando se quiere tener acceso a elementos devueltos de una búsqueda (por ejemplo, una búsqueda de todos los elementos de un almacén). Este tema muestra un ejemplo de cómo usar la **Búsqueda instantánea** para buscar todos los elementos recibidos del administrador del usuario actual que están marcados como importantes, y luego mostrar el asunto de cada resultado de la búsqueda.

En el ejemplo siguiente, el método **GetItemsInView** comprueba si la cuenta primaria del almacén de entrega del usuario actual es una cuenta de Exchange, si el usuario actual tiene un administrador y si la **Búsqueda instantánea** está operativa en el almacén predeterminado de la sesión. Como la búsqueda se basa en el método [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) del objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)), y el resultado de la búsqueda se obtiene mediante el método **GetTable**, **GetItemsInView** crea un objeto **Explorer**, muestra la Bandeja de entrada en este objeto, y lo usa para configurar la búsqueda. 

**GetItemsInView** busca en todas las carpetas del tipo [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) los elementos del administrador del usuario actual que están marcados como importantes. Una vez que **GetItemsInView** llama al método [Explorer.Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), los resultados de la búsqueda se muestran en el Explorador, incluso los elementos de otras carpetas y almacenes que cumplan los criterios de búsqueda. **GetItemsInView** obtiene un objeto **TableView** que contiene esta vista del explorador de los resultados de la búsqueda. Mediante el método **GetTable** de este objeto **TableView**, **GetItemsInView** obtiene después un objeto **Table** que contiene los elementos agregados devueltos de la búsqueda. Por último, **GetItemsInView** muestra la columna de asunto de cada fila del objeto **Table** que representa un elemento en los resultados de la búsqueda.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Buscar y filtrar](search-and-filter.md)

