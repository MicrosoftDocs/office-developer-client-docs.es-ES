---
title: Administrar elementos en una conversación
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fcfe76632c2fda742a85a571d655569dc2fcd33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349465"
---
# <a name="get-and-display-items-in-a-conversation"></a><span data-ttu-id="36935-102">Administrar elementos en una conversación</span><span class="sxs-lookup"><span data-stu-id="36935-102">Get and display items in a conversation</span></span>

<span data-ttu-id="36935-103">En este ejemplo se muestra cómo obtener y mostrar los elementos de correo de una conversación.</span><span class="sxs-lookup"><span data-stu-id="36935-103">This example shows how to get and display mail items in a conversation.</span></span>

## <a name="example"></a><span data-ttu-id="36935-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36935-104">Example</span></span>

<span data-ttu-id="36935-105">En el ejemplo de código siguiente, DemoConversation obtiene un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))y, después, determina el almacén del objeto **MailItem** mediante la propiedad [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) del objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="36935-105">In the following code example, DemoConversation gets a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object and then determines the store of the **MailItem** object by using the [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) property of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="36935-106">Después, DemoConversation comprueba si la propiedad [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) es **true**. Si es **true**, el código de ejemplo obtiene el objeto [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) mediante el método [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="36935-106">DemoConversation then checks whether the [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) property is **true**; if it is **true**, the code example gets [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) object by using the [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)) method.</span></span> <span data-ttu-id="36935-107">Si el objeto **Conversation** no es una referencia nula, el ejemplo obtiene el objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) asociado que contiene cada elemento de la conversación mediante el método [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="36935-107">If the **Conversation** object is not a null reference, the example gets the associated [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains each item in the conversation by using the [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)) method.</span></span> 

<span data-ttu-id="36935-108">Después, el ejemplo enumera todos los elementos del objeto **Table** y llama a EnumerateConversation en cada elemento para obtener acceso a los nodos secundarios de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="36935-108">The example then enumerates each item in the **Table** and calls EnumerateConversation on each item to access the child nodes of each item.</span></span> <span data-ttu-id="36935-109">EnumerateConversation toma un objeto **Conversation** y obtiene los nodos secundarios mediante el método [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="36935-109">EnumerateConversation takes a **Conversation** object and gets the child nodes by using the [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)) method.</span></span> <span data-ttu-id="36935-110">Se sigue llamando de forma recursiva a EnumerateConversation hasta que no quedan más nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="36935-110">EnumerateConversation is called recursively until there are no more child nodes.</span></span> <span data-ttu-id="36935-111">Después, se muestra al usuario cada elemento de la conversación.</span><span class="sxs-lookup"><span data-stu-id="36935-111">Each conversation item is then displayed to the user.</span></span>

<span data-ttu-id="36935-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="36935-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="36935-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="36935-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="36935-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="36935-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
void DemoConversation()
{
    object selectedItem = 
        Application.ActiveExplorer().Selection[1];
    // For this example, you will work only with 
    //MailItem. Other item types such as
    //MeetingItem and PostItem can participate 
    //in Conversation.
    if (selectedItem is Outlook.MailItem)
    {
        // Cast selectedItem to MailItem.
        Outlook.MailItem mailItem =
            selectedItem as Outlook.MailItem; ;
        // Determine store of mailItem.
        Outlook.Folder folder = mailItem.Parent
            as Outlook.Folder;
        Outlook.Store store = folder.Store;
        if (store.IsConversationEnabled == true)
        {
            // Obtain a Conversation object.
            Outlook.Conversation conv =
                mailItem.GetConversation();
            // Check for null Conversation.
            if (conv != null)
            {
                // Obtain Table that contains rows 
                // for each item in Conversation.
                Outlook.Table table = conv.GetTable();
                Debug.WriteLine("Conversation Items Count: " +
                    table.GetRowCount().ToString());
                Debug.WriteLine("Conversation Items from Table:");
                while (!table.EndOfTable)
                {
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]
                        + " Modified: "
                        + nextRow["LastModificationTime"]);
                }
                Debug.WriteLine("Conversation Items from Root:");
                // Obtain root items and enumerate Conversation.
                Outlook.SimpleItems simpleItems 
                    = conv.GetRootItems();
                foreach (object item in simpleItems)
                {
                    // In this example, enumerate only MailItem type.
                    // Other types such as PostItem or MeetingItem
                    // can appear in Conversation.
                    if (item is Outlook.MailItem)
                    {
                        Outlook.MailItem mail = item
                            as Outlook.MailItem;
                        Outlook.Folder inFolder =
                            mail.Parent as Outlook.Folder;
                        string msg = mail.Subject
                            + " in folder " + inFolder.Name;
                        Debug.WriteLine(msg);
                    }
                    // Call EnumerateConversation 
                    // to access child nodes of root items.
                    EnumerateConversation(item, conv);
                }
            }
        }
    }
}

void EnumerateConversation(object item,
    Outlook.Conversation conversation)
{
    Outlook.SimpleItems items =
        conversation.GetChildren(item);
    if (items.Count > 0)
    {
        foreach (object myItem in items)
        {
            // In this example, enumerate only MailItem type.
            // Other types such as PostItem or MeetingItem
            // can appear in Conversation.
            if (myItem is Outlook.MailItem)
            {
                Outlook.MailItem mailItem =
                    myItem as Outlook.MailItem;
                Outlook.Folder inFolder =
                    mailItem.Parent as Outlook.Folder;
                string msg = mailItem.Subject
                    + " in folder " + inFolder.Name;
                Debug.WriteLine(msg);
            }
            // Continue recursion.
            EnumerateConversation(myItem, conversation);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="36935-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="36935-115">See also</span></span>

- [<span data-ttu-id="36935-116">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="36935-116">Conversations</span></span>](conversations.md)

