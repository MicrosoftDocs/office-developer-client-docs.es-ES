---
title: Obtener y enumerar las conversaciones seleccionadas
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: cf36003f183c9ddfe40cb2c27a9feab2962324d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405598"
---
# <a name="get-and-enumerate-selected-conversations"></a><span data-ttu-id="a89d4-102">Obtener y enumerar las conversaciones seleccionadas</span><span class="sxs-lookup"><span data-stu-id="a89d4-102">Get and enumerate selected conversations</span></span>

<span data-ttu-id="a89d4-103">En este ejemplo se obtienen y se enumeran las conversaciones seleccionadas mediante el método [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a89d4-103">This example obtains and enumerates selected conversations by using the [M:Microsoft.Office.Interop.Outlook.Selection.GetSelection(Microsoft.Office.Interop.Outlook.OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="a89d4-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a89d4-104">Example</span></span>

<span data-ttu-id="a89d4-105">Microsoft Outlook puede configurarse para mostrar los elementos de la Bandeja de entrada por conversación.</span><span class="sxs-lookup"><span data-stu-id="a89d4-105">Microsoft Outlook can be set to display items in the Inbox by conversation.</span></span> <span data-ttu-id="a89d4-106">Si un usuario hace una selección en la Bandeja de entrada, puede obtener la selección mediante programación, incluidos los encabezados de conversación y los elementos de conversación.</span><span class="sxs-lookup"><span data-stu-id="a89d4-106">If a user makes a selection in the Inbox, you can obtain the selection programmatically, including conversation headers and conversation items.</span></span> <span data-ttu-id="a89d4-107">En el ejemplo de código de este tema se muestra cómo obtener una selección de la Bandeja de entrada y enumerar los elementos de correo de cada conversación contenidos en la selección.</span><span class="sxs-lookup"><span data-stu-id="a89d4-107">The code example in this topic shows how to obtain a selection in the Inbox and enumerate the mail items in each conversation in the selection.The example contains one method,  .</span></span>

<span data-ttu-id="a89d4-108">El ejemplo contiene un método: DemoConversationHeadersFromSelection.</span><span class="sxs-lookup"><span data-stu-id="a89d4-108">The example contains one method, DemoConversationHeadersFromSelection.</span></span> <span data-ttu-id="a89d4-109">El método establece la vista actual en la Bandeja de entrada y, a continuación, comprueba si la vista actual es una vista de tabla que muestra las conversaciones ordenadas por fecha.</span><span class="sxs-lookup"><span data-stu-id="a89d4-109">The method sets the current view to the Inbox, and then checks to see if the current view is a table view that displays conversations sorted by date.</span></span> <span data-ttu-id="a89d4-110">Para obtener una selección, incluidos los objetos [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) seleccionados, DemoConversationHeadersFromSelection usa el método **GetSelection** del objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) mediante la especificación de la constante [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) como argumento.</span><span class="sxs-lookup"><span data-stu-id="a89d4-110">To obtain a selection, including any selected ConversationHeader objects,  uses theGetSelection method of theSelection object, specifying the OlSelectionContents.olConversationHeaders constant as an argument.</span></span> <span data-ttu-id="a89d4-111">Si los encabezados de conversación están seleccionados, DemoConversationHeadersFromSelection usa el objeto [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\))para enumerar los elementos contenidos en cada una de las conversaciones seleccionadas y, a continuación, muestra el asunto de esos elementos de conversación, que son objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a89d4-111">If conversation headers are selected,  uses theSimpleItems object to enumerate items in each selected conversation, and then displays the subject of those conversation items that areMailItem objects.The following managed code sample is written in C#.</span></span>

<span data-ttu-id="a89d4-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a89d4-112">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="a89d4-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="a89d4-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a89d4-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="a89d4-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a89d4-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a89d4-115">See also</span></span>

- [<span data-ttu-id="a89d4-116">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="a89d4-116">Conversations</span></span>](conversations.md)

