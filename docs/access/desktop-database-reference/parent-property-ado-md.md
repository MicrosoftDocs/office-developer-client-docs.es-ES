---
title: Principal (propiedad, ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7beba341a2374e1868c67c8f7b4fab73c71c0ba8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880302"
---
# <a name="parent-property-ado-md"></a>Principal (propiedad, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Indica cuál es el elemento principal del elemento activo en una jerarquía.

## <a name="return-values"></a>Valores devueltos

Devuelve un objeto [Member](member-object-ado-md.md) y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Un elemento que está en el nivel superior de una jerarquía (la raíz) no tiene elemento principal. Esta propiedad sólo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.

