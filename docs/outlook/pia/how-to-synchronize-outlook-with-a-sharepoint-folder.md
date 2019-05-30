---
title: Sincronizar Outlook con una carpeta de SharePoint
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ab8da62d75b5714967c3fbdc0d0f985370e617aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540640"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a>Sincronizar Outlook con una carpeta de SharePoint

En este ejemplo se muestra cómo conectar Outlook con una carpeta de SharePoint y sincronizar el contenido de la carpeta mediante programación.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En Outlook, puede sincronizar calendarios, listas de contactos, listas de tareas, paneles de discusión y bibliotecas de documentos en las carpetas de SharePoint. Según la dirección URL proporcionada durante la sincronización, Outlook creará una nueva carpeta del mismo tipo base de la carpeta de SharePoint. Por ejemplo, la sincronización en una carpeta de calendario de SharePoint creará una nueva carpeta de calendario en Outlook. Las carpetas de sincronización de SharePoint se almacenan en su propio archivo de carpetas personales de Outlook (.pst) fuera del buzón de correo del usuario. Puede conectarse a una carpeta de SharePoint mediante el método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Tenga en cuenta que debe usar una dirección UR stssync:// que proporcione información sobre el servidor de SharePoint, la ruta de acceso a la carpeta y otra información que Outlook necesita para abrir una carpeta de SharePoint.

Al conectarse a una carpeta de SharePoint mediante programación, debe determinar la dirección URL correcta para crear la relación de uso compartido. Como la dirección URL stssync:// no se proporciona en la interfaz de usuario de SharePoint para la carpeta, debe vincular manualmente la carpeta de destino en Outlook. Después use el primer procedimiento, DisplaySharePointUrl, en el siguiente ejemplo de código para obtener la dirección URL correcta. DisplaySharePointUrl usa el objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) para buscar la información de enlace de uso compartido en la carpeta actual de la ventana activa del explorador. Si se encuentran uno o más contextos de enlace, se mostrarán las direcciones URL de todos los contextos de uso compartido disponibles.

Ahora tiene la dirección URL correcta para crear la relación de uso compartido. Para sincronizar la nueva carpeta de SharePoint en Outlook, copie y pegue la dirección URL de la asignación de la variable de cadena calendarUrl en el segundo procedimiento, AddSpsFolder. AddSpsFolder automatiza la sincronización de la nueva carpeta de SharePoint en Outlook mediante el método **NameSpace.OpenSharedFolder** con una dirección URL `stssync://` (en este caso, la dirección URL creada mediante el procedimiento DisplaySharePointUrl) . AddSpsFolderalso proporciona un nombre de carpeta personalizado, “Example SPS Calendar”, y especifica que Outlook use el Período de vida (TTL) predeterminado para la carpeta. Las carpetas de SharePoint descargan siempre los datos adjuntos del elemento, por lo que no debe especificarlo aquí.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "http://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a>Vea también

- [Uso compartido de grupos](group-sharing.md)

