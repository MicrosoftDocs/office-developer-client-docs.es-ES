---
title: Propiedad TableDef. ConflictTable ((DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308431"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="97a7a-102">Propiedad TableDef. ConflictTable ((DAO)</span><span class="sxs-lookup"><span data-stu-id="97a7a-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="97a7a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97a7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97a7a-p101">Devuelve el nombre de una tabla de conflictos que contiene los registros de base de datos que generaron conflictos durante la sincronización de dos réplicas (sólo áreas de trabajo de Microsoft Access). **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="97a7a-p101">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only). Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a7a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97a7a-106">Syntax</span></span>

<span data-ttu-id="97a7a-107">*expresión* . ConflictTable (</span><span class="sxs-lookup"><span data-stu-id="97a7a-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="97a7a-108">*expresión* Expresión que devuelve un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="97a7a-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a7a-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97a7a-109">Remarks</span></span>

<span data-ttu-id="97a7a-110">El valor devuelto es un tipo de datos **String** que es una cadena de longitud cero ("") si no hay ninguna tabla de conflictos o la base de datos no es una réplica.</span><span class="sxs-lookup"><span data-stu-id="97a7a-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="97a7a-p102">Si dos usuarios en dos réplicas independientes realizan cada uno un cambio en el mismo registro de la base de datos, los cambios efectuados por uno de los usuarios no se aplicarán en la otra réplica. En consecuencia, el usuario cuyos cambios no se aplicaron debe resolver los conflictos.</span><span class="sxs-lookup"><span data-stu-id="97a7a-p102">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica. Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="97a7a-p103">Los conflictos se producen en el nivel de registro, no entre campos. Por ejemplo, si un usuario cambia el campo Dirección y otro actualiza el campo Teléfono del mismo registro, uno de los cambios se rechaza. Puesto que los conflictos se producen en el nivel de registro, el rechazo se produce incluso si es improbable que el cambio realizado y el cambio rechazado den como resultado un conflicto real de información.</span><span class="sxs-lookup"><span data-stu-id="97a7a-p103">Conflicts occur at the record level, not between fields. For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected. Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="97a7a-p104">El mecanismo de sincronización controla los conflictos de registros mediante la creación de tablas de conflictos, que contienen la información que se habría incluido en la tabla si el cambio hubiera tenido éxito. Puede examinar estas tablas de conflictos fila por fila para realizar las correcciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="97a7a-p104">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful. You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="97a7a-118">Todas las tablas de conflictos se\_denominan conflicto de tablas, donde tabla es el nombre original de la tabla, truncado a la longitud máxima de nombre de tabla.</span><span class="sxs-lookup"><span data-stu-id="97a7a-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

