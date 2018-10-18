---
title: Principal (propiedad, ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603339"
---
# <a name="parent-property-ado-md"></a>Principal (propiedad, ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Indica cuál es el elemento principal del elemento activo en una jerarquía.

<<<<<<< HEAD
## <a name="return-values"></a>Valores devueltos
=======
## <a name="return-values"></a>Valores devueltos
>>>>>>> master

Devuelve un objeto [Member](member-object-ado-md.md) y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Un elemento que está en el nivel superior de una jerarquía (la raíz) no tiene elemento principal. Esta propiedad sólo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.

