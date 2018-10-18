---
title: Connection.CreateQueryDef Method (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 35bf71742133b65c2e55583e1c62922cb5bc91e8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606042"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="14ff8-102">Connection.CreateQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="14ff8-102">Connection.CreateQueryDef Method (DAO)</span></span>


<span data-ttu-id="14ff8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="14ff8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="14ff8-104">Crea un nuevo objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="14ff8-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ff8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14ff8-105">Syntax</span></span>

<span data-ttu-id="14ff8-106">*expresión* . CreateQueryDef (***nombre***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="14ff8-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="14ff8-107">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="14ff8-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="14ff8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14ff8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14ff8-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="14ff8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="14ff8-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="14ff8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="14ff8-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="14ff8-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="14ff8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="14ff8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14ff8-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="14ff8-113">Name</span></span></p></td>
<td><p><span data-ttu-id="14ff8-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="14ff8-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="14ff8-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="14ff8-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="14ff8-116"><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="14ff8-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14ff8-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="14ff8-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="14ff8-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="14ff8-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="14ff8-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="14ff8-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="14ff8-p101"><strong>Variant</strong> (subtipo <strong>String</strong>) que es una instrucción SQL que define el objeto <strong>QueryDef</strong>. Si omite este argumento, puede definir el objeto <strong>QueryDef</strong> estableciendo su propiedad <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes o después de agregarlo a una colección.</span><span class="sxs-lookup"><span data-stu-id="14ff8-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14ff8-122"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="14ff8-122"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="14ff8-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14ff8-123">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="14ff8-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14ff8-124">Return value</span></span>
>>>>>>> <span data-ttu-id="14ff8-125">master</span><span class="sxs-lookup"><span data-stu-id="14ff8-125">master</span></span>

<span data-ttu-id="14ff8-126">Objeto QueryDef</span><span class="sxs-lookup"><span data-stu-id="14ff8-126">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="14ff8-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14ff8-127">Remarks</span></span>

<span data-ttu-id="14ff8-128">En un área de trabajo de Microsoft Access, si proporciona cualquier otro elemento que no sea una cadena de longitud cero para el nombre al crear un objeto **QueryDef**, el objeto **QueryDef** resultante se agrega automáticamente a la colección **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="14ff8-128">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="14ff8-129">Si el objeto especificado por el nombre ya es un miembro de la colección **QueryDefs** , se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="14ff8-129">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="14ff8-130">Puede crear un **objeto QueryDef** de temporal utilizando una cadena de longitud cero para el argumento name cuando ejecute el método **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="14ff8-130">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="14ff8-131">También puede hacerlo estableciendo la propiedad **[Name](connection-name-property-dao.md)** de un **objeto QueryDef** de recién creado en una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="14ff8-131">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="14ff8-132">Los objetos **QueryDef** temporales son útiles si desea utilizar repetidamente instrucciones SQL sin tener que crear nuevos objetos permanentes en la colección **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="14ff8-132">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="14ff8-133">No se puede anexar un **objeto QueryDef** de temporal a cualquier colección debido a que una cadena de longitud cero no es un nombre válido para un objeto **QueryDef** permanente.</span><span class="sxs-lookup"><span data-stu-id="14ff8-133">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="14ff8-134">Siempre puede establecer el **nombre** y las propiedades **SQL** del objeto **QueryDef** recién creado y, posteriormente, anexe el **objeto QueryDef** a la colección **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="14ff8-134">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="14ff8-135">Para ejecutar una instrucción SQL en un objeto **QueryDef**, use el método **[Execute](connection-execute-method-dao.md)** u **[OpenRecordset](connection-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="14ff8-135">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="14ff8-136">El uso de un objeto **QueryDef** es el método recomendado para realizar consultas de paso SQL con bases de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="14ff8-136">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="14ff8-137">Para quitar un objeto **QueryDef** de una colección **QueryDefs** en una base de datos del motor de base de datos de Microsoft Access, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="14ff8-137">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

