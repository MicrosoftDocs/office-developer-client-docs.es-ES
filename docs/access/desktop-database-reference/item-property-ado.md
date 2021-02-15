---
title: Propiedad Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290796"
---
# <a name="item-property-ado"></a>Propiedad Item (ADO)

**Se aplica a:** Access 2013, Office 2013

Indica un miembro específico de una colección, por nombre o número ordinal.

## <a name="syntax"></a>Sintaxis

Establecer *colección de*  =  *objetos*. Item ( Index )

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia de objeto.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Index* |Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.|

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Item** para devolver un objeto específico de una colección. Si **Item** no puede encontrar un objeto en la colección que corresponde al argumento *Index*, se produce un error. Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.

La propiedad **Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, las formas de sintaxis siguientes son intercambiables:

```vb
    collection.Item (Index)
    collection (Index)
```
