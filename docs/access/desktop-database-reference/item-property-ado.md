---
title: Item (propiedad, ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73e6240b92a34a6ff1d215cd3211a844f10fe766
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868315"
---
# <a name="item-property-ado"></a>Item (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica un miembro específico de una colección, por nombre o número ordinal.

## <a name="syntax"></a>Sintaxis

*Objeto*de conjunto de = *colección*. Item (Index)

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia de objeto.

## <a name="parameters"></a>Parámetros

- *Index*

- Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Item** para devolver un objeto específico de una colección. Si el **elemento** no se puede encontrar un objeto en la colección que corresponde al argumento *Index* , se produce un error. Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.

**Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, los siguientes formatos de sintaxis son intercambiables:

```vb
    collection.Item (Index)
    collection (Index)
```
