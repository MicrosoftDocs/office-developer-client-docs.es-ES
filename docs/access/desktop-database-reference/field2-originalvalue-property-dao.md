---
title: Field2.OriginalValue Property (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c88e03962789946d222acb1a6106c57d5335f3dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889787"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="2546a-102">Field2.OriginalValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2546a-102">Field2.OriginalValue Property (DAO)</span></span>


<span data-ttu-id="2546a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2546a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2546a-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2546a-104">Syntax</span></span>

<span data-ttu-id="2546a-105">*expresión* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="2546a-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="2546a-106">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="2546a-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2546a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2546a-107">Remarks</span></span>

<span data-ttu-id="2546a-p101">Durante una actualización por lotes optimista, puede producirse un conflicto si el segundo cliente modifica el mismo campo y se registra en el intervalo de tiempo que transcurre desde que el primer cliente recupera los datos hasta que realiza un intento de actualización. La propiedad **OriginalValue** contiene el valor del campo al tiempo que comienza la última actualización por lotes **Update**. Si este valor no coincide con el valor real en la base de datos cuando la actualización por lotes **Update** intenta escribir en la base de datos, se produce un conflicto. Si esto ocurre, se tendrá acceso al nuevo valor en la base de datos a través de la propiedad **VisibleValue**.</span><span class="sxs-lookup"><span data-stu-id="2546a-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

