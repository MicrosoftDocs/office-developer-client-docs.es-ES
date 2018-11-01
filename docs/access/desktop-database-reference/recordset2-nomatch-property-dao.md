---
title: Recordset2.NoMatch Property (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbc35b696f74aa0da64ec24ce38c2f8ad8cfab4d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879097"
---
# <a name="recordset2nomatch-property-dao"></a><span data-ttu-id="61f22-102">Recordset2.NoMatch Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="61f22-102">Recordset2.NoMatch Property (DAO)</span></span>


<span data-ttu-id="61f22-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61f22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61f22-104">Indica si se encontró un registro concreto al utilizar el método **[Seek](recordset2-seek-method-dao.md)** o uno de los métodos **[Find](recordset2-findfirst-method-dao.md)** (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="61f22-104">Indicates whether a particular record was found by using the **[Seek](recordset2-seek-method-dao.md)** method or one of the **[Find](recordset2-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="61f22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61f22-105">Syntax</span></span>

<span data-ttu-id="61f22-106">*expresión* . NoMatch</span><span class="sxs-lookup"><span data-stu-id="61f22-106">*expression* .NoMatch</span></span>

<span data-ttu-id="61f22-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="61f22-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f22-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61f22-108">Remarks</span></span>

<span data-ttu-id="61f22-109">Cuando abre o crea un objeto **[Recordset](recordset-object-dao.md)**, su propiedad **NoMatch** se establece en **False**.</span><span class="sxs-lookup"><span data-stu-id="61f22-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="61f22-p101">Para localizar un registro, use el método **Seek** en un objeto **Recordset** tipo tabla o use uno de los métodos **Find** en un objeto **Recordset** de tipo Dynaset o Snapshot. Compruebe el valor de la propiedad **NoMatch** para ver si se encontró el registro.</span><span class="sxs-lookup"><span data-stu-id="61f22-p101">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object. Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="61f22-p102">Si el método **Seek** o el método **Find** no se han ejecutado correctamente y la propiedad **NoMatch** es **True**, el registro actual ya no será válido. Si va a necesitar volver a un registro, asegúrese de obtener el marcador del registro actual antes de utilizar el método **Seek** o un método **Find**.</span><span class="sxs-lookup"><span data-stu-id="61f22-p102">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid. Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="61f22-114">[!NOTA] Cuando se usa alguno de los métodos <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> en un objeto <STRONG>Recordset</STRONG> no se afecta al valor de su propiedad <STRONG>NoMatch</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="61f22-114">Using any of the <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> methods on a <STRONG>Recordset</STRONG> object won't affect its <STRONG>NoMatch</STRONG> property setting.</span></span></P>



## <a name="example"></a><span data-ttu-id="61f22-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61f22-115">Example</span></span>

<span data-ttu-id="61f22-p103">En este ejemplo se utiliza la propiedad **NoMatch** para determinar si **Seek** y **FindFirst** han tenido un resultado correcto y, en caso contrario, proporcionar información adecuada. Se necesitan los procedimientos SeekMatch y FindMatch para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="61f22-p103">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
