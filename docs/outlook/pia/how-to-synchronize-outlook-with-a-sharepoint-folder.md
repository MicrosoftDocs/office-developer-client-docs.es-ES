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
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a><span data-ttu-id="04d6b-102">Sincronizar Outlook con una carpeta de SharePoint</span><span class="sxs-lookup"><span data-stu-id="04d6b-102">Synchronize Outlook with a SharePoint folder</span></span>

<span data-ttu-id="04d6b-103">En este ejemplo se muestra cómo conectar Outlook con una carpeta de SharePoint y sincronizar el contenido de la carpeta mediante programación.</span><span class="sxs-lookup"><span data-stu-id="04d6b-103">This example shows how to programmatically connect Outlook with a SharePoint folder and to synchronize the folder contents.</span></span>

## <a name="example"></a><span data-ttu-id="04d6b-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04d6b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="04d6b-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="04d6b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="04d6b-106">En Outlook, puede sincronizar calendarios, listas de contactos, listas de tareas, paneles de discusión y bibliotecas de documentos en las carpetas de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="04d6b-106">In Outlook, you can synchronize calendars, contact lists, task lists, discussion boards, and document libraries to SharePoint folders.</span></span> <span data-ttu-id="04d6b-107">Según la dirección URL proporcionada durante la sincronización, Outlook creará una nueva carpeta del mismo tipo base de la carpeta de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="04d6b-107">Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder.</span></span> <span data-ttu-id="04d6b-108">Por ejemplo, la sincronización en una carpeta de calendario de SharePoint creará una nueva carpeta de calendario en Outlook.</span><span class="sxs-lookup"><span data-stu-id="04d6b-108">For example, synchronizing to a SharePoint calendar folder will create a new calendar folder in Outlook.</span></span> <span data-ttu-id="04d6b-109">Las carpetas de sincronización de SharePoint se almacenan en su propio archivo de carpetas personales de Outlook (.pst) fuera del buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="04d6b-109">SharePoint synchronization folders are stored in their own Outlook Personal Folders (.pst) file outside of the user’s mailbox.</span></span> <span data-ttu-id="04d6b-110">Puede conectarse a una carpeta de SharePoint mediante el método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="04d6b-110">You can connect to a SharePoint folder by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="04d6b-111">Tenga en cuenta que debe usar una dirección UR stssync:// que proporcione información sobre el servidor de SharePoint, la ruta de acceso a la carpeta y otra información que Outlook necesita para abrir una carpeta de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="04d6b-111">Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.</span></span>

<span data-ttu-id="04d6b-112">Al conectarse a una carpeta de SharePoint mediante programación, debe determinar la dirección URL correcta para crear la relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="04d6b-112">When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship.</span></span> <span data-ttu-id="04d6b-113">Como la dirección URL stssync:// no se proporciona en la interfaz de usuario de SharePoint para la carpeta, debe vincular manualmente la carpeta de destino en Outlook.</span><span class="sxs-lookup"><span data-stu-id="04d6b-113">Because the stssync:// URL is not provided in the SharePoint user interface for the folder, manually link the destination folder into Outlook.</span></span> <span data-ttu-id="04d6b-114">Después use el primer procedimiento, DisplaySharePointUrl, en el siguiente ejemplo de código para obtener la dirección URL correcta.</span><span class="sxs-lookup"><span data-stu-id="04d6b-114">Then use the first procedure, DisplaySharePointUrl, in the following code example, to get the correct URL.</span></span> <span data-ttu-id="04d6b-115">DisplaySharePointUrl usa el objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) para buscar la información de enlace de uso compartido en la carpeta actual de la ventana activa del explorador.</span><span class="sxs-lookup"><span data-stu-id="04d6b-115">DisplaySharePointUrl uses the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to look for the sharing binding information in the current folder for the active explorer window.</span></span> <span data-ttu-id="04d6b-116">Si se encuentran uno o más contextos de enlace, se mostrarán las direcciones URL de todos los contextos de uso compartido disponibles.</span><span class="sxs-lookup"><span data-stu-id="04d6b-116">If one or more binding contexts are found, the URLs for all available sharing contexts will be displayed.</span></span>

<span data-ttu-id="04d6b-117">Ahora tiene la dirección URL correcta para crear la relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="04d6b-117">Now you have the proper URL to create the sharing relationship.</span></span> <span data-ttu-id="04d6b-118">Para sincronizar la nueva carpeta de SharePoint en Outlook, copie y pegue la dirección URL de la asignación de la variable de cadena calendarUrl en el segundo procedimiento, AddSpsFolder.</span><span class="sxs-lookup"><span data-stu-id="04d6b-118">To synchronize the new SharePoint folder in Outlook, copy and paste the URL to the assignment of the string variable calendarUrl in the second procedure, AddSpsFolder.</span></span> <span data-ttu-id="04d6b-119">AddSpsFolder automatiza la sincronización de la nueva carpeta de SharePoint en Outlook mediante el método **NameSpace.OpenSharedFolder** con una dirección URL `stssync://` (en este caso, la dirección URL creada mediante el procedimiento DisplaySharePointUrl) .</span><span class="sxs-lookup"><span data-stu-id="04d6b-119">AddSpsFolder automates the synchronization of the new SharePoint folder in Outlook by using the **NameSpace.OpenSharedFolder** method with a `stssync://` URL (in this case, the URL produced by the DisplaySharePointUrl procedure).</span></span> <span data-ttu-id="04d6b-120">AddSpsFolderalso proporciona un nombre de carpeta personalizado, “Example SPS Calendar”, y especifica que Outlook use el Período de vida (TTL) predeterminado para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="04d6b-120">AddSpsFolderalso provides a custom folder name, “Example SPS Calendar”, and specifies Outlook to use the default Time to Live (TTL) for the folder.</span></span> <span data-ttu-id="04d6b-121">Las carpetas de SharePoint descargan siempre los datos adjuntos del elemento, por lo que no debe especificarlo aquí.</span><span class="sxs-lookup"><span data-stu-id="04d6b-121">SharePoint folders always download item attachments, so you do not have to specify that here.</span></span>

<span data-ttu-id="04d6b-122">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="04d6b-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="04d6b-123">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="04d6b-123">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="04d6b-124">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="04d6b-124">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="04d6b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="04d6b-125">See also</span></span>

- [<span data-ttu-id="04d6b-126">Uso compartido de grupos</span><span class="sxs-lookup"><span data-stu-id="04d6b-126">Group sharing</span></span>](group-sharing.md)

