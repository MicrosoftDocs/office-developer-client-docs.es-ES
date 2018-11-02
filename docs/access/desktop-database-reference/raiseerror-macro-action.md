---
title: ProvocarError (acción de macro)
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3e778c8dce83ecad32328f0d7ad762d9f825a6d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919783"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="e2e0a-102">ProvocarError (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e2e0a-102">RaiseError macro action</span></span>

<span data-ttu-id="e2e0a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2e0a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="e2e0a-104">La acción **ProvocarError** produce una excepción que se puede controlar mediante la acción de macro **[AlOcurrirError](onerror-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="e2e0a-105">[!NOTA] La acción **ProvocarError** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="e2e0a-106">Valores</span><span class="sxs-lookup"><span data-stu-id="e2e0a-106">Setting</span></span>

<span data-ttu-id="e2e0a-107">La acción **ProvocarError** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2e0a-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="e2e0a-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e2e0a-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e2e0a-109">Required</span></span></p></th>
<th><p><span data-ttu-id="e2e0a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2e0a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2e0a-111">Número de error </span><span class="sxs-lookup"><span data-stu-id="e2e0a-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="e2e0a-112">Sí</span><span class="sxs-lookup"><span data-stu-id="e2e0a-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="e2e0a-113">Un número o una expresión que da como resultado el tipo de datos Long .</span><span class="sxs-lookup"><span data-stu-id="e2e0a-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2e0a-114">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="e2e0a-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="e2e0a-115">No</span><span class="sxs-lookup"><span data-stu-id="e2e0a-115">No</span></span></p></td>
<td><p><span data-ttu-id="e2e0a-116">Una expresión de cadena que describe el error.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e2e0a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2e0a-117">Remarks</span></span>

<span data-ttu-id="e2e0a-118">Si se llama a la acción **ProvocarError** en un evento de macro **[Cambio previo](before-change-macro-event.md)** o **[Eliminación previa](before-delete-macro-event.md)**, se cancela el evento.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="e2e0a-p101">Si no hay ninguna instrucción **AlOcurrirError** activa que esté controlando los errores, el error provocado por la acción **ProvocarError** se agrega a la tabla de sistema **USysApplicationLog**. Cuando la acción **ProvocarError** se escribe en la tabla **USysApplicationLog**, la columna **Categoría** se establece automáticamente en **Ejecución**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-p101">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="e2e0a-121">Para ver la tabla **USysApplicationLog**, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="e2e0a-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="e2e0a-122">Haga clic en el menú **archivo** y, a continuación, haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="e2e0a-123">En el cuadro de diálogo **Opciones de Access**, haga clic en la pestaña **Base de datos actual**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="e2e0a-124">En la sección **Navegación**, haga clic en **Opciones de navegación**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="e2e0a-125">En el cuadro de diálogo **Opciones de navegación**, haga clic en **Mostrar objetos del sistema** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="e2e0a-126">Haga clic en **Aceptar** para descartar el cuadro de diálogo **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="e2e0a-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2e0a-127">Example</span></span>

<span data-ttu-id="e2e0a-128">En el ejemplo siguiente se muestra cómo usar la acción Provocarerror para cancelar el evento de macro de datos antes de cambiar.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="e2e0a-129">Cuando se actualiza el campo AssignedTo, un bloque de datos BuscarRegistro se usa para determinar si el técnico asignado actualmente está asignado a una solicitud de servicio abiertas.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="e2e0a-130">Si es true, a continuación, se cancela el evento cambio previo y no se actualiza el registro.</span><span class="sxs-lookup"><span data-stu-id="e2e0a-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="e2e0a-131">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e2e0a-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
