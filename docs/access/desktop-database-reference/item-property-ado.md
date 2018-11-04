---
title: Item (propiedad, ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4afbb31fb95aeea66d9cf93624b95c8796e2d25
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949365"
---
# <a name="item-property-ado"></a>Item (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica un miembro específico de una colección, por nombre o número ordinal.

## <a name="syntax"></a>Sintaxis

*Objeto*de conjunto de = *colección*. Item (Index)

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia de objeto.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Index* |Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.|

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Item** para devolver un objeto específico de una colección. Si el **elemento** no se puede encontrar un objeto en la colección que corresponde al argumento *Index* , se produce un error. Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.

**Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, los siguientes formatos de sintaxis son intercambiables:

```vb
    collection.Item (Index)
    collection (Index)
```
