---
title: Método Recordset.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 223612be0b2fca457c9aa78af0394c19574096f0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606524"
---
# <a name="recordsetopenrecordset-method-dao"></a><span data-ttu-id="ca794-102">Método Recordset.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="ca794-102">Recordset.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="ca794-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca794-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ca794-104">Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ca794-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca794-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca794-105">Syntax</span></span>

<span data-ttu-id="ca794-106">*expresión* . OpenRecordset (***tipo***, ***las opciones de***)</span><span class="sxs-lookup"><span data-stu-id="ca794-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="ca794-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ca794-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ca794-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca794-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca794-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="ca794-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ca794-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="ca794-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ca794-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ca794-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ca794-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca794-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca794-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="ca794-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ca794-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ca794-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ca794-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ca794-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ca794-p101">Origen de los registros para el nuevo <strong>Recordset</strong>. El origen puede ser un nombre de tabla o de consulta, o una instrucción SQL que devuelve registros. Para los objetos <strong>Recordset</strong> de tipo tabla en las bases de datos del motor de base de datos de Microsoft Access, el origen solo puede ser un nombre de tabla.  </span><span class="sxs-lookup"><span data-stu-id="ca794-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca794-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca794-119">Type</span></span></p></td>
<td><p><span data-ttu-id="ca794-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="ca794-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ca794-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ca794-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ca794-122">Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</span><span class="sxs-lookup"><span data-stu-id="ca794-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="ca794-p102">Si abre un <STRONG>Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica un tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo tabla, si es posible. Si especifica una tabla o una consulta vinculada, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo conjunto de registros dinámicos.</span><span class="sxs-lookup"><span data-stu-id="ca794-p102">If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></P>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca794-125">Options</span><span class="sxs-lookup"><span data-stu-id="ca794-125">Options</span></span></p></td>
<td><p><span data-ttu-id="ca794-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="ca794-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="ca794-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ca794-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ca794-128">Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica las características del nuevo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca794-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="ca794-p103">Las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente exclusivas, y usar las dos producirá un error. Proporcionar un argumento lockedits cuando las opciones usan la constante <STRONG>dbReadOnly</STRONG> también produce un error.</span><span class="sxs-lookup"><span data-stu-id="ca794-p103">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca794-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="ca794-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="ca794-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="ca794-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="ca794-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ca794-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ca794-134">Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo de <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca794-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="ca794-p104">Puede usar <STRONG>dbReadOnly</STRONG> en el argumento options o en el argumento lockedits, pero no en ambos. Si lo usa para los dos argumentos, ocurre un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ca794-p104">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca794-137"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ca794-137"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="ca794-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca794-138">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="ca794-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca794-139">Return value</span></span>
>>>>>>> <span data-ttu-id="ca794-140">master</span><span class="sxs-lookup"><span data-stu-id="ca794-140">master</span></span>

<span data-ttu-id="ca794-141">Recordset</span><span class="sxs-lookup"><span data-stu-id="ca794-141">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="ca794-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca794-142">Remarks</span></span>

<span data-ttu-id="ca794-p105">En general, si el usuario obtiene este error mientras actualiza un registro, el código debe actualizar el contenido de los campos y recuperar los valores recién modificados. Si el error se produce al eliminar un registro, el código puede mostrar los nuevos datos de registros al usuario y un mensaje en el que se indica que los datos han cambiado recientemente. En ese momento, el código puede pedir una confirmación de que aún se desea eliminar el registro.</span><span class="sxs-lookup"><span data-stu-id="ca794-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="ca794-146">Debe usar también la constante **dbSeeChanges** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.</span><span class="sxs-lookup"><span data-stu-id="ca794-146">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="ca794-p106">Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **MoveLast** en cuanto se abra el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ca794-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="ca794-149">Cerrar un objeto **Recordset** con el método **[Close](connection-close-method-dao.md)** lo elimina automáticamente de la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ca794-149">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ca794-150">Si <EM>origen</EM> hace referencia a una instrucción SQL consta de una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se produce un error al intentar abrir el <STRONG>conjunto de registros</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ca794-150">If <EM>source</EM> refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="ca794-151">Esto se debe a que, durante la concatenación, el número se convierte en una cadena con el carácter decimal predeterminado del sistema, y SQL solo acepta los caracteres decimales de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="ca794-151">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span></P>


