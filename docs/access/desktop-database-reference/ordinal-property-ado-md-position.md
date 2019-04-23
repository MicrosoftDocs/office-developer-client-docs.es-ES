---
title: Ordinal (propiedad, Position de ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288193"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal (propiedad, Position de ADO MD)


**Se aplica a:** Access 2013, Office 2013

Identifica exclusivamente una posición a lo largo de un eje.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

El **Ordinal** de un objeto [Position](position-object-ado-md.md) corresponde al índice del objeto **Position** dentro de la colección [Positions](positions-collection-ado-md.md).

Una celda se puede recuperar rápidamente utilizando el **Ordinal** de la **posición** a lo largo de cada eje con la propiedad [Item](item-property-ado-md-cellset.md) del objeto [Cellset](cellset-object-ado-md.md).

