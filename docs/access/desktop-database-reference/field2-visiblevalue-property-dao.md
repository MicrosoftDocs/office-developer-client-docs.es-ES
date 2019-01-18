---
title: Propiedad Field2.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0161ea66068457b53a9667a6739c3a3a0458c8c5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721034"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="7dc84-102">Propiedad Field2.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="7dc84-102">Field2.VisibleValue property (DAO)</span></span>


<span data-ttu-id="7dc84-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dc84-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc84-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7dc84-104">Syntax</span></span>

<span data-ttu-id="7dc84-105">*expresión* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="7dc84-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="7dc84-106">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="7dc84-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc84-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7dc84-107">Remarks</span></span>

<span data-ttu-id="7dc84-p101">Esta propiedad contiene el valor del campo que está actualmente en la base de datos del servidor. Durante una actualización por lotes "optimista", puede producirse un conflicto si un segundo cliente modificó el mismo campo y registro entre el momento en que el primer cliente recuperó los datos y el intento de actualización del primer cliente. Cuando esto sucede, se tendrá acceso al valor establecido por el segundo cliente mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7dc84-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

