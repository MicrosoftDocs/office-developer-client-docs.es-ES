---
title: Description (propiedad, ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd66e0288e20bcf38adefc2fcc30f1856ebf3e6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606874"
---
# <a name="description-property-ado-md"></a>Description (propiedad, ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Devuelve un texto de explicación del objeto actual.

<<<<<<< HEAD
## <a name="return-values"></a>Valores devueltos
=======
## <a name="return-values"></a>Valores devueltos
>>>>>>> master

Devuelve un valor **String** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Para objetos [Member](member-object-ado-md.md), **Description** se aplica únicamente a elementos de medida y de fórmula. **Description** devuelve una cadena vacía ("") para todos los demás tipos de elementos. Para obtener más información acerca de los distintos tipos de elementos, vea la propiedad [Tipo](type-property-ado-md.md).

Esta propiedad sólo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.

