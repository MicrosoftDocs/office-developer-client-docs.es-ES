---
title: Propiedad Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292919"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="da6a5-102">Propiedad Field.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="da6a5-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="da6a5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da6a5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="da6a5-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da6a5-104">Syntax</span></span>

<span data-ttu-id="da6a5-105">*expresión* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="da6a5-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="da6a5-106">*expression* Variable que representa un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="da6a5-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da6a5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da6a5-107">Remarks</span></span>

<span data-ttu-id="da6a5-p101">Esta propiedad contiene el valor del campo que está actualmente en la base de datos del servidor. Durante una actualización por lotes "optimista", puede producirse un conflicto si un segundo cliente modificó el mismo campo y registro entre el momento en que el primer cliente recuperó los datos y el intento de actualización del primer cliente. Cuando esto sucede, se tendrá acceso al valor establecido por el segundo cliente mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="da6a5-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

