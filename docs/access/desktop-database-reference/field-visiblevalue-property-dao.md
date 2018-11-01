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
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue Property (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . VisibleValue

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Esta propiedad contiene el valor del campo que está actualmente en la base de datos del servidor. Durante una actualización por lotes "optimista", puede producirse un conflicto si un segundo cliente modificó el mismo campo y registro entre el momento en que el primer cliente recuperó los datos y el intento de actualización del primer cliente. Cuando esto sucede, se tendrá acceso al valor establecido por el segundo cliente mediante esta propiedad.

