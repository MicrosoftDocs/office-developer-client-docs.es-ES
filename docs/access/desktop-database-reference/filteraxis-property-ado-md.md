---
title: FilterAxis (propiedad, ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f298acf3a9250a0376ba31f5d3afc6b079ce0c78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867709"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis (propiedad, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Indica información de filtro acerca del conjunto de celdas activo.

## <a name="return-values"></a>Valores devueltos

Devuelve un objeto [Axis](axis-object-ado-md.md) y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **FilterAxis** para devolver información acerca de las dimensiones que se utilizaron para distribuir los datos en sectores. La propiedad [DimensionCount](dimensioncount-property-ado-md.md) del **eje** devuelve el número de dimensiones del rebanador. Este eje normalmente tiene sólo una fila.

El **eje** que devuelve [FilterAxis](filteraxis-property-ado-md.md) no está contenido en la colección [Axes](axes-collection-ado-md.md) correspondiente a un objeto [Cellset](cellset-object-ado-md.md).

