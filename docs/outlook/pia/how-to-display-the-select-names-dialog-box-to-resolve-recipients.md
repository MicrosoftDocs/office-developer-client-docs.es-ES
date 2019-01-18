---
title: Mostrar el cuadro de diálogo Seleccionar nombres para resolver los destinatarios
TOCTitle: Display the Select Names dialog box to resolve recipients
ms:assetid: 841dd4cd-6d69-46d5-8c83-e28c95b631a9
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646055(v=office.15)
ms:contentKeyID: 55119876
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f92891188e7c317465ce70fede1dedca7f6344fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723043"
---
# <a name="display-the-select-names-dialog-box-to-resolve-recipients"></a><span data-ttu-id="262b5-102">Mostrar el cuadro de diálogo Seleccionar nombres para resolver los destinatarios</span><span class="sxs-lookup"><span data-stu-id="262b5-102">Display the Select Names dialog box to resolve recipients</span></span>

<span data-ttu-id="262b5-103">En este ejemplo se intentan resolver los destinatarios proporcionados por el parámetro *recips* y se muestra el cuadro de diálogo **Seleccionar nombres** de Outlook para cada destinatario que sea ambiguo y no se pueda resolver.</span><span class="sxs-lookup"><span data-stu-id="262b5-103">This example attempts to resolve the recipients provided by the *recips* parameter, and displays the Outlook **Select Names** dialog box for each recipient that is ambiguous and cannot be resolved.</span></span>

## <a name="example"></a><span data-ttu-id="262b5-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="262b5-104">Example</span></span>

<span data-ttu-id="262b5-105">Este ejemplo de código llama al objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) para mostrar el cuadro de diálogo **Seleccionar nombres** que muestra la libreta de direcciones de Outlook.</span><span class="sxs-lookup"><span data-stu-id="262b5-105">This code sample calls the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the **Select Names** dialog box which shows the Outlook address book.</span></span> <span data-ttu-id="262b5-106">Mediante este cuadro de diálogo, el usuario puede seleccionar un nombre de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="262b5-106">Through this dialog box, the user can select a name from the address book.</span></span> <span data-ttu-id="262b5-107">Si no se resuelve el nombre el destinatario, se quitará de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="262b5-107">If the name is not resolved, the recipient will be removed from recips.</span></span> <span data-ttu-id="262b5-108">Si se resuelve el nombre, el código de ejemplo devolverá el objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) del destinatario para los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="262b5-108">If the name is resolved, then the code sample will return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object of the recipient to recips.</span></span>

<span data-ttu-id="262b5-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="262b5-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="262b5-110">La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="262b5-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="262b5-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="262b5-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ResolveRecipients(ByVal recips As Outlook.Recipients)
    If recips Is Nothing Then
        Throw New ArgumentNullException()
    End If
    If recips.ResolveAll() Then
        Return
    Else
        For i As Integer = recips.Count To 1 Step -1
            If Not (recips(i).Resolve()) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.Recipients.Add(recips(i).Name)
                snd.NumberOfRecipientSelectors = _
                    Outlook.OlRecipientSelectors.olShowTo
                snd.AllowMultipleSelection = False
                snd.Display()
                If Not (snd.Recipients.ResolveAll()) Then
                    recips.Remove(i)
                Else
                    recips.Remove(i)
                    recips.Add(snd.Recipients(1).Address)
                End If
                snd = Nothing
            End If
        Next
    End If
End Sub
```


```csharp
private void ResolveRecipients(Outlook.Recipients recips)
{
    if (recips == null)
    {
        throw new ArgumentNullException();
    }
    if (recips.ResolveAll())
    {
        return;
    }
    else
    {
        for (int i = recips.Count; i > 0; i--)
        {
            if (!recips[i].Resolve())
            {
                Outlook.SelectNamesDialog snd =
                    Application.Session.
                    GetSelectNamesDialog();
                snd.Recipients.Add(recips[i].Name);
                snd.NumberOfRecipientSelectors =
                    Outlook.OlRecipientSelectors.olShowTo;
                snd.AllowMultipleSelection = false;
                snd.Display();
                if (!snd.Recipients.ResolveAll())
                {
                    recips.Remove(i);
                }
                else
                {
                    recips.Remove(i);
                    recips.Add(snd.Recipients[1].Address);
                }
                snd = null;
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="262b5-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="262b5-112">See also</span></span>

- [<span data-ttu-id="262b5-113">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="262b5-113">Recipients</span></span>](recipients.md)

