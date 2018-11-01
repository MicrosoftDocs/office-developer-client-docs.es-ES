---
title: Recordset.PercentPosition Property (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e319cea6e33f2f40490d5236746337040bf16dae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888695"
---
# <a name="recordsetpercentposition-property-dao"></a><span data-ttu-id="f865a-102">Recordset.PercentPosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f865a-102">Recordset.PercentPosition Property (DAO)</span></span>


<span data-ttu-id="f865a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f865a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f865a-104">Establece o devuelve un valor que indica la ubicación aproximada del registro actual en el objeto **[Recordset](recordset-object-dao.md)** a partir de un porcentaje de los registros en **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f865a-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f865a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f865a-105">Syntax</span></span>

<span data-ttu-id="f865a-106">*expresión* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="f865a-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="f865a-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f865a-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f865a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f865a-108">Remarks</span></span>

<span data-ttu-id="f865a-p101">Para indicar o cambiar la ubicación aproximada del registro actual en un objeto **Recordset**, puede comprobar o establecer la propiedad **PercentPosition**. Al trabajar con un objeto **Recordset** de tipo Dynaset o Snapshot abierto directamente desde una tabla base, primero rellene el objeto **Recordset** moviendo el último registro antes de establecer o comprobar la propiedad **PercentPosition**. Si usa la propiedad **PercentPosition** antes de rellenar completamente el objeto **Recordset**, el número de movimientos será relativo al número de registros a los que se tuvo acceso como indica el valor de la propiedad **[RecordCount](recordset-recordcount-property-dao.md)**. Puede moverse hasta el último registro usando el método **[MoveLast](recordset-movelast-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f865a-p101">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset-movelast-method-dao.md)** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f865a-113">[!NOTA] No se recomienda usar la propiedad <STRONG>PercentPosition</STRONG> para mover el registro actual hasta un registro específico en un objeto <STRONG>Recordset</STRONG>, la propiedad <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> es más apropiada para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="f865a-113">Using the <STRONG>PercentPosition</STRONG> property to move the current record to a specific record in a <STRONG>Recordset</STRONG> object isn't recommended?the <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> property is better suited for this task.</span></span></P>



<span data-ttu-id="f865a-p102">Una vez que establezca la propiedad **PercentPosition** en un valor, el registro en la ubicación aproximada correspondiente a ese valor se convierte en el actual y la propiedad **PercentPosition** se restablece con el valor que refleja la ubicación aproximada del registro actual. Por ejemplo, si su objeto **Recordset** contiene solo cinco registros y establece el valor de su propiedad **PercentPosition** en 77, el valor devuelto desde la propiedad **PercentPosition** puede que sea 80 y no 77.</span><span class="sxs-lookup"><span data-stu-id="f865a-p102">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record. For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="f865a-116">La propiedad **PercentPosition** se aplica a todos los tipos de objetos **Recordset** excepto los objetos **Recordset** de tipo forward – only o los objetos **Recordset** abiertos desde consultas de paso a través con bases de datos remotas.</span><span class="sxs-lookup"><span data-stu-id="f865a-116">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="f865a-117">Puede usar la propiedad **PercentPosition** con una barra de desplazamiento en un formulario o en un cuadro de texto para indicar la ubicación del registro actual en un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f865a-117">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="f865a-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f865a-118">Example</span></span>

<span data-ttu-id="f865a-119">En este ejemplo se usa la propiedad **PercentPosition** para mostrar la ubicación del puntero de registro actual con respecto al principio del **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f865a-119">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
