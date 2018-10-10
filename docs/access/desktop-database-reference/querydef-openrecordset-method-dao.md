---
title: QueryDef.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50d31adf61df0848a22c9c22f229b22c7992d913
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483870"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="2263f-102">QueryDef.OpenRecordset Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2263f-102">QueryDef.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="2263f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2263f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2263f-104">Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="2263f-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2263f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2263f-105">Syntax</span></span>

<span data-ttu-id="2263f-106">*expresión* . OpenRecordset (***tipo***, ***Opciones***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="2263f-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="2263f-107">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2263f-107">*expression* A variable that represents a **QueryDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2263f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2263f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2263f-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2263f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2263f-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="2263f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2263f-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2263f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2263f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2263f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2263f-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="2263f-113">Type</span></span></p></td>
<td><p><span data-ttu-id="2263f-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="2263f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="2263f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2263f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2263f-116">Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</span><span class="sxs-lookup"><span data-stu-id="2263f-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="2263f-p101">Si abre un <STRONG>Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica un tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo tabla, si es posible. Si especifica una tabla o una consulta vinculada, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo conjunto de registros dinámicos.</span><span class="sxs-lookup"><span data-stu-id="2263f-p101">If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2263f-119">Options</span><span class="sxs-lookup"><span data-stu-id="2263f-119">Options</span></span></p></td>
<td><p><span data-ttu-id="2263f-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="2263f-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="2263f-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2263f-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2263f-122">Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica las características del nuevo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2263f-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="2263f-p102">Las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente exclusivas, y usar las dos producirá un error. Proporcionar un argumento lockedits cuando las opciones usan la constante <STRONG>dbReadOnly</STRONG> también produce un error.</span><span class="sxs-lookup"><span data-stu-id="2263f-p102">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></P>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2263f-125">LockEdit</span><span class="sxs-lookup"><span data-stu-id="2263f-125">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="2263f-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="2263f-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="2263f-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2263f-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2263f-128">Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo de <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2263f-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="2263f-p103">Puede usar <STRONG>dbReadOnly</STRONG> en el argumento options o en el argumento lockedits, pero no en ambos. Si lo usa para los dos argumentos, ocurre un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2263f-p103">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span></P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2263f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2263f-131">Return Value</span></span>

<span data-ttu-id="2263f-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="2263f-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="2263f-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2263f-133">Remarks</span></span>

<span data-ttu-id="2263f-134">Debe usar también la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.</span><span class="sxs-lookup"><span data-stu-id="2263f-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="2263f-p104">Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **[MoveLast](recordset-movelast-method-dao.md)** en cuanto se abra el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2263f-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="2263f-137">Cerrar un objeto **Recordset** con el método **Close** lo elimina automáticamente de la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="2263f-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2263f-138">Si <EM>origen</EM> hace referencia a una instrucción SQL consta de una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se produce un error al intentar abrir el <STRONG>conjunto de registros</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2263f-138">If <EM>source</EM> refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="2263f-139">Esto se debe a que, durante la concatenación, el número se convierte en una cadena con el carácter decimal predeterminado del sistema, y SQL solo acepta los caracteres decimales de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="2263f-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span></P>

