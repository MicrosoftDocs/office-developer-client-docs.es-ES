---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462359ca02b4a5724c781da303b13a97c73be388
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871209"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="4fdf5-102">Field.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="4fdf5-102">Field.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="4fdf5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fdf5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4fdf5-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fdf5-104">Syntax</span></span>

<span data-ttu-id="4fdf5-105">*expresión* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="4fdf5-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="4fdf5-106">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="4fdf5-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fdf5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fdf5-107">Remarks</span></span>

<span data-ttu-id="4fdf5-p101">Esta propiedad contiene el valor del campo que está actualmente en la base de datos del servidor. Durante una actualización por lotes "optimista", puede producirse un conflicto si un segundo cliente modificó el mismo campo y registro entre el momento en que el primer cliente recuperó los datos y el intento de actualización del primer cliente. Cuando esto sucede, se tendrá acceso al valor establecido por el segundo cliente mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4fdf5-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

