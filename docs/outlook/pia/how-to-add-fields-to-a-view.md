---
title: Agregar campos a una vista
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4b850bf87be4024152ee808624ad93836b904897
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705270"
---
# <a name="add-fields-to-a-view"></a>Agregar campos a una vista

En este ejemplo se muestra cómo personalizar una vista mediante el método [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) de la colección [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) para agregar campos a una vista.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Puede especificar qué propiedades de elemento de Outlook se muestran en una vista agregando una o más propiedades a la colección **ViewFields** solo para los objetos [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) y [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)). Para otros objetos **View** derivados como [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) y [TimelineView ](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) use otros métodos para determinar qué propiedades del elemento de Outlook se muestran en la vista. Por ejemplo, los campos que se muestran para el objeto **BusinessCardView** se determinan según el diseño de tarjeta de presentación electrónica (EBC) asociado a cada elemento de Outlook mostrado.

Para obtener la colección **ViewFields** para una vista, use la propiedad **ViewFields** del objeto **View** asociado (por ejemplo, los objetos **CardView**o **TableView**). El método **Add** de la colección **ViewFields** se utiliza para crear un objeto [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) que representa la propiedad del elemento de Outlook que se muestra en la vista. Un objeto **ViewField** no solo identifica la propiedad de elemento de Outlook que se va a mostrar dentro de la vista, sino que también describe cómo se deben mostrar los valores de dicha propiedad. Puede cambiar cómo se muestran las propiedades de columna en una vista modificando la propiedad [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) del objeto **ViewField**.

En el ejemplo de código siguiente, ModifyMeetingRequestsView obtiene el objeto **TableView** que representa todas las vistas desde la Bandeja de entrada del usuario que son vistas de "Convocatorias de reunión". A continuación, en el ejemplo se usa el método **Add** para agregar los campos "Inicio" y "Fin" al objeto **ViewFields** corresponde al objeto **TableView**. También se cambia la etiqueta para el campo "De" a "Organizada por". A continuación, ModifyMeetingRequestsView, guarda el objeto **TableView** modificado.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Vistas](views.md)

