---
title: PageSize (propiedad, ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483728"
---
# <a name="pagesize-property-ado"></a>PageSize (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica cuántos registros constituyen una página en el objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que indica cuántos registros hay en una página. El valor predeterminado es 10.

## <a name="remarks"></a>Comentarios

Use la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor web cuando se desea permitir al usuario que se desplace por los datos de las páginas para ver un número determinado de registros a la vez.

Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.

