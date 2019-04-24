---
title: Método Recordset2. OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307255"
---
# <a name="recordset2openrecordset-method-dao"></a><span data-ttu-id="97939-102">Método Recordset2. OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="97939-102">Recordset2.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="97939-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97939-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97939-104">Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="97939-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="97939-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97939-105">Syntax</span></span>

<span data-ttu-id="97939-106">*expresión* . OpenRecordset (***tipo***, ***Opciones***)</span><span class="sxs-lookup"><span data-stu-id="97939-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="97939-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="97939-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="97939-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="97939-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97939-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="97939-109">Name</span></span></p></th>
<th><p><span data-ttu-id="97939-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="97939-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="97939-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="97939-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="97939-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="97939-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97939-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="97939-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="97939-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="97939-114">Required</span></span></p></td>
<td><p><span data-ttu-id="97939-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="97939-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="97939-p101">Origen de los registros para el nuevo <strong>Recordset</strong>. El origen puede ser un nombre de tabla o de consulta, o una instrucción SQL que devuelve registros. Para los objetos <strong>Recordset</strong> de tipo tabla en las bases de datos del motor de base de datos de Microsoft Access, el origen solo puede ser un nombre de tabla.  </span><span class="sxs-lookup"><span data-stu-id="97939-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97939-119"><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="97939-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="97939-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="97939-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="97939-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="97939-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="97939-122">Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</span><span class="sxs-lookup"><span data-stu-id="97939-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="97939-123"><strong>Nota</strong>: Si abre un <STRONG>objeto Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica un tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>objeto Recordset</STRONG>de tipo tabla, si es posible.</span><span class="sxs-lookup"><span data-stu-id="97939-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="97939-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="97939-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97939-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="97939-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="97939-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="97939-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="97939-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="97939-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="97939-128">Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica las características del nuevo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="97939-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="97939-129"><strong>Nota</strong>: las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente excluyentes y, si se usan ambas, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="97939-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="97939-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span><span class="sxs-lookup"><span data-stu-id="97939-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97939-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="97939-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="97939-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="97939-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="97939-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="97939-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="97939-134">Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo de <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="97939-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="97939-135"><strong>Nota</strong>: puede usar <STRONG>dbReadOnly</STRONG> en el argumento Options o en el argumento LockEdits, pero no en ambos.</span><span class="sxs-lookup"><span data-stu-id="97939-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="97939-136">If you use it for both arguments, a run-time error occurs.</span><span class="sxs-lookup"><span data-stu-id="97939-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="97939-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97939-137">Return value</span></span>

<span data-ttu-id="97939-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="97939-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="97939-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97939-139">Remarks</span></span>

<span data-ttu-id="97939-p105">En general, si el usuario obtiene este error mientras actualiza un registro, el código debe actualizar el contenido de los campos y recuperar los valores recién modificados. Si el error se produce al eliminar un registro, el código puede mostrar los nuevos datos de registros al usuario y un mensaje en el que se indica que los datos han cambiado recientemente. En ese momento, el código puede pedir una confirmación de que aún se desea eliminar el registro.</span><span class="sxs-lookup"><span data-stu-id="97939-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="97939-143">Debe usar también la constante **dbSeeChanges** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.</span><span class="sxs-lookup"><span data-stu-id="97939-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="97939-p106">Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **MoveLast** en cuanto se abra el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="97939-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="97939-146">Cerrar un objeto **Recordset** con el método **[Close](connection-close-method-dao.md)** lo elimina automáticamente de la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="97939-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="97939-147">Si *source* hace referencia a una instrucción SQL compuesta por una cadena concatenada con un valor no entero, y los parámetros del sistema especifican un carácter no. decimal como una coma (por ejemplo, strSQL = "Price &gt; " &amp; lngPrice e lngPrice = 125, 50), se produce un error al intentar abrir el **objeto Recordset**.</span><span class="sxs-lookup"><span data-stu-id="97939-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="97939-148">Esto se debe a que durante la concatenación, el número se convierte en una cadena que usa el carácter decimal predeterminado de su sistema y SQL solo acepta caracteres decimales de EE.UU.</span><span class="sxs-lookup"><span data-stu-id="97939-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


