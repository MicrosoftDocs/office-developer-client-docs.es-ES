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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712459"
---
# <a name="fieldvisiblevalue-property-dao"></a>Propiedad Field.VisibleValue (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . VisibleValue

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Esta propiedad contiene el valor del campo que está actualmente en la base de datos del servidor. Durante una actualización por lotes "optimista", puede producirse un conflicto si un segundo cliente modificó el mismo campo y registro entre el momento en que el primer cliente recuperó los datos y el intento de actualización del primer cliente. Cuando esto sucede, se tendrá acceso al valor establecido por el segundo cliente mediante esta propiedad.

