---
title: ChildCount (propiedad, ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ac5e65356e7ee66cda864bffc983ae1d394825b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879609"
---
# <a name="childcount-property-ado-md"></a>ChildCount (propiedad, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Indica el número de elementos para los que el objeto [Member](member-object-ado-md.md) activo es el principal en una jerarquía.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Use la propiedad **ChildCount** para devolver una estimación del número de elementos secundarios que tiene un objeto **Member**. Los elementos secundarios de un objeto **Member** se pueden obtener mediante la propiedad [Children](children-property-ado-md.md).

Para objetos **Member** a partir de un objeto [Position](position-object-ado-md.md), el máximo valor que se puede devolver es 65.536. Si la cantidad real de elementos secundarios es mayor que 65.536, el valor devuelto seguirá siendo 65.536. Por tanto, la aplicación debería interpretar un valor **ChildCount** de 65.536 como que existe esta cantidad o más de elementos secundarios.

Para objetos **Member** a partir de un objeto [Level](level-object-ado-md.md), utilice la propiedad [Contar](count-property-ado.md) de la colección de ADO con la colección **Children** para determinar el número exacto de elementos secundarios. La determinación del número exacto de elementos secundarios puede requerir su tiempo si la cantidad de secundarios en la colección es elevada.

