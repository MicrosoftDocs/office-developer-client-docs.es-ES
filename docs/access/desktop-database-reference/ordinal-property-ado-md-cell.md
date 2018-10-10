---
title: Ordinal (propiedad) (celda de ADO MD)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 284e2cac2c1a86d87e39d9913a262fbafb435ece
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484080"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal (propiedad) (celda de ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Identifica exclusivamente una celda por su posición dentro de un conjunto de celdas.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

El valor ordinal de la celda identifica inequívocamente la celda dentro de un conjunto de celdas. Conceptualmente, las celdas se numeran en un conjunto de celdas como si el conjunto de celdas fuera una matriz de *p* dimensiones, donde *p* es el número de [ejes](axes-collection-ado-md.md). Las celdas se numeran empezando desde cero en orden de fila mayor.

El valor ordinal de la celda se puede utilizar con la propiedad [Item](item-property-ado-md-cellset.md) del objeto [Cellset](cellset-object-ado-md.md) para recuperar rápidamente la [celda](cell-object-ado-md.md).

