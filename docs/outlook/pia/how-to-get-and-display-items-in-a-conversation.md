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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705613"
---
# <a name="get-and-display-items-in-a-conversation"></a>Administrar elementos en una conversación

En este ejemplo se muestra cómo obtener y mostrar los elementos de correo de una conversación.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente, DemoConversation obtiene un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))y, después, determina el almacén del objeto **MailItem** mediante la propiedad [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) del objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)). Después, DemoConversation comprueba si la propiedad [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) es **true**. Si es **true**, el código de ejemplo obtiene el objeto [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) mediante el método [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)). Si el objeto **Conversation** no es una referencia nula, el ejemplo obtiene el objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) asociado que contiene cada elemento de la conversación mediante el método [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)). 

Después, el ejemplo enumera todos los elementos del objeto **Table** y llama a EnumerateConversation en cada elemento para obtener acceso a los nodos secundarios de cada elemento. EnumerateConversation toma un objeto **Conversation** y obtiene los nodos secundarios mediante el método [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)). Se sigue llamando de forma recursiva a EnumerateConversation hasta que no quedan más nodos secundarios. Después, se muestra al usuario cada elemento de la conversación.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Conversaciones](conversations.md)

