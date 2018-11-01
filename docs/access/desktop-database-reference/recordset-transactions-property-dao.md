---
title: Recordset.Transactions Property (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3b34f8f027b2e70ada94c6d15584cf25a4aec1c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873295"
---
# <a name="recordsettransactions-property-dao"></a><span data-ttu-id="dfc5f-102">Recordset.Transactions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="dfc5f-102">Recordset.Transactions Property (DAO)</span></span>


<span data-ttu-id="dfc5f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfc5f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfc5f-p101">Devuelve un valor que indica si un objeto admite transacciones. **Boolean** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-p101">Returns a value that indicates whether an object supports transactions. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc5f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfc5f-106">Syntax</span></span>

<span data-ttu-id="dfc5f-107">*expresión* . Transacciones</span><span class="sxs-lookup"><span data-stu-id="dfc5f-107">*expression* .Transactions</span></span>

<span data-ttu-id="dfc5f-108">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="dfc5f-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc5f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfc5f-109">Remarks</span></span>

<span data-ttu-id="dfc5f-110">En un área de trabajo de Microsoft Access, también puede usar la propiedad **Transactions** con objetos **Recordset** de tipo Dynaset o de tabla.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="dfc5f-111">Objetos **[Recordset](recordset-object-dao.md)** de tipo Snapshot y forward – only siempre devuelven **False**.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="dfc5f-p103">Si un objeto **Recordset** de tipo Dynaset o Table se basa en una tabla de motor de base de datos de Microsoft Access, la propiedad **Transactions** será **True** y se pueden usar las transacciones. Puede ser que otros motores de bases de datos no admitan transacciones. Por ejemplo, no se pueden usar transacciones en un objeto **Recordset** de tipo Dynaset basado en una tabla de Paradox.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="dfc5f-p104">Compruebe la propiedad **Transactions** antes de usar el método **[BeginTrans](dbengine-begintrans-method-dao.md)** en el objeto [**Workspace**](workspace-object-dao.md) del objeto **Recordset** para asegurarse de que se admiten transacciones. El uso de los métodos **BeginTrans**, **CommitTrans** o **Rollback** no tiene ningún efecto en un objeto no admitido.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="dfc5f-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfc5f-117">Example</span></span>

<span data-ttu-id="dfc5f-118">En este ejemplo se muestra la propiedad **Transactions** en áreas de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

