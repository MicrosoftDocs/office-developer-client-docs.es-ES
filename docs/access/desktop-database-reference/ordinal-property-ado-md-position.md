---
title: Ordinal (propiedad, Position de ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abf355cc4d066604035fddbbe8f8a428d8c7a6b0
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944784"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal (propiedad, Position de ADO MD)


**Se aplica a**: Access 2013, Office 2013

Identifica exclusivamente una posición a lo largo de un eje.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

El **Ordinal** de un objeto [Position](position-object-ado-md.md) corresponde al índice del objeto **Position** dentro de la colección [Positions](positions-collection-ado-md.md).

Una celda se puede recuperar rápidamente utilizando el **Ordinal** de la **posición** a lo largo de cada eje con la propiedad [Item](item-property-ado-md-cellset.md) del objeto [Cellset](cellset-object-ado-md.md).

