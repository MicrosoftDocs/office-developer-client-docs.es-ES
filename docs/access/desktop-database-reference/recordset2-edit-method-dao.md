---
title: Recordset2.Edit (método) (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1ab4577c9bfc487d7ce8d3c271b6a5c8edb37028
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997199"
---
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="289a1-102">Recordset2.Edit (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="289a1-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="289a1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="289a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="289a1-104">Copia el registro actual de un objeto **[Recordset](recordset-object-dao.md)** actualizable en el búfer de copias para su posterior modificación.</span><span class="sxs-lookup"><span data-stu-id="289a1-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="289a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="289a1-105">Syntax</span></span>

<span data-ttu-id="289a1-106">*expresión* . Editar</span><span class="sxs-lookup"><span data-stu-id="289a1-106">*expression* .Edit</span></span>

<span data-ttu-id="289a1-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="289a1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="289a1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="289a1-108">Remarks</span></span>

<span data-ttu-id="289a1-p101">Después de usar el método **Edit**, los cambios efectuados en los campos del registro actual se copian en el búfer de copias. Tras realizar los cambios necesarios en el registro, use el método **[Update](recordset2-update-method-dao.md)** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="289a1-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="289a1-111">El registro actual sigue siendo el registro actual después de usar **Edit**.</span><span class="sxs-lookup"><span data-stu-id="289a1-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="289a1-112">[!NOTA] Si edita un registro y realiza cualquier operación que mueva a otro registro pero sin usar primero **Update**, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="289a1-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="289a1-113">Además, si cierra recordset o termina el procedimiento que declara el **objeto Recordset** o el objeto primario de **[base de datos](database-object-dao.md)** o **[conexión](connection-object-dao.md)** , el registro editado se descarta sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="289a1-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="289a1-114">El uso de **Edit** produce un error si:</span><span class="sxs-lookup"><span data-stu-id="289a1-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="289a1-115">No hay ningún registro actual.</span><span class="sxs-lookup"><span data-stu-id="289a1-115">There is no current record.</span></span>

- <span data-ttu-id="289a1-116">El objeto **Connection**, **Database** o **Recordset** se abre como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="289a1-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="289a1-117">No hay campos actualizables en el registro.</span><span class="sxs-lookup"><span data-stu-id="289a1-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="289a1-118">El objeto **Database** o **Recordset** se abrió para uso exclusivo de otro usuario (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="289a1-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="289a1-119">Otro usuario ha bloqueado la página que contiene el registro (área de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="289a1-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="289a1-p103">En un área de trabajo de Microsoft Access, cuando el valor de la propiedad [**LockEdits**](recordset2-lockedits-property-dao.md) del objeto **Recordset** es **True** (bloqueo pesimista) en un entorno multiusuario, el registro permanece bloqueado desde que se usa **Edit** hasta que finaliza la actualización. Si el valor de la propiedad **LockEdits** es **False** (bloqueo optimista), el registro se bloquea y se compara con el registro previo a la modificación antes de actualizarse en la base de datos. Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error en tiempo de ejecución si usa **OpenRecordset** sin especificar **dbSeeChanges**. De manera predeterminada, las bases de datos de ODBC e ISAM instalable conectadas al motor de base de datos de Microsoft Access usan siempre el bloqueo optimista.</span><span class="sxs-lookup"><span data-stu-id="289a1-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="289a1-p104">[!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** o **Edit** en un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="289a1-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="289a1-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="289a1-126">Example</span></span>

<span data-ttu-id="289a1-p105">En este ejemplo se usa el método **Edit** para reemplazar los datos actuales por el nombre especificado. Se necesita el procedimiento EditName para que se pueda ejecutar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="289a1-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
