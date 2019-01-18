---
title: ProvocarError (acción de macro)
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726039"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="48f45-102">ProvocarError (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="48f45-102">RaiseError macro action</span></span>

<span data-ttu-id="48f45-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48f45-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="48f45-104">La acción **ProvocarError** produce una excepción que se puede controlar mediante la acción de macro **[AlOcurrirError](onerror-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="48f45-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="48f45-105">[!NOTA] La acción **ProvocarError** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="48f45-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="48f45-106">Valores</span><span class="sxs-lookup"><span data-stu-id="48f45-106">Setting</span></span>

<span data-ttu-id="48f45-107">La acción **ProvocarError** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="48f45-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f45-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="48f45-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="48f45-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="48f45-109">Required</span></span></p></th>
<th><p><span data-ttu-id="48f45-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="48f45-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f45-111">Número de error </span><span class="sxs-lookup"><span data-stu-id="48f45-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="48f45-112">Sí</span><span class="sxs-lookup"><span data-stu-id="48f45-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="48f45-113">Un número o una expresión que da como resultado el tipo de datos Long .</span><span class="sxs-lookup"><span data-stu-id="48f45-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f45-114">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="48f45-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="48f45-115">No</span><span class="sxs-lookup"><span data-stu-id="48f45-115">No</span></span></p></td>
<td><p><span data-ttu-id="48f45-116">Una expresión de cadena que describe el error.</span><span class="sxs-lookup"><span data-stu-id="48f45-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="48f45-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48f45-117">Remarks</span></span>

<span data-ttu-id="48f45-118">Si se llama a la acción **ProvocarError** en un evento de macro **[Cambio previo](before-change-macro-event.md)** o **[Eliminación previa](before-delete-macro-event.md)**, se cancela el evento.</span><span class="sxs-lookup"><span data-stu-id="48f45-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="48f45-p101">Si no hay ninguna instrucción **AlOcurrirError** activa que esté controlando los errores, el error provocado por la acción **ProvocarError** se agrega a la tabla de sistema **USysApplicationLog**. Cuando la acción **ProvocarError** se escribe en la tabla **USysApplicationLog**, la columna **Categoría** se establece automáticamente en **Ejecución**.</span><span class="sxs-lookup"><span data-stu-id="48f45-p101">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="48f45-121">Para ver la tabla **USysApplicationLog**, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="48f45-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="48f45-122">Haga clic en el menú **archivo** y, a continuación, haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="48f45-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="48f45-123">En el cuadro de diálogo **Opciones de Access**, haga clic en la pestaña **Base de datos actual**.</span><span class="sxs-lookup"><span data-stu-id="48f45-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="48f45-124">En la sección **Navegación**, haga clic en **Opciones de navegación**.</span><span class="sxs-lookup"><span data-stu-id="48f45-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="48f45-125">En el cuadro de diálogo **Opciones de navegación**, haga clic en **Mostrar objetos del sistema** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="48f45-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="48f45-126">Haga clic en **Aceptar** para descartar el cuadro de diálogo **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="48f45-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="48f45-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48f45-127">Example</span></span>

<span data-ttu-id="48f45-128">En el ejemplo siguiente se muestra cómo usar la acción Provocarerror para cancelar el evento de macro de datos antes de cambiar.</span><span class="sxs-lookup"><span data-stu-id="48f45-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="48f45-129">Cuando se actualiza el campo AssignedTo, un bloque de datos BuscarRegistro se usa para determinar si el técnico asignado actualmente está asignado a una solicitud de servicio abiertas.</span><span class="sxs-lookup"><span data-stu-id="48f45-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="48f45-130">Si es true, a continuación, se cancela el evento cambio previo y no se actualiza el registro.</span><span class="sxs-lookup"><span data-stu-id="48f45-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="48f45-131">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="48f45-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
