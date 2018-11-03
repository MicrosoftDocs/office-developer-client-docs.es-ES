---
title: Database.MakeReplica (método) (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a47709d1be3eab66f849e076c5756d5081d28fc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930234"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="be6e7-102">Database.MakeReplica (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="be6e7-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="be6e7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be6e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be6e7-104">Crea una nueva réplica a partir de otra réplica de base de datos (sólo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="be6e7-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="be6e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be6e7-105">Syntax</span></span>

<span data-ttu-id="be6e7-106">*expresión* . MakeReplica (***nombreruta***, ***Descripción***, ***Opciones***)</span><span class="sxs-lookup"><span data-stu-id="be6e7-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="be6e7-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="be6e7-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="be6e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be6e7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be6e7-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="be6e7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="be6e7-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="be6e7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="be6e7-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="be6e7-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="be6e7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="be6e7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be6e7-113">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="be6e7-113">PathName</span></span></p></td>
<td><p><span data-ttu-id="be6e7-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="be6e7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="be6e7-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="be6e7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="be6e7-p101">Ruta de acceso y nombre de archivo de la nueva réplica. Si la réplica es un nombre de archivo existente, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="be6e7-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be6e7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="be6e7-118">Description</span></span></p></td>
<td><p><span data-ttu-id="be6e7-119">Necesario</span><span class="sxs-lookup"><span data-stu-id="be6e7-119">Required</span></span></p></td>
<td><p><span data-ttu-id="be6e7-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="be6e7-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="be6e7-121"><strong>String</strong> que describe la réplica que se va a crear</span><span class="sxs-lookup"><span data-stu-id="be6e7-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be6e7-122">Options</span><span class="sxs-lookup"><span data-stu-id="be6e7-122">Options</span></span></p></td>
<td><p><span data-ttu-id="be6e7-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="be6e7-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="be6e7-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="be6e7-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="be6e7-125">Constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> que especifica las características de la réplica que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="be6e7-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="be6e7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be6e7-126">Remarks</span></span>

<span data-ttu-id="be6e7-127">Una réplica parcial recién creada tendrá todas las propiedades **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** establecidas en **False**, lo que indica que no habrá datos en las tablas.</span><span class="sxs-lookup"><span data-stu-id="be6e7-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="be6e7-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be6e7-128">Example</span></span>

<span data-ttu-id="be6e7-129">Esta función utiliza el método **MakeReplica** para crear una réplica adicional de un diseño principal existente.</span><span class="sxs-lookup"><span data-stu-id="be6e7-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="be6e7-130">El argumento intOptions puede ser una combinación de las constantes **dbRepMakeReadOnly** y **dbRepMakePartial**, o puede ser 0.</span><span class="sxs-lookup"><span data-stu-id="be6e7-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="be6e7-131">Por ejemplo, para crear una réplica parcial de sólo lectura, debe pasar el valor **dbRepMakeReadOnly** + **dbRepMakePartial** como el valor de intOptions.</span><span class="sxs-lookup"><span data-stu-id="be6e7-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

