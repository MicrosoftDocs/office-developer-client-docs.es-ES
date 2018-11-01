---
title: PageSize (propiedad, ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883277"
---
# <a name="pagesize-property-ado"></a>PageSize (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica cuántos registros constituyen una página en el objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que indica cuántos registros hay en una página. El valor predeterminado es 10.

## <a name="remarks"></a>Comentarios

Use la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor web cuando desea permitir al usuario desplazarse por los datos, ve un cierto número de registros a la vez.

Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.

