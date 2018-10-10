---
title: Field2.VisibleValue Property (DAO)
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
ms.openlocfilehash: 9c901045f1f856142a628fb31806610e7d5dce43
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483714"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="99555-102">Field2.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="99555-102">Field2.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="99555-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="99555-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="99555-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99555-104">Syntax</span></span>

<span data-ttu-id="99555-105">*expresión* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="99555-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="99555-106">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="99555-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="99555-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99555-107">Remarks</span></span>

<span data-ttu-id="99555-p101">Esta propiedad contiene el valor del campo que está actualmente en la base de datos del servidor. Durante una actualización por lotes "optimista", puede producirse un conflicto si un segundo cliente modificó el mismo campo y registro entre el momento en que el primer cliente recuperó los datos y el intento de actualización del primer cliente. Cuando esto sucede, se tendrá acceso al valor establecido por el segundo cliente mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="99555-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

