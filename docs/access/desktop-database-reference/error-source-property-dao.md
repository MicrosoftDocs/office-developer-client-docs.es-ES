---
title: Error.Source Property (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 51acfc5f349d6096028ef86aac480ce81c9b26bf
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860500"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="3bc26-102">Error.Source Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="3bc26-102">Error.Source Property (DAO)</span></span>


<span data-ttu-id="3bc26-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bc26-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="3bc26-104">Devuelve el nombre del objeto o de la aplicación que generó originalmente el error.</span><span class="sxs-lookup"><span data-stu-id="3bc26-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bc26-105">Syntax</span></span>

<span data-ttu-id="3bc26-106">*expresión* . Origen</span><span class="sxs-lookup"><span data-stu-id="3bc26-106">*expression* .Source</span></span>

<span data-ttu-id="3bc26-107">*expresión* Variable que representa un objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="3bc26-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc26-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bc26-108">Remarks</span></span>

<span data-ttu-id="3bc26-p101">El valor de la propiedad **Source** suele ser el identificador de programa o el nombre de clase del objeto. Use la propiedad **Source** para proporcionar a los usuarios información cuando el código no puede controlar un error generado en un objeto en otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="3bc26-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="3bc26-111">Por ejemplo, si para tener acceso a Microsoft Excel y se genera un error "División por cero", Microsoft Excel establece **Error.Number** en el código de Microsoft Excel correspondiente a dicho error y establece la propiedad **Source** en Excel.Application.</span><span class="sxs-lookup"><span data-stu-id="3bc26-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="3bc26-112">Observe que si el error se genera en otro objeto invocado por Microsoft Excel, este intercepta el error y sigue estableciendo **Error.Number** en el código de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3bc26-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="3bc26-113">Sin embargo, las otras propiedades del objeto **Error** (incluida la propiedad **Source**) conservarán los valores establecidos por el objeto que generó el error.</span><span class="sxs-lookup"><span data-stu-id="3bc26-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="3bc26-114">La propiedad **Source** siempre contiene el nombre del objeto que generó originalmente el error.</span><span class="sxs-lookup"><span data-stu-id="3bc26-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="3bc26-p103">Basándose en toda la documentación del error, puede escribir código que controlará el error apropiadamente. Si el controlador de errores no actúa correctamente, puede usar la información del objeto **[Error](error-object-dao.md)** para describir el error al usuario, utilizando la propiedad **Source** y las demás propiedades de **Error** con el fin de proporcionar al usuario información sobre qué objeto generó originalmente el error, la descripción del mismo, etc.</span><span class="sxs-lookup"><span data-stu-id="3bc26-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <span data-ttu-id="3bc26-p104">La construcción **On Error Resume Next** puede ser preferible a **On Error GoTo** cuando se tratan errores generados durante el acceso a otros objetos. La comprobación de la propiedad del objeto **Error** después de cada interacción con un objeto elimina la ambigüedad sobre cuál fue el objeto al que obtuvo acceso el código cuando se produjo el error. De este modo, puede saber con seguridad qué objeto colocó el código de error en **Error.Number** y qué objeto generó originalmente el error (**Error.Source**).</span><span class="sxs-lookup"><span data-stu-id="3bc26-p104">The **On Error Resume Next** construct may be preferable to **On Error GoTo** when dealing with errors generated during access to other objects. Checking the **Error** object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred. Thus, you can be sure which object placed the error code in **Error.Number**, as well as which object originally generated the error (**Error.Source**).</span></span>

## <a name="example"></a><span data-ttu-id="3bc26-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bc26-120">Example</span></span>

<span data-ttu-id="3bc26-121">En este ejemplo se fuerza un error, se captura y se muestran las propiedades **Description**, **Number**, **Source**, **HelpContext** y **HelpFile** del objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="3bc26-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb
    Sub DescriptionX() 
     
     Dim dbsTest As Database 
     
     On Error GoTo ErrorHandler 
     
     ' Intentionally trigger an error. 
     Set dbsTest = OpenDatabase("NoDatabase") 
     
     Exit Sub 
     
    ErrorHandler: 
     Dim strError As String 
     Dim errLoop As Error 
     
     ' Enumerate Errors collection and display properties of 
     ' each Error object. 
     For Each errLoop In Errors 
     With errLoop 
     strError = _ 
     "Error #" & .Number & vbCr 
     strError = strError & _ 
     " " & .Description & vbCr 
     strError = strError & _ 
     " (Source: " & .Source & ")" & vbCr 
     strError = strError & _ 
     "Press F1 to see topic " & .HelpContext & vbCr 
     strError = strError & _ 
     " in the file " & .HelpFile & "." 
     End With 
     MsgBox strError 
     Next 
     
     Resume Next 
     
    End Sub
```
