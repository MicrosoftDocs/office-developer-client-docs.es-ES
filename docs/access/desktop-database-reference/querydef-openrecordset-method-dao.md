---
title: Método QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302852"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="f10de-102">Método QueryDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="f10de-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="f10de-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f10de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f10de-104">Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="f10de-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f10de-105">Syntax</span></span>

<span data-ttu-id="f10de-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="f10de-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="f10de-107">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="f10de-107">*expression*  A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f10de-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="f10de-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f10de-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f10de-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f10de-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="f10de-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f10de-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f10de-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f10de-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f10de-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f10de-113"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="f10de-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="f10de-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="f10de-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f10de-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f10de-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f10de-116">Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</span><span class="sxs-lookup"><span data-stu-id="f10de-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="f10de-117"><strong>NOTA</strong>: si abre un <STRONG>Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica un tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo tabla, si es posible.</span><span class="sxs-lookup"><span data-stu-id="f10de-117"> > If you open a Recordset in a Microsoft Access workspace and you don't specify a type, OpenRecordset creates a table-type Recordset, if possible.</span></span> <span data-ttu-id="f10de-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f10de-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f10de-119"><em>Opciones</em></span><span class="sxs-lookup"><span data-stu-id="f10de-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="f10de-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="f10de-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="f10de-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f10de-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f10de-122">Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifican características del nuevo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f10de-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="f10de-123"><strong>NOTA</strong>: las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente exclusivas, y usar las dos producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f10de-123">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="f10de-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span><span class="sxs-lookup"><span data-stu-id="f10de-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f10de-125"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="f10de-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="f10de-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="f10de-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="f10de-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f10de-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f10de-128">Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo del <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f10de-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="f10de-129"><strong>NOTA</strong>: Puede usar <STRONG>dbReadOnly</STRONG> en el argumento options o en el argumento lockedits, pero no en ambos.</span><span class="sxs-lookup"><span data-stu-id="f10de-129">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="f10de-130">Si lo usa para ambos argumentos, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f10de-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="f10de-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f10de-131">Return value</span></span>

<span data-ttu-id="f10de-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="f10de-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="f10de-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f10de-133">Remarks</span></span>

<span data-ttu-id="f10de-134">Debe usar también la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.</span><span class="sxs-lookup"><span data-stu-id="f10de-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="f10de-p104">Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **[MoveLast](recordset-movelast-method-dao.md)** en cuanto se abra el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f10de-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="f10de-137">Cerrar un objeto **Recordset** con el método **Close** lo elimina automáticamente de la colección **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="f10de-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="f10de-138">Si *origen* hace referencia a una instrucción SQL compuesta por una cadena concatenada con un valor de tipo no entero y los parámetros del sistema especifican un carácter decimal que no es de EE.UU., como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), se produce un error cuando intenta abrir **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f10de-138">If source refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the Recordset.</span></span> <span data-ttu-id="f10de-139">Esto se debe a que durante la concatenación, el número se convierte en una cadena que usa el carácter decimal predeterminado de su sistema y SQL solo acepta caracteres decimales de EE.UU.</span><span class="sxs-lookup"><span data-stu-id="f10de-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


