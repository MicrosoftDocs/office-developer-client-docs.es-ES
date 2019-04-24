---
title: Propiedad Recordset2. transActions (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309248"
---
# <a name="recordset2transactions-property-dao"></a><span data-ttu-id="06a0d-102">Propiedad Recordset2. transActions (DAO)</span><span class="sxs-lookup"><span data-stu-id="06a0d-102">Recordset2.Transactions property (DAO)</span></span>


<span data-ttu-id="06a0d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06a0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06a0d-104">Devuelve un valor que indica si un objeto admite transacciones.</span><span class="sxs-lookup"><span data-stu-id="06a0d-104">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="06a0d-105">**Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="06a0d-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06a0d-106">Syntax</span></span>

<span data-ttu-id="06a0d-107">*expresión* . Realizadas</span><span class="sxs-lookup"><span data-stu-id="06a0d-107">*expression* .Transactions</span></span>

<span data-ttu-id="06a0d-108">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="06a0d-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a0d-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06a0d-109">Remarks</span></span>

<span data-ttu-id="06a0d-110">En un área de trabajo de Microsoft Access, también puede usar la propiedad **Transactions** con objetos **Recordset** de tipo Dynaset o de tabla.</span><span class="sxs-lookup"><span data-stu-id="06a0d-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="06a0d-111">Los objetos **[Recordset](recordset-object-dao.md)** de tipo Snapshot y Forward – only siempre devuelven **false**.</span><span class="sxs-lookup"><span data-stu-id="06a0d-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="06a0d-p103">Si un objeto **Recordset** de tipo Dynaset o Table se basa en una tabla de motor de base de datos de Microsoft Access, la propiedad **Transactions** será **True** y se pueden usar las transacciones. Puede ser que otros motores de bases de datos no admitan transacciones. Por ejemplo, no se pueden usar transacciones en un objeto **Recordset** de tipo Dynaset basado en una tabla de Paradox.</span><span class="sxs-lookup"><span data-stu-id="06a0d-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="06a0d-p104">Compruebe la propiedad **Transactions** antes de usar el método **[BeginTrans](dbengine-begintrans-method-dao.md)** en el objeto [**Workspace**](workspace-object-dao.md) del objeto **Recordset** para asegurarse de que se admiten transacciones. El uso de los métodos **BeginTrans**, **CommitTrans** o **Rollback** no tiene ningún efecto en un objeto no admitido.</span><span class="sxs-lookup"><span data-stu-id="06a0d-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="06a0d-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06a0d-117">Example</span></span>

<span data-ttu-id="06a0d-118">En este ejemplo se muestra la propiedad **Transactions** en áreas de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="06a0d-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

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

