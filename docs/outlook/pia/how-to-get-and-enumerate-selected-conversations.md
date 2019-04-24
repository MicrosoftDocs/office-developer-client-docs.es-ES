---
title: Obtener y enumerar las conversaciones seleccionadas
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d71fc1d582abebc8cb00f4885ec5b5ba348228c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320317"
---
# <a name="get-and-enumerate-selected-conversations"></a>Obtener y enumerar las conversaciones seleccionadas

En este ejemplo se obtienen y se enumeran las conversaciones seleccionadas mediante el método [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).

## <a name="example"></a>Ejemplo

Microsoft Outlook puede configurarse para mostrar los elementos de la Bandeja de entrada por conversación. Si un usuario hace una selección en la Bandeja de entrada, puede obtener la selección mediante programación, incluidos los encabezados de conversación y los elementos de conversación. En el ejemplo de código de este tema se muestra cómo obtener una selección de la Bandeja de entrada y enumerar los elementos de correo de cada conversación contenidos en la selección.

El ejemplo contiene un método: DemoConversationHeadersFromSelection. El método establece la vista actual en la Bandeja de entrada y, a continuación, comprueba si la vista actual es una vista de tabla que muestra las conversaciones ordenadas por fecha. Para obtener una selección, incluidos los objetos [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) seleccionados, DemoConversationHeadersFromSelection usa el método **GetSelection** del objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) mediante la especificación de la constante [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) como argumento. Si los encabezados de conversación están seleccionados, DemoConversationHeadersFromSelection usa el objeto [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\))para enumerar los elementos contenidos en cada una de las conversaciones seleccionadas y, a continuación, muestra el asunto de esos elementos de conversación, que son objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoConversationHeadersFromSelection()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType ==
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view =
            inbox.CurrentView as Outlook.TableView;
        if (view.ShowConversationByDate == true)
        {
            Outlook.Selection selection =
                Application.ActiveExplorer().Selection;
            Debug.WriteLine("Selection.Count = " + selection.Count);
            // Call GetSelection to create a Selection object
            // that contains ConversationHeader objects.
            Outlook.Selection convHeaders =
                selection.GetSelection(
                Outlook.OlSelectionContents.olConversationHeaders)
                as Outlook.Selection;
            Debug.WriteLine("Selection.Count (ConversationHeaders) = " 
                + convHeaders.Count);
            if (convHeaders.Count >= 1)
            {
                foreach (Outlook.ConversationHeader convHeader in convHeaders)
                {
                    // Enumerate the items in the ConversationHeader.
                    Outlook.SimpleItems items = convHeader.GetItems();
                    for (int i = 1; i <= items.Count; i++)
                    {
                        // Enumerate only MailItems in this example.
                        if (items[i] is Outlook.MailItem)
                        {
                            Outlook.MailItem mail = 
                                items[i] as Outlook.MailItem;
                            Debug.WriteLine(mail.Subject 
                                + " Received:" + mail.ReceivedTime);
                        }
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Conversaciones](conversations.md)

