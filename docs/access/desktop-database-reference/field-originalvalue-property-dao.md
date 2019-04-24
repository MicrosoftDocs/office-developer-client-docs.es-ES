---
title: Propiedad Field. OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293003"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="aa63d-102">Propiedad Field. OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa63d-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="aa63d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa63d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="aa63d-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa63d-104">Syntax</span></span>

<span data-ttu-id="aa63d-105">*expresión* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="aa63d-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="aa63d-106">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="aa63d-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa63d-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa63d-107">Remarks</span></span>

<span data-ttu-id="aa63d-p101">Durante una actualización por lotes optimista, puede producirse un conflicto si el segundo cliente modifica el mismo campo y se registra en el intervalo de tiempo que transcurre desde que el primer cliente recupera los datos hasta que realiza un intento de actualización. La propiedad **OriginalValue** contiene el valor del campo al tiempo que comienza la última actualización por lotes **Update**. Si este valor no coincide con el valor real en la base de datos cuando la actualización por lotes **Update** intenta escribir en la base de datos, se produce un conflicto. Si esto ocurre, se tendrá acceso al nuevo valor en la base de datos a través de la propiedad **[VisibleValue](field-visiblevalue-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="aa63d-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

