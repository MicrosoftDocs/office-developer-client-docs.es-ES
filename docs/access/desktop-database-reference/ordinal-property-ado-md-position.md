---
title: Ordinal (propiedad, posición de ADO MD)
TOCTitle: Ordinal Property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e953c038947073d3cdeb971e705c80f63d12a15b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483981"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal (propiedad, posición de ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Identifica exclusivamente una posición a lo largo de un eje.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

El **Ordinal** de un objeto [Position](position-object-ado-md.md) corresponde al índice del objeto **Position** dentro de la colección [Positions](positions-collection-ado-md.md).

Una celda se puede recuperar rápidamente utilizando el **Ordinal** de la **posición** a lo largo de cada eje con la propiedad [Item](item-property-ado-md-cellset.md) del objeto [Cellset](cellset-object-ado-md.md).

