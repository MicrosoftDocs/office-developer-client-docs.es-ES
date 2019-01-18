---
title: Crear una vista
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c91f43001d6c56ad3b4c316aede9845a5e0a0064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721874"
---
# <a name="create-a-view"></a>Crear una vista

En este ejemplo se usa el método [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) de la colección [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) para crear una vista para un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


Puede crear vistas personalizables que permitan ordenar, agrupar y ver datos de todos los tipos diferentes dentro del panel de vista de la ventana del explorador de Outlook. También puede personalizar vistas integradas mediante programación. En la tabla siguiente se enumeran objetos que representan vistas de Outlook. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de objeto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></p></td>
<td><p>Los datos se ven como una serie de imágenes de tarjeta de presentación electrónica.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></p></td>
<td><p>Los datos se ven en un formato de calendario.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></p></td>
<td><p>Los datos se ven en una serie de tarjetas.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></p></td>
<td><p>Los datos se ven como iconos de explorador o iconos de carpeta de Windows.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></p></td>
<td><p>Los datos se ven en una tabla sencilla basada en campos.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></p></td>
<td><p>Los datos se ven en una línea de tiempo lineal personalizable.</p></td>
</tr>
</tbody>
</table>


Puede acceder a las propiedades y los métodos comunes para todas las vistas mediante el objeto [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)). Sin embargo, para obtener acceso a algunas propiedades que no son comunes para todas las vistas, debe convertir el objeto **View** en un objeto **View** derivado al que pertenezca la propiedad a la que quiera obtener acceso. Por ejemplo, para obtener acceso a la propiedad [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) del objeto **Cardview**, debe convertir el objeto **View** en un objeto **Cardview**. Si quiere determinar qué tipo de vista se representa con un determinado objeto **View**, use la propiedad [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).

Para crear una nueva vista, use el método **Add** de la colección **Views** para un objeto **Folder**. Después, establezca la visibilidad de la vista en el momento de la creación o en cualquier momento después de crear la vista. Para establecer la visibilidad de la vista en el momento de creación, especifique una constante [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) en el parámetro *SaveOption* del método **Add**. Para establecer la visibilidad en cualquier momento después de la creación de la vista, especifique una constante **OlViewSaveOption** para la propiedad [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) del objeto **View**. 

Agregar una nueva vista genera el evento [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) de la colección **Views**. Una vez que se crea la vista, puede personalizarla mediante programación convirtiendo el objeto **View** en uno de los objetos derivados y, después, haciendo los cambios necesarios. Use el método **Save** del objeto **View** derivado del objeto **View** para guardar los cambios realizados en la vista. Por último, use el método **Apply** del objeto **View**derivado del objeto **View** para aplicar la vista al objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) actual. Esto genera el evento [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) del objeto **Explorer**.

En el ejemplo de código siguiente, CreateMeetingRequestsView agrega una nueva vista denominada "Meeting Requests" a la Bandeja de entrada del usuario convirtiendo el objeto **View** en un objeto **TableView**. Después, CreateMeetingRequestsView llama al método **Add** del objeto **Views** con el parámetro *Name* establecido en “Meeting Requests” y el parámetro *ViewType* establecido en **olTableView**. La propiedad [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) del objeto **TableView** se establece en una cadena de búsqueda y ubicación DAV (DASL) que hace que la vista se muestre únicamente cuando hay elementos que contienen "IPM.Schedule" en la clase de mensaje para el elemento. Después, se guarda y se aplica la nueva vista.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a>Vea también

- [Vistas](views.md)

