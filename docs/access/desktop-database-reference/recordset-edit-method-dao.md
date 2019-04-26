---
title: Método Recordset.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300542"
---
# <a name="recordsetedit-method-dao"></a><span data-ttu-id="5218b-102">Método Recordset.Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="5218b-102">Recordset.Edit Method (DAO)</span></span>

<span data-ttu-id="5218b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5218b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5218b-104">Copia el registro actual de un objeto **[Recordset](recordset-object-dao.md)** actualizable al búfer de copia para su posterior edición.</span><span class="sxs-lookup"><span data-stu-id="5218b-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="5218b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5218b-105">Syntax</span></span>

<span data-ttu-id="5218b-106">*expression* .Edit</span><span class="sxs-lookup"><span data-stu-id="5218b-106">*expression* .Edit</span></span>

<span data-ttu-id="5218b-107">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5218b-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5218b-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5218b-108">Remarks</span></span>

<span data-ttu-id="5218b-p101">Una vez utilizado el método **Edit**, los cambios realizados en los campos del registro activo se copian en el búfer de copia. Tras realizar los cambios que desee en el registro, utilice el método **[Update](recordset-update-method-dao.md)** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="5218b-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="5218b-111">El registro activo sigue estando activo después de utilizar **Edit**.</span><span class="sxs-lookup"><span data-stu-id="5218b-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="5218b-112">Si edita un registro y ejecuta luego cualquier operación para desplazarse a otro registro pero sin usar primero **Update**, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="5218b-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="5218b-113">Además, si cierra recordset o termina el procedimiento que declara el objeto **Recordset** o el objeto **[Database](database-object-dao.md)** o **[Connection](connection-object-dao.md)** principal, el registro editado se descarta sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="5218b-113">In addition, if you close  recordset or end the procedure which declares the **Recordset** or the parent [**Database**](connection-object-dao.md) or **Connection** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="5218b-114">El uso de **Edit** produce un error si:</span><span class="sxs-lookup"><span data-stu-id="5218b-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="5218b-115">No hay un registro activo.</span><span class="sxs-lookup"><span data-stu-id="5218b-115">There is no current record.</span></span>

- <span data-ttu-id="5218b-116">El objeto **Connection**, **Database** o **Recordset** se abrió como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5218b-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="5218b-117">No hay campos actualizables en el registro.</span><span class="sxs-lookup"><span data-stu-id="5218b-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="5218b-118">El objeto **Database** o **Recordset** se abrió para uso exclusivo de otro usuario (área de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5218b-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="5218b-119">Otro usuario ha bloqueado la página que contiene el registro (área de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5218b-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="5218b-p103">En un área de trabajo de Microsoft Access, cuando el valor de la propiedad [**LockEdits**](recordset-lockedits-property-dao.md) del objeto **Recordset** es **True** (bloqueo pesimista) en un entorno multiusuario, el registro permanece bloqueado desde que se usa **Edit** hasta que finaliza la actualización. Si el valor de la propiedad **LockEdits** es **False** (bloqueo optimista), el registro se bloquea y se compara con el registro previo a la modificación antes de actualizarse en la base de datos. Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error en tiempo de ejecución si usa **OpenRecordset** sin especificar **dbSeeChanges**. De manera predeterminada, las bases de datos de ODBC e ISAM instalable conectadas al motor de base de datos de Microsoft Access usan siempre el bloqueo optimista.</span><span class="sxs-lookup"><span data-stu-id="5218b-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="5218b-p104">Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** o **Edit** en un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5218b-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="5218b-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5218b-126">Example</span></span>

<span data-ttu-id="5218b-p105">En este ejemplo se usa el método **Edit** para reemplazar los datos actuales por el nombre especificado. Se necesita el procedimiento EditName para que se pueda ejecutar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5218b-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Sub EditName(rstTemp As Recordset, _ 
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
