---
title: Botones de desplazamiento por la Libreta de direcciones
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f37a188fd3ddb3608eda414fbdcea6402cd9d41
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603948"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="b508d-102">Botones de desplazamiento por la Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="b508d-102">Address Book Navigation Buttons</span></span>


<span data-ttu-id="b508d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b508d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b508d-104"><<<<<<< Aplicación HEAD la libreta de direcciones muestra los botones de navegación en la parte inferior de la página Web.</span><span class="sxs-lookup"><span data-stu-id="b508d-104"><<<<<<< HEAD The Address Book application displays the navigation buttons at the bottom of the Web page.</span></span> <span data-ttu-id="b508d-105">Puede utilizar estos botones para desplazarse por los datos de la cuadrícula HTML seleccionando la primera o la última fila de datos o las filas adyacentes a la selección actual.</span><span class="sxs-lookup"><span data-stu-id="b508d-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
<span data-ttu-id="b508d-106">=== La aplicación de la libreta de direcciones muestra los botones de navegación en la parte inferior de la página Web.</span><span class="sxs-lookup"><span data-stu-id="b508d-106">======= The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="b508d-107">Puede utilizar estos botones para desplazarse por los datos de la cuadrícula HTML seleccionando la primera o la última fila de datos o las filas adyacentes a la selección actual.</span><span class="sxs-lookup"><span data-stu-id="b508d-107">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
>>>>>>> <span data-ttu-id="b508d-108">master</span><span class="sxs-lookup"><span data-stu-id="b508d-108">master</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="b508d-109">Procedimientos (Sub) de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="b508d-109">Navigation Sub Procedures</span></span>

<span data-ttu-id="b508d-110">La aplicación Libreta de direcciones contiene varios procedimientos que permiten a los usuarios hacer clic en los botones **Primero**, **Siguiente**, **Anterior** y **Último** para desplazarse por los datos.</span><span class="sxs-lookup"><span data-stu-id="b508d-110">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="b508d-111">Por ejemplo, al hacer clic en el **primer** botón activa la primera VBScript\_procedimiento OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="b508d-111">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="b508d-112">El procedimiento ejecuta un método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) que hace que la primera fila de datos pase a ser la selección actual.</span><span class="sxs-lookup"><span data-stu-id="b508d-112">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="b508d-113">Al hacer clic en el botón **último** , se activa la última\_procedimiento OnClick Sub, que invoca el método [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , hacer que la última fila de datos de la selección actual.</span><span class="sxs-lookup"><span data-stu-id="b508d-113">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="b508d-114">Los botones de navegación restantes funcionan de un modo similar.</span><span class="sxs-lookup"><span data-stu-id="b508d-114">The remaining navigation buttons work in a similar fashion.</span></span>

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

